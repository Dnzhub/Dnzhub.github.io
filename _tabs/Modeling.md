---
icon: fas fa-tags
order: 3
title: Modeling
---






<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  margin: 0;
}

* {
 
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
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
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
  width: 16.66%;
}

/* Add a transparency effect for thumnbail images */
.demo {
  opacity: 0.6;
}

.active,
.demo:hover {
  opacity: 1;
}

.site-title
{
    font-family: inherit;
    font-weight: 900;
    font-size: 1.75rem;
    line-height: 1.2;
    letter-spacing: .25px;
    margin-top: 1.25rem;
    margin-bottom: .5rem;
    width: fit-content;
    color: var(--site-title-color);
}
.site-subtitle{
  font-size: 95%;
    color: var(--site-subtitle-color);
    margin-top: .25rem;
    word-spacing: 1px;
    -webkit-user-select: none;
}
</style>
<body>


<div class="container">
  <div class="mySlides">
    <img src="/assets/images/Cleaver.webp" style="width:100%" alt="cleaver">
  </div>

  <div class="mySlides">
    <img src="/assets/images/Gorehowl.png" style="width:100%" alt="axe">
  </div>

  <div class="mySlides">
    <img src="/assets/images/Horn.webp" style="width:100%" alt="horn">
  </div>
    
  <div class="mySlides">
    <img src="/assets/images/Building.webp" style="width:100%" alt="building">
  </div>

  <div class="mySlides">
    <img src="/assets/images/Imp.webp" style="width:100%" alt="imp">
  </div>
    
  <div class="mySlides">
    <img src="/assets/images/Orc.webp" style="width:100%" alt="orc">
  </div>
  <div class="mySlides">
    <img src="/assets/images/Room.webp" style="width:100%" alt="room">
  </div>
  <div class="mySlides">
    <img src="/assets/images/mechaRobot.webp" style="width:100%" alt="robot">
  </div>
    
  <span class="prev" onclick="plusSlides(-1)">❮</span>
  <span class="next" onclick="plusSlides(1)">❯</span>



  <div class="row">
    <div class="column">
      <img class="demo cursor" src="/assets/images/Cleaver.webp" style="width:100%" onclick="currentSlide(1)" alt="cleaver">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Gorehowl.png" style="width:100%" onclick="currentSlide(2)" alt="axe">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Horn.webp" style="width:100%" onclick="currentSlide(3)" alt="horn">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Building.webp" style="width:100%" onclick="currentSlide(4)" alt="building">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Imp.webp" style="width:100%" onclick="currentSlide(5)" alt="imp">
    </div>    
    <div class="column">
      <img class="demo cursor" src="/assets/images/Orc.webp" style="width:100%" onclick="currentSlide(6)" alt="orc">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/Room.webp" style="width:100%" onclick="currentSlide(6)" alt="room">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/mechaRobot.webp" style="width:100%" onclick="currentSlide(6)" alt="mecha">
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
