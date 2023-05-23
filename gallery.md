---
layout: page
title: Gallery
permalink: /gallery/
---

<style>

.responsive {
  padding: 0 auto;
  border: 1px solid black;
  float: left;
  width: 24%;
  visibility:visible;
}
.responsive:hover {
  border: 1px solid white; 
}

.responsive-m {
  padding: 0 auto;
  float: left;
  border: 0px;
  width:100%;
  display:none;
}

@media (max-width:800px) {
  .responsive {
    display:none;
  }
  .responsive-m {
    display:inline;
  } 
}

a.lightbox img {
  height: 150px;
  border: 3px solid white;
  box-shadow: 0px 0px 8px rgba(0,0,0,.3);
  margin: 94px 20px 20px 20px;
}


.lightbox-target {
  z-index:999999;
  position:absolute;
  width:100%;
  left:0;
  top:0;
  text-align:center;
  background: rgba(0,0,0,1);
  opacity: 1;
  -webkit-transition: opacity .5s ease-in-out;
  -moz-transition: opacity .5s ease-in-out;
  -o-transition: opacity .5s ease-in-out;
  transition: opacity .5s ease-in-out;
}

.lightbox-target img {
  margin: 0 auto;
  display:block;
  position: absolute;
  top:0;
  left:0;
  right:0;
  bottom: 0;
  max-height: 0%;
  max-width: 0%;
  box-shadow: 0px 0px 8px rgba(0,0,0,.3);
  box-sizing: border-box;
  overflow:hidden;
  -webkit-transition: .5s ease-in-out;
  -moz-transition: .5s ease-in-out;
  -o-transition: .5s ease-in-out;
  transition: .5s ease-in-out;
}

a.lightbox-close {
  display: block;
  width:50px;
  height:50px;
  box-sizing: border-box;
  color: black;
  text-decoration: none;
  position: absolute;
  top: -80px;
  right: 0;
  -webkit-transition: .5s ease-in-out;
  -moz-transition: .5s ease-in-out;
  -o-transition: .5s ease-in-out;
  transition: .5s ease-in-out;
}

a.lightbox-close:before {
  content: "";
  display: block;
  height: 30px;
  width: 1px;
  background: white;
  position: absolute;
  left: 26px;
  top:10px;
  -webkit-transform:rotate(45deg);
  -moz-transform:rotate(45deg);
  -o-transform:rotate(45deg);
  transform:rotate(45deg);
}

a.lightbox-close:after {
  content: "";
  display: block;
  height: 30px;
  width: 1px;
  background: white;
  position: absolute;
  left: 26px;
  top:10px;
  -webkit-transform:rotate(-45deg);
  -moz-transform:rotate(-45deg);
  -o-transform:rotate(-45deg);
  transform:rotate(-45deg);
}

.lightbox-target:target {
  opacity: 1;
  display:block;
  height:200vh;
  top: 0;
  bottom: 0;
}

.lightbox-target:target img {
  max-height: 100%;
  max-width: 100%;
}

.lightbox-target:target a.lightbox-close {
  top: 0px;
}


table {
  width:100%;
  margin:auto;
  display:inline-table;
}
td,th {
  text-align:center;
}
.table-container {
  text-align:center;
}
.spacer {
  height:0px;
}
@media (min-width:600px) {
  table {
    width:30%;
  }
  .spacer {
    height:10px; 
  }
}

</style>

<div class="table-container">
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/13.png');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/12.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/11.jpg');background-size:cover;background-position:center"></td></tr>
</table>
</div>


<div class="table-container">
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/10.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/9.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/8.jpg');background-size:cover;background-position:center"></td></tr>
</table>
</div>

<div class="table-container">
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/7.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/6.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/5.jpg');background-size:cover;background-position:center"></td></tr>
</table>
</div>

<div class="table-container">
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/4.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/3.jpg');background-size:cover;background-position:center"></td></tr>
</table>
<table>
<tr><td><img style="display:inline-block;height:300px;width:100%;background:url('/assets/img/gallery/2.jpg');background-size:cover;background-position:center"></td></tr>
</table>
</div>

<div class="table-container">
<table>
<tr><td> 

<img src=url"('/assets/img/gallery/1.jpg')"
        onclick="enlargeImg()"
        id="img1" />


</td></tr>
</table>
</div>

