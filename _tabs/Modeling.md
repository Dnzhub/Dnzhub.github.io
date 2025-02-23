---
icon: fas fa-tags
order: 3
title: Modeling
---






<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>


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
