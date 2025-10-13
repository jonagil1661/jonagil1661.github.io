---
layout: single
title: "About Me"
permalink: /about/
author_profile: true
---

<style>
.about-nav {
  position: fixed;
  left: 20px;
  top: 50%;
  transform: translateY(-50%);
  background: #f8f9fa;
  border: 1px solid #dee2e6;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  z-index: 1000;
  min-width: 200px;
}

.about-nav h4 {
  margin-top: 0;
  color: #495057;
  font-size: 16px;
  border-bottom: 1px solid #dee2e6;
  padding-bottom: 10px;
}

.about-nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.about-nav li {
  margin: 8px 0;
}

.about-nav a {
  color: #007bff;
  text-decoration: none;
  font-size: 14px;
  padding: 5px 8px;
  border-radius: 4px;
  transition: background-color 0.2s;
}

.about-nav a:hover {
  background-color: #e9ecef;
  text-decoration: none;
}

@media (max-width: 768px) {
  .about-nav {
    position: static;
    transform: none;
    margin-bottom: 30px;
    width: 100%;
  }
}

.profile-image {
  max-width: 300px;
  width: 100%;
  height: auto;
  display: block;
  margin: 20px 0;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.image-carousel {
  position: relative;
  max-width: 600px;
  width: 100%;
  margin: 20px auto;
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  background-color: #f8f9fa;
}

.carousel-container {
  display: flex;
  transition: transform 0.5s ease-in-out;
  align-items: center;
}

.carousel-image {
  width: 100%;
  min-width: 100%;
  max-width: 100%;
  height: auto;
  max-height: 600px;
  display: block;
  flex-shrink: 0;
  object-fit: contain;
  background-color: #f8f9fa;
}

.carousel-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0,0,0,0.7);
  color: white;
  border: none;
  padding: 15px 20px;
  cursor: pointer;
  font-size: 18px;
  border-radius: 50%;
  transition: background 0.3s;
  z-index: 10;
}

.carousel-nav:hover {
  background: rgba(0,0,0,0.9);
}

.carousel-prev {
  left: 10px;
}

.carousel-next {
  right: 10px;
}

.carousel-indicators {
  text-align: center;
  margin-top: 15px;
}

.indicator {
  display: inline-block;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #ccc;
  margin: 0 5px;
  cursor: pointer;
  transition: background 0.3s;
}

.indicator.active {
  background: #007bff;
}

.carousel-caption {
  text-align: center;
  margin-top: 10px;
  font-weight: bold;
  color: #495057;
}
</style>

<script>
// Traveling Carousel Functions
let slideIndexTraveling = 1;
const captionsTraveling = ['Germany 2024', 'Zermatt, Switzerland 2025', 'Grindelwald, Switzerland 2025'];

function changeSlideTraveling(n) {
  showSlideTraveling(slideIndexTraveling += n);
}

function currentSlideTraveling(n) {
  showSlideTraveling(slideIndexTraveling = n);
}

function showSlideTraveling(n) {
  const carousel = document.getElementById('carousel-traveling');
  const dots = document.querySelectorAll('#traveling .indicator');
  const caption = document.getElementById('caption-traveling');
  
  if (n > captionsTraveling.length) { slideIndexTraveling = 1; }
  if (n < 1) { slideIndexTraveling = captionsTraveling.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexTraveling - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexTraveling - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsTraveling[slideIndexTraveling - 1];
}

// Initialize traveling carousel on page load
document.addEventListener('DOMContentLoaded', function() {
  showSlideTraveling(1);
  
  // Debug: Check if images are loading
  const travelingImages = document.querySelectorAll('#carousel-traveling .carousel-image');
  console.log('Found', travelingImages.length, 'traveling images');
  travelingImages.forEach((img, index) => {
    console.log(`Image ${index + 1}:`, img.src);
    img.onload = () => console.log(`✓ Image ${index + 1} loaded successfully`);
    img.onerror = () => console.log(`✗ Image ${index + 1} failed to load:`, img.src);
  });
});

// Auto-advance Traveling carousel (optional)
setInterval(() => {
  changeSlideTraveling(1);
}, 5000);

// Exercise Carousel Functions
let slideIndexExercise = 1;
const captionsExercise = ['UGA Fall 2024 Tournament', 'Emory Spring 2025 Tournament', '2025 Atlanta Korean Hypersmash Tournament', 'Badminton'];

function changeSlideExercise(n) {
  showSlideExercise(slideIndexExercise += n);
}

function currentSlideExercise(n) {
  showSlideExercise(slideIndexExercise = n);
}

function showSlideExercise(n) {
  const carousel = document.getElementById('carousel-exercise');
  const dots = document.querySelectorAll('#exercise .indicator');
  const caption = document.getElementById('caption-exercise');
  
  if (n > captionsExercise.length) { slideIndexExercise = 1; }
  if (n < 1) { slideIndexExercise = captionsExercise.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexExercise - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexExercise - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsExercise[slideIndexExercise - 1];
}

// Initialize exercise carousel on page load
document.addEventListener('DOMContentLoaded', function() {
  showSlideExercise(1);
});

// Auto-advance Exercise carousel (optional)
setInterval(() => {
  changeSlideExercise(1);
}, 5000);
</script>

<div class="about-nav">
  <h4>About Me</h4>
  <ul>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#hobbies">Hobbies</a></li>
  </ul>
</div>


<img src="/assets/images/jonathan/me.png" alt="jonathan" class="profile-image">

jonathangil@gatech.edu
770-595-7773
<a href="https://github.com/jonagil1661/">GitHub</a>
<a href="https://https://www.linkedin.com/in/jonagil1661/">LinkedIn</a>


<h1 id="introduction">Introduction</h1>

Howdy! My name is Jonathan Gil, and I'm a third year CS major at Georgia Tech! My Concentrations/Treads are in Information-Internetwork and Intelligence. 



<h1 id="skills">Skills</h1>

| Programming Languages | Frameworks | Technologies |
|----------------------|------------|--------------|
| C/C++ | Agile | IntelliJ |
| Python | Flutter | VS Code |
| Java | .NET 6 | Git/GitHub |
| C# | | Firebase |
| SQL | | Android Studio |
| Dart | | CoLab |
| JavaScript | | Docker |
| HTML/CSS | | Postman |
| XML | | Eclipse |
| PHP | | |
| ROS2 | | |

<h1 id="hobbies">Hobbies</h1>
<div class="hobbies" id="traveling">
  <h2>Traveling</h2>
  <p>I love traveling to different countries and exploring new cultures! </p>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideTraveling(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideTraveling(1)">›</button>
    
    <div class="carousel-container" id="carousel-traveling">
      <img src="/assets/images/jonathan/castle.png" alt="Germany" class="carousel-image">
      <img src="/assets/images/jonathan/mountain.png" alt="Zermatt, Switzerland 2025" class="carousel-image">
      <img src="/assets/images/jonathan/switzerland.png" alt="Switzerland" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-traveling">Germany 2024</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideTraveling(1)"></span>
      <span class="indicator" onclick="currentSlideTraveling(2)"></span>
      <span class="indicator" onclick="currentSlideTraveling(3)"></span>
    </div>
  </div>
</div>

<div class="hobbies" id="exercise">
  <h2>Exercising</h2>
  <p>I love to exercise, weightlift, and play sports! </p>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideExercise(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideExercise(1)">›</button>
    
    <div class="carousel-container" id="carousel-exercise">
      <img src="/assets/images/jonathan/uga.png" alt="UGA Fall 2024 Tournament" class="carousel-image">
      
      <img src="/assets/images/jonathan/emory2.png" alt="Emory Spring 2025 Tournament" class="carousel-image">
      <img src="/assets/images/jonathan/tournament.png" alt="2025 Atlanta Korean Hypersmash Tournament" class="carousel-image">
      <img src="/assets/images/jonathan/badminton.png" alt="Badminton" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-exercise">UGA Fall 2024 Tournament</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideExercise(1)"></span>
      <span class="indicator" onclick="currentSlideExercise(2)"></span>
      <span class="indicator" onclick="currentSlideExercise(3)"></span>
      <span class="indicator" onclick="currentSlideExercise(4)"></span>
    </div>
  </div>
</div>
