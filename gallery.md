---
layout: page
title: Gallery
permalink: /gallery/
---

<style>

.card {
  position: relative;
  
  width: 100%;
  height: 739px;
  overflow: hidden;

  border-radius: 5px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
}


.card::after {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  z-index: 900;

  display: block;
  width: 100%;
  height: 100%;

  background-color: rgba(0,0,0, 0.2);
}

.card_part {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 12;

  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
  
  transform: translateX(100vh);
  background-image: url(/assets/img/gallery/12.png);
  background-size: cover;
  background-repeat: no-repeat;
  
  animation: opaqTransition 105s cubic-bezier(0, 0, 0, 0.97) infinite;
}


.card_part.card_part-two {
  z-index: 11;
  background-image: url(/assets/img/gallery/11.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 7s;
}

.card_part.card_part-three {
  z-index: 10;
  background-image: url(/assets/img/gallery/10.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 14s;
}

.card_part.card_part-four {
  z-index: 9;
  background-image: url(/assets/img/gallery/9.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 21s;
}
.card_part.card_part-five {
  z-index: 8;
  background-image: url(/assets/img/gallery/8.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 28s;
}
.card_part.card_part-six {
  z-index: 7;
  background-image: url(/assets/img/gallery/7.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 35s;
}
.card_part.card_part-seven {
  z-index: 6;
  background-image: url(/assets/img/gallery/6.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 42s;
}
.card_part.card_part-eight {
  z-index: 5;
  background-image: url(/assets/img/gallery/5.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 49s;
}

.card_part.card_part-nine {
  z-index: 4;
  background-image: url(/assets/img/gallery/4.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 56s;
}
.card_part.card_part-ten {
  z-index: 3;
  background-image: url(/assets/img/gallery/3.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 63s;
}
.card_part.card_part-eleven {
  z-index: 2;
  background-image: url(/assets/img/gallery/2.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 70s;
}
.card_part.card_part-twelve {
  z-index: 1;
  background-image: url(/assets/img/gallery/1.png);
  background-size: cover;
  background-repeat: no-repeat;
  animation-delay: 77s;
}

@keyframes opaqTransition {
  3% { transform: translateX( 0 ); }
  25% { transform: translateX( 0 ); }
  28% { transform: translateX( -100vh ); }
  100% { transform: translateX( -100vh ); }
}

</style>

<div class="card">
  
  <div class="card_part card_part"></div>
  <div class="card_part card_part-two"></div>
  <div class="card_part card_part-three"></div>
  <div class="card_part card_part-four"></div>
  <div class="card_part card_part-five"></div>
  <div class="card_part card_part-six"></div>
  <div class="card_part card_part-seven"></div>
  <div class="card_part card_part-eight"></div>
  <div class="card_part card_part-nine"></div>
  <div class="card_part card_part-ten"></div>
  <div class="card_part card_part-eleven"></div>
  <div class="card_part card_part-twelve"></div>
</div>

