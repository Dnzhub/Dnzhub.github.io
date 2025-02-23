---
icon: fas fa-file-alt
order: 5
title: Landscapes


---


<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
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
    <img src="/assets/images/DarkForest Concept.webp" style="width:100%" alt="df">
  </div>

  <div class="mySlides">
    <img src="/assets/images/DarkLand.webp" style="width:100%" alt="dl">
  </div>

  <div class="mySlides">
    <img src="/assets/images/DarkLandScape.webp" style="width:100%" alt="dlscape">
  </div>
    
  <div class="mySlides">
    <img src="/assets/images/DarklandSecond.webp" style="width:100%" alt="dl2">
  </div>

  <div class="mySlides">
    <img src="/assets/images/LandScape.webp" style="width:100%" alt="ls">
  </div>
    
    
  <span class="prev" onclick="plusSlides(-1)">❮</span>
  <span class="next" onclick="plusSlides(1)">❯</span>



  <div class="row">
    <div class="column">
      <img class="demo cursor" src="/assets/images/DarkForest Concept.webp" style="width:100%" onclick="currentSlide(1)" alt="df">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/DarkLand.webp" style="width:100%" onclick="currentSlide(2)" alt="dl">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/DarkLandScape.webp" style="width:100%" onclick="currentSlide(3)" alt="dls">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/DarklandSecond.webp" style="width:100%" onclick="currentSlide(4)" alt="dl2">
    </div>
    <div class="column">
      <img class="demo cursor" src="/assets/images/LandScape.webp" style="width:100%" onclick="currentSlide(5)" alt="ls">
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
