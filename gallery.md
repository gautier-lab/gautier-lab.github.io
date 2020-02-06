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
  text-align:center;
  background: rgba(0,0,0,1);
  opacity: 0;
  -webkit-transition: opacity .5s ease-in-out;
  -moz-transition: opacity .5s ease-in-out;
  -o-transition: opacity .5s ease-in-out;
  transition: opacity .5s ease-in-out;
  overflow: hidden;
}

.lightbox-target img {
  margin: auto;
  position: relative;
  right:0;
  bottom: 0;
  max-height: 0%;
  max-width: 0%;
  box-shadow: 0px 0px 8px rgba(0,0,0,.3);
  box-sizing: border-box;
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

</style>

<div class="responsive-m"><img src="/assets/img/gallery/12.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/11.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/10.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/9.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/8.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/7.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/6.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/5.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/4.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/3.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/2.png"></div>
<div class="responsive-m"><img src="/assets/img/gallery/1.png"></div>

<a class="responsive" href="#12"><img src="/assets/img/gallery/12.png"></a>
<a class="responsive" href="#11"><img src="/assets/img/gallery/11.png"></a>
<a class="responsive" href="#10"><img src="/assets/img/gallery/10.png"></a>
<a class="responsive" href="#9"><img src="/assets/img/gallery/9.png"></a>
<a class="responsive" href="#8"><img src="/assets/img/gallery/8.png"></a>
<a class="responsive" href="#7"><img src="/assets/img/gallery/7.png"></a>
<a class="responsive" href="#6"><img src="/assets/img/gallery/6.png"></a>
<a class="responsive" href="#5"><img src="/assets/img/gallery/5.png"></a>
<a class="responsive" href="#4"><img src="/assets/img/gallery/4.png"></a>
<a class="responsive" href="#3"><img src="/assets/img/gallery/3.png"></a>
<a class="responsive" href="#2"><img src="/assets/img/gallery/2.png"></a>
<a class="responsive" href="#1"><img src="/assets/img/gallery/1.png"></a>

<div class="lightbox-target" id="12">
   <img src="/assets/img/gallery/12.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="11">
   <img src="/assets/img/gallery/11.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="10">
   <img src="/assets/img/gallery/10.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="9">
   <img src="/assets/img/gallery/9.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="8">
   <img src="/assets/img/gallery/8.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="7">
   <img src="/assets/img/gallery/7.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="6">
   <img src="/assets/img/gallery/6.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="5">
   <img src="/assets/img/gallery/5.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="4">
   <img src="/assets/img/gallery/4.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="3">
   <img src="/assets/img/gallery/3.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="2">
   <img src="/assets/img/gallery/2.png"/>
   <a class="lightbox-close" href="#"></a>
</div>
<div class="lightbox-target" id="1">
   <img src="/assets/img/gallery/1.png"/>
   <a class="lightbox-close" href="#"></a>
</div>

