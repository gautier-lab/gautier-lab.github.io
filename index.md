---
layout: home
---

<script src="{{ base.url | prepend: site.url }}/assets/js/index.js"></script>
<style>

#container {
  position: relative;
  height: 450px;
  overflow: hidden;
  display: block;
  border: 1px solid #000000;
  box-shadow: 5px 10px 5px #888888;
}

#slides {
  position: relative;
  width: 100%;
  height: 100%;
  margin-left:0px; 
}
#slides .slide {
  position: absolute;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  width: 100%;
  height: 100%;
}
#slides .slide .slide-partial {
  position: absolute;
  width: 50%;
  height: 100%;
  overflow: hidden;
  -webkit-transition: -webkit-transform 1s ease-in-out;
  transition: -webkit-transform 1s ease-in-out;
  transition: transform 1s ease-in-out;
  transition: transform 1s ease-in-out, -webkit-transform 1s ease-in-out;
}
#slides .slide .slide-partial img {
  position: absolute;
  z-index: 1;
  width: 100%;
  height: 100%;
  -o-object-fit: cover;
     object-fit: cover;
  -webkit-transition: -webkit-transform 1s ease-in-out;
  transition: -webkit-transform 1s ease-in-out;
  transition: transform 1s ease-in-out;
  transition: transform 1s ease-in-out, -webkit-transform 1s ease-in-out;
}
#slides .slide .slide-left {
  top: 0;
  left: 0;
  -webkit-transform: translateX(-100%);
          transform: translateX(-100%);
}
#slides .slide .slide-left img {
  top: 0;
  right: 0;
  -o-object-position: 100% 50%;
     object-position: 100% 50%;
  -webkit-transform: translateX(50%);
          transform: translateX(50%);
}
#slides .slide .slide-right {
  top: 0;
  right: 0;
  -webkit-transform: translateX(100%);
          transform: translateX(100%);
  -webkit-transition-delay: 0.2s;
          transition-delay: 0.2s;
}
#slides .slide .slide-right img {
  top: 0;
  left: 0;
  -o-object-position: 0% 50%;
     object-position: 0% 50%;
  -webkit-transition-delay: 0.2s;
          transition-delay: 0.2s;
  -webkit-transform: translateX(-50%);
          transform: translateX(-50%);
}
#slides .slide.active .slide-partial, #slides .slide.active .slide-partial img {
  -webkit-transform: translateX(0);
          transform: translateX(0);
}

#slide-select {
  position: absolute;
  bottom: 0px;
  left: -20px;
  z-index: 100;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -ms-flex-pack: distribute;
  justify-content: space-around;
  color: #1d4f91;
  list-style-type: none;
}
#slide-select li {
  position: relative;
  cursor: pointer;
  margin: 0 5px;
}
#slide-select .selector {
  height: 14px;
  width: 14px;
  border: 2px solid #1d4f91;
  border-radius: 50%;
  background-color: transparent;
  -webkit-transition: background-color 1s ease-in-out;
  transition: background-color 1s ease-in-out;
}
#slide-select .selector.current {
  background-color: #1d4f91;
}

</style>

<div>
<div id="container" align="center">
  <ul id="slides">
    <li class="slide">
      <div class="slide-partial slide-left"><img src="/assets/img/home/Fig2-L.jpg"/></div>
      <div class="slide-partial slide-right"><img src="/assets/img/home/Fig2-R.jpg"/></div>
    </li>
    <li class="slide">
      <div class="slide-partial slide-left"><img src="/assets/img/home/Fig3-L.jpg"/></div>
      <div class="slide-partial slide-right"><img src="/assets/img/home/Fig3-R.jpg"/></div>
    </li>
    <li class="slide">
      <div class="slide-partial slide-left"><img src="/assets/img/home/Slide1-L.gif"/></div>
      <div class="slide-partial slide-right"><img src="/assets/img/home/Slide1-R.gif"/></div>
    </li>
    <li class="slide">
      <div class="slide-partial slide-left"><img src="/assets/img/home/Slide2-L.gif"/></div>
      <div class="slide-partial slide-right"><img src="/assets/img/home/Slide2-R.gif"/></div>
    </li>
    <li class="slide">
      <div class="slide-partial slide-left"><img src="/assets/img/home/Slide3-L.gif"/></div>
      <div class="slide-partial slide-right"><img src="/assets/img/home/Slide3-R.gif"/></div>
    </li>
  </ul>
  <ul id="slide-select">
    <li class="selector"></li>
    <li class="selector"></li>
    <li class="selector"></li>
    <li class="selector"></li>
    <li class="selector"></li>
  </ul>
</div>
<div style="height:50px;"></div>
</div>

<h2>Our Research</h2> 
The main objective of our research is to better understand the molecular mechanisms responsible for the maintenance of genome stability. These controls are lost in cancer, which is characterized by genomic instability.