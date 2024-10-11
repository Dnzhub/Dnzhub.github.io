---
icon: fas fa-tags
order: 2
title: Modeling
---


<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  font-family: Arial;
  margin: 0;
}

* {
  box-sizing: border-box;
}

img {
  vertical-align: middle;
}

/* Position the image container (needed to position the left and right arrows) */
.container {
  position: relative;
}

/* Hide the images by default */
.mySlides {
  display: none;
}

/* Add a pointer when hovering over the thumbnail images */
.cursor {
  cursor: pointer;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
   background-color: rgba(0, 0, 0, 0.8);
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 1);
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* Container for image text */
.caption-container {
  text-align: center;
  background-color: #222;
  padding: 2px 16px;
  color: white;
}

.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Six columns side by side */
.column {
  float: left;
  width: 12.50%;
}

/* Add a transparency effect for thumnbail images */
.demo {
  opacity: 0.6;
}

.active,
.demo:hover {
  opacity: 1;
}

</style>
<body>


<div class="container">
  <div class="mySlides">
    <div class="numbertext">1 / 8</div>
    <img src="/assets/images/Room.webp" style="width:100%" alt="Room">
  </div>

  <div class="mySlides">
    <div class="numbertext">2 / 8</div>
    <img src="/assets/images/Imp.webp" style="width:100%" alt="Imp">
  </div>

  <div class="mySlides">
    <div class="numbertext">3 / 8</div>
    <img src="/assets/images/Building.webp" style="width:100%" alt="Building">
  </div>
    
  <div class="mySlides">
    <div class="numbertext">4 / 8</div>
    <img src="/assets/images/Orc.webp" style="width:100%" alt="Orc">
  </div>

  <div class="mySlides">
    <div class="numbertext">5 / 8</div>
    <img src="/assets/images/Gorehowl.png" style="width:100%" alt="Gorehowl">
  </div>
  
  <div class="mySlides">
    <div class="numbertext">6 / 8</div>
    <img src="/assets/images/Cleaver.webp" style="width:100%" alt="Cleaver">
  </div>
   
   <div class="mySlides">
    <div class="numbertext">7 / 8</div>
    <img src="/assets/images/Horn.webp" style="width:100%" alt="Horn">
  </div>
    
   <div class="mySlides">
    <div class="numbertext">8 / 8</div>
    <img src="/assets/images/mechaRobot.webp" style="width:100%" alt="Robot">
  </div>
  
    
  <a class="prev" href="" onclick="plusSlides(-1)">❮</a>
  <a class="next" href="" onclick="plusSlides(1)">❯</a>
  

  <div class="caption-container">
  </div>

  <div class="row">
    <div class="column">
      <img class="demo cursor" src="/assets/images/Room.webp" style="width:100%"   onclick="currentSlide(1)" alt="Room">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Imp.webp" style="width:100%"   onclick="currentSlide(2)" alt="Imp">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Building.webp" style="width:100%" onclick="currentSlide(3)" alt="Building">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Orc.webp" style="width:100%" onclick="currentSlide(4)" alt="Orc">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Gorehowl.png" style="width:100%"  onclick="currentSlide(5)" alt="Gorehowl">
    </div>    
    <div class="column">
      <img class="demo cursor" src="/assets/images/Cleaver.webp" style="width:100%"  onclick="currentSlide(6)" alt="Cleaver">
    </div>    
    <div class="column">
      <img class="demo cursor" src="/assets/images/Horn.webp" style="width:100%"  onclick="currentSlide(7)" alt="Horn">
    </div>      
    <div class="column">
      <img class="demo cursor" src="/assets/images/mechaRobot.webp" style="width:100%"  onclick="currentSlide(8)" alt="Robot">
    </div> 
    
    
  </div>
</div>

<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("demo");
  let captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
</script>
    
</body>
</html>










