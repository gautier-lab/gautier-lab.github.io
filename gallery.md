---
layout: page
title: Gallery
permalink: /gallery/
---

<style>
div.gallery {
  border: 1px solid #ccc;
}

div.gallery:hover {
  border: 1px solid #777;
}

div.gallery img {
  width: 100%;
  height: auto;
}

.responsive {
  padding: 0 auto;
  float: left;
  width: 24.99999%;
}

.clearfix:after {
  content: "";
  display: table;
  clear: both;
}

.overlay {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1000;
  top: 0;
  left: 0;
  background-color: rgb(0,0,0);
  background-color: rgba(0,0,0, 1);
  overflow-x: hidden;
  transition: 0.5s;
}

.overlay-content {
  position: relative;
  top: 0%;
  width: 100%;
  text-align: center;
  margin-top: 30px;
}

.overlay a {
  padding: 8px;
  text-decoration: none;
  font-size: 36px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.overlay a:hover, .overlay a:focus {
  color: #f1f1f1;
}

.overlay .closebtn {
  position: absolute;
  top: 20px;
  right: 45px;
  font-size: 60px;
  z-index:1000;
}

@media only screen and (max-width: 700px) {
  .responsive {
    width: 49.99999%;
    margin: 6px 0;
  }
  img {
    width: 100%;
  }
  .overlay-content {
    top:15%;
  } 
  .overlay .closebtn {
    position: absolute;
    top: -10px;
    right: 10px;
    font-size: 45px;
  }
}

@media only screen and (max-width: 500px) {
  .responsive {
    width: 100%;
  }
  img {
    width: 100%;
  }
  .overlay-content {
    top:15%;
  } 
  .overlay .closebtn {
    position: absolute;
    top: -10px;
    right: 10px;
    font-size: 45px;
  }
}

</style>


<div id="myNav" class="overlay">
  <a href="javascript:void(0)" class="closebtn" onclick="closeNav()">&times;</a>
  <div class="overlay-content">
    <img src="" width="50%" id="myImg">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/12.png')">
      <img src="/assets/img/gallery/12.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/11.png')">
      <img src="/assets/img/gallery/11.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/10.png')">
      <img src="/assets/img/gallery/10.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/9.png')">
      <img src="/assets/img/gallery/9.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/8.png')">
      <img src="/assets/img/gallery/8.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/7.png')">
      <img src="/assets/img/gallery/7.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/6.png')">
      <img src="/assets/img/gallery/6.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/5.png')">
      <img src="/assets/img/gallery/5.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/4.png')">
      <img src="/assets/img/gallery/4.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/3.png')">
      <img src="/assets/img/gallery/3.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/2.png')">
      <img src="/assets/img/gallery/2.png">
  </div>
</div>

<div class="responsive">
  <div class="gallery" onclick="openNav('/assets/img/gallery/1.png')">
      <img src="/assets/img/gallery/1.png">
  </div>
</div>

<div class="clearfix"></div>

<script>
function openNav(imgFileName) {
  document.getElementById("myNav").style.width = "100%";
  document.getElementById("myImg").src = imgFileName;
}

function closeNav() {
  document.getElementById("myNav").style.width = "0%";
}
</script>
