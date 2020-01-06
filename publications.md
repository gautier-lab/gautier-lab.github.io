---
layout: page
title: Publications
permalink: /publications/
---

<script>

//From "http://www.alexhadik.com/blog/2014/6/12/create-pubmed-citations-automatically-using-pubmed-api" adapted from reply to blog post by Les Ansley

var HTMLpublication = '%authors% (%date%). %title% <i>%journal%\</i><b>%volume%</b>%issue%%pages%DOI: <a href="%DOIadd%"target="_blank">%DOI%</a></br></br>' //Formats output

var publications, idStringList;
var pubmedSearchAPI = "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?";
var pubmedSummaryAPI = "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?";
var database = "db=pubmed";
var returnmode = "&retmode=json";
var returnmax = "&retmax=100";
var searchterm = "&term=(((Gautier, Jean[Author]) AND Institute for Cancer Genetics[Affiliation])) OR ((Gautier, Jean[Author]) AND Institute of Cancer Genetics[Affiliation])";
var returntype = "&rettype=abstract";
var idURL = pubmedSearchAPI + database + returnmode + returnmax + searchterm
console.log(idURL);

var getPubmed = function(url) { //passed url
    return new Promise(function(resolve, reject) {
        var xhr = new XMLHttpRequest();
        xhr.open('get', url, true);
        xhr.responseType = 'json';
        xhr.onload = function() {
            var status = xhr.status;
            if (status == 200) { //status 200 signifies OK (http://www.w3schools.com/ajax/ajax_xmlhttprequest_onreadystatechange.asp)
                resolve(xhr.response);
            } else {
                reject(status);
            }
        };
        xhr.send();
    });
};
getPubmed(idURL).then(function(data) {
    var idList = data.esearchresult.idlist;
    idStringList = idList.toString(); //converts the idlist to a string to be appended to the search url
    idStringList = '&id=' + idStringList;
    summaryURL = pubmedSummaryAPI + database + returnmode + returntype + idStringList;
    getPubmed(summaryURL).then(function(summary) {
        publications = formatReferences(summary);
        console.log(publications);	
		document.getElementById("demo").innerHTML = publications;
		
    }, function(status) {
        publications = 'Something went wrong getting the ids.';
    });
}, function(status) {
    publications = 'Something went wrong getting the ids.';
});


function formatReferences(summary) {
    var publicationList = '';
    for (refs in summary.result) {
        if (refs !== 'uids') {
            var authors = '';
            var publication = '';
            var authorCount = ((summary.result[refs].authors).length);
            var i = 0;
            while (i < authorCount - 1) {
                authors += summary.result[refs].authors[i].name + ', ';
                i++;
            }
            publication = HTMLpublication.replace('%data%', 'http://www.ncbi.nlm.nih.gov/pubmed/' + refs);
            authors += summary.result[refs].lastauthor;
            publication = publication.replace('%authors%', authors);
            publication = publication.replace('%title%', summary.result[refs].title);
            publication = publication.replace('%journal%', summary.result[refs].source);
            publication = publication.replace('%PMID%', summary.result[refs].uid);
            var idCount = ((summary.result[refs].articleids).length);
            var i = 0;
            while (i < idCount - 1) {
                if (summary.result[refs].articleids[i].idtype == "doi") {
                    publication = publication.replace('%DOI%', summary.result[refs].articleids[i].value);
                    publication = publication.replace('%DOIadd%', 'https://doi.org/' + summary.result[refs].articleids[i].value);
                }
                i++;
            }
            //Alter formatting if article is In Press
            if (summary.result[refs].volume !== '') {
                publication = publication.replace('%volume%', ' ' + summary.result[refs].volume);
                if (summary.result[refs].issue !== '') {
                    publication = publication.replace('%issue%', ' (' + summary.result[refs].issue + ')');
                } else { 
                    publication = publication.replace('%issue%','');
                }
                if (summary.result[refs].pages !== '') {
                    var str = summary.result[refs].pages + '';
                    if (str.includes('-')) {
                        const pp = str.split('-'); 
                        const len0 = pp[0].length;
                        const len1 = pp[1].length;
                        if (len0 > len1) {
                            var addend = pp[0].substring(0,len0-len1);
                        } else { 
                            var addend = '';
                        } 
                        var nstr = pp[0] + '-' + addend + pp[1];
                    } else {
                        var nstr = str;
                    } 
                    publication = publication.replace('%pages%', ', ' + nstr + '. ');
                } else { 
                    publication = publication.replace('%pages%','. ');
                }
                var date = summary.result[refs].pubdate.slice(0, 4);
                publication = publication.replace('%date%', date + '');
            } else {
                publication = publication.replace('%volume%', ' In Press');
                publication = publication.replace('%issue%', '.');
                publication = publication.replace('%pages%', '');
                publication = publication.replace('%date%', '');
            }
            publicationList = publication + publicationList;
        }
    }
    return (publicationList);
} 

</script>

<p id="demo"></p>
