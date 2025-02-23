---
icon: fas fa-file-alt
order: 5
title: Landscapes


---


<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>

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
