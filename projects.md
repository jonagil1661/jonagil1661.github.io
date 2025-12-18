---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
---

<style>
.project-nav {
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

.project-nav h4 {
  margin-top: 0;
  color: #495057;
  font-size: 16px;
  border-bottom: 1px solid #dee2e6;
  padding-bottom: 10px;
}

.project-nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.project-nav li {
  margin: 8px 0;
}

.project-nav a {
  color: #007bff;
  text-decoration: none;
  font-size: 14px;
  padding: 5px 8px;
  border-radius: 4px;
  transition: background-color 0.2s;
}

.project-nav a:hover {
  background-color: #e9ecef;
  text-decoration: none;
}

.project {
  margin: 40px 0;
  padding: 30px;
  border: 1px solid #dee2e6;
  border-radius: 8px;
  background: #fff;
}

.project h3 {
  color: #495057;
  margin-bottom: 5px;
}

.project-date {
  color: #6c757d;
  font-size: 14px;
  margin-bottom: 15px;
  font-style: italic;
}

.image-carousel {
  position: relative;
  max-width: 600px;
  margin: 20px auto;
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.carousel-container {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.carousel-image {
  width: auto;
  height: auto;
  max-width: 100%;
  max-height: 600px;
  display: block;
  margin: 0 auto;
  object-fit: contain;
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

@media (max-width: 768px) {
  .project-nav {
    position: static;
    transform: none;
    margin-bottom: 30px;
    width: 100%;
  }
  }
</style>

<script>
let slideIndex = 1;
const captions = ['Login Page', 'Home Page', 'Stringing Request Page', 'Live Progress Page', 'Stringer Page'];

function changeSlide(n) {
  showSlide(slideIndex += n);
}

function currentSlide(n) {
  showSlide(slideIndex = n);
}

function showSlide(n) {
  const carousel = document.getElementById('carousel');
  const dots = document.getElementsByClassName('indicator');
  const caption = document.getElementById('caption');
  
  if (n > captions.length) { slideIndex = 1; }
  if (n < 1) { slideIndex = captions.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndex - 1) * 100}%)`;
  
  // Update indicators
  for (let i = 0; i < dots.length; i++) {
    dots[i].classList.remove('active');
  }
  dots[slideIndex - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captions[slideIndex - 1];
}

// Auto-advance carousel (optional)
setInterval(() => {
  changeSlide(1);
}, 5000);

// BuzzBrief Carousel Functions
let slideIndexBuzzBrief = 1;
const captionsBuzzBrief = ['Login Screen', 'Squad Manager Message', 'Project Debrief Message', 'Flagging Video', 'Project Update Required Message'];

function changeSlideBuzzBrief(n) {
  showSlideBuzzBrief(slideIndexBuzzBrief += n);
}

function currentSlideBuzzBrief(n) {
  showSlideBuzzBrief(slideIndexBuzzBrief = n);
}

function showSlideBuzzBrief(n) {
  const carousel = document.getElementById('carousel-buzzbrief');
  const dots = document.querySelectorAll('#buzzbrief .indicator');
  const caption = document.getElementById('caption-buzzbrief');
  
  if (n > captionsBuzzBrief.length) { slideIndexBuzzBrief = 1; }
  if (n < 1) { slideIndexBuzzBrief = captionsBuzzBrief.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexBuzzBrief - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexBuzzBrief - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsBuzzBrief[slideIndexBuzzBrief - 1];
}

// Auto-advance BuzzBrief carousel (optional)
setInterval(() => {
  changeSlideBuzzBrief(1);
}, 5000);

// DermaScan Carousel Functions
let slideIndexDermaScan = 1;
const captionsDermaScan = ['Home Page', 'Personalized Skincare Tips Page', 'Dermatological Condition Detection Page', 'Find Dermatologists Page', 'Skin Type Quiz'];

function changeSlideDermaScan(n) {
  showSlideDermaScan(slideIndexDermaScan += n);
}

function currentSlideDermaScan(n) {
  showSlideDermaScan(slideIndexDermaScan = n);
}

function showSlideDermaScan(n) {
  const carousel = document.getElementById('carousel-dermascan');
  const dots = document.querySelectorAll('#dermascan .indicator');
  const caption = document.getElementById('caption-dermascan');
  
  if (n > captionsDermaScan.length) { slideIndexDermaScan = 1; }
  if (n < 1) { slideIndexDermaScan = captionsDermaScan.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexDermaScan - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexDermaScan - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsDermaScan[slideIndexDermaScan - 1];
}

// Auto-advance DermaScan carousel (optional)
setInterval(() => {
  changeSlideDermaScan(1);
}, 5000);

// WanderSync Carousel Functions
let slideIndexWanderSync = 1;
const captionsWanderSync = ['Sign Up Page', 'Destinations Page', 'Accommodations Page', 'Dining Reservations Page', 'Invite User Collaboration', 'Logistics Page', 'Note Page', 'Community Page'];

function changeSlideWanderSync(n) {
  showSlideWanderSync(slideIndexWanderSync += n);
}

function currentSlideWanderSync(n) {
  showSlideWanderSync(slideIndexWanderSync = n);
}

function showSlideWanderSync(n) {
  const carousel = document.getElementById('carousel-wandersync');
  const dots = document.querySelectorAll('#wandersync .indicator');
  const caption = document.getElementById('caption-wandersync');
  
  if (n > captionsWanderSync.length) { slideIndexWanderSync = 1; }
  if (n < 1) { slideIndexWanderSync = captionsWanderSync.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexWanderSync - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexWanderSync - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsWanderSync[slideIndexWanderSync - 1];
}

// Auto-advance WanderSync carousel (optional)
setInterval(() => {
  changeSlideWanderSync(1);
}, 5000);

// Fractal Tree Visualizer Carousel Functions
let slideIndexFractal = 1;
const captionsFractal = ['Complex Tree', 'GUI Controls', 'Black Background Tree', 'Thick Branches Tree'];

function changeSlideFractal(n) {
  showSlideFractal(slideIndexFractal += n);
}

function currentSlideFractal(n) {
  showSlideFractal(slideIndexFractal = n);
}

function showSlideFractal(n) {
  const carousel = document.getElementById('carousel-fractal');
  const dots = document.querySelectorAll('#fractaltreevisualizer .indicator');
  const caption = document.getElementById('caption-fractal');
  
  if (n > captionsFractal.length) { slideIndexFractal = 1; }
  if (n < 1) { slideIndexFractal = captionsFractal.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexFractal - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexFractal - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsFractal[slideIndexFractal - 1];
}

// Auto-advance Fractal carousel (optional)
setInterval(() => {
  changeSlideFractal(1);
}, 5000);

// Geography Web Game Carousel Functions
let slideIndexGeography = 1;
const captionsGeography = ['Starting Screen', 'Positive Score', 'Negative Score'];

function changeSlideGeography(n) {
  showSlideGeography(slideIndexGeography += n);
}

function currentSlideGeography(n) {
  showSlideGeography(slideIndexGeography = n);
}

function showSlideGeography(n) {
  const carousel = document.getElementById('carousel-geography');
  const dots = document.querySelectorAll('#geographywebgame .indicator');
  const caption = document.getElementById('caption-geography');
  
  if (n > captionsGeography.length) { slideIndexGeography = 1; }
  if (n < 1) { slideIndexGeography = captionsGeography.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexGeography - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexGeography - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsGeography[slideIndexGeography - 1];
}

// Auto-advance Geography carousel (optional)
setInterval(() => {
  changeSlideGeography(1);
}, 5000);

// Toxic Sentiment Analysis Carousel Functions
let slideIndexToxic = 1;
const captionsToxic = ['ROC Curves', 'ML Model Comparison', 'Inverse Document Frequency'];

function changeSlideToxic(n) {
  showSlideToxic(slideIndexToxic += n);
}

function currentSlideToxic(n) {
  showSlideToxic(slideIndexToxic = n);
}

function showSlideToxic(n) {
  const carousel = document.getElementById('carousel-toxic');
  const dots = document.querySelectorAll('#toxicsentimentanalysis .indicator');
  const caption = document.getElementById('caption-toxic');
  
  if (n > captionsToxic.length) { slideIndexToxic = 1; }
  if (n < 1) { slideIndexToxic = captionsToxic.length; }
  
  // Move the carousel container
  carousel.style.transform = `translateX(-${(slideIndexToxic - 1) * 100}%)`;
  
  // Update indicators
  dots.forEach((dot, i) => {
    dot.classList.remove('active');
  });
  dots[slideIndexToxic - 1].classList.add('active');
  
  // Update caption
  caption.textContent = captionsToxic[slideIndexToxic - 1];
}

// Auto-advance Toxic carousel (optional)
setInterval(() => {
  changeSlideToxic(1);
}, 5000);
</script>

<div class="project-nav">
  <h4>Project Outline</h4>
  <ul>
    <li><a href="#toxicsentimentanalysis">Toxic Sentiment Analysis</a></li>
    <li><a href="#buzzstring">BuzzString</a></li>
    <li><a href="#buzzbrief">BuzzBrief</a></li>
    <li><a href="#dermascan">DermaScan</a></li>
    <li><a href="#wandersync">WanderSync</a></li>
    <li><a href="#fractaltreevisualizer">Fractal Tree</a></li>
    <li><a href="#geographywebgame">Geography Game</a></li>
  </ul>
</div>









<div class="project" id="toxicsentimentanalysis">
  <h2>Toxic Sentiment Analysis</h2>
  <p class="project-date">August 2025 - December 2025</p>
  <p>A machine learning project that analyzes in-game chat logs to identify and understand toxic behavior, while comparing three different machine learning methods to determine the best performer for toxicity detection. Using the CONDA dataset, this project performs a comparative analysis of toxic language in competitive online environments with the goal to contribute to the development of methods that can help minimize toxicity and make online gaming a better experience for everyone.</p>
  <p><strong>Tech:</strong> Python, Machine Learning, Seaborn, Pandas, Scikit-learn</p>
  <a href="https://github.com/jonagil1661/toxic-sentiment-analysis" target="_blank">Code</a> | 
  <a href="/assets/files/report.pdf" target="_blank">Report</a> |
  <a href="https://docs.google.com/presentation/d/1Kql406maa9X99TiWHtiPk6VBWCbFO1tV_2c5xzMrpZE/edit?usp=sharing" target="_blank">Presentation</a>

  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideToxic(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideToxic(1)">›</button>
    
    <div class="carousel-container" id="carousel-toxic">
    <img src="/assets/images/toxicsentimentanalysis/roc_curves.png" alt="ROC Curves" class="carousel-image">
      <img src="/assets/images/toxicsentimentanalysis/model_comparison.png" alt="ML Model Comparison" class="carousel-image">
      <img src="/assets/images/toxicsentimentanalysis/idf.png" alt="Inverse Document Frequency" class="carousel-image">

    </div>
    
    <div class="carousel-caption" id="caption-toxic">ROC Curves</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideToxic(1)"></span>
      <span class="indicator" onclick="currentSlideToxic(2)"></span>
      <span class="indicator" onclick="currentSlideToxic(3)"></span>

    </div>
  </div>
  
</div>

<div class="project" id="buzzstring">
  <h2>BuzzString</h2>
  <p class="project-date">August 2025 - October 2025</p>
  <p>A web app that conveniently allows Georgia Tech Badminton Club members to submit racket stringing requests online. Features include Google Sign-In authentication, real-time stringing request tracking, and a streamlined interface for managing service status updates.</p>
  <p><strong>Tech:</strong> Flutter, Dart, Firebase, Google OAuth</p>
  <a href="https://buzzstring.org" target="_blank">Live Website</a> | 
  <a href="https://github.com/jonagil1661/BuzzString" target="_blank">Code</a>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlide(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlide(1)">›</button>
    
    <div class="carousel-container" id="carousel">
      <img src="/assets/images/buzzstring/login.png" alt="Login Page" class="carousel-image">
      <img src="/assets/images/buzzstring/home.png" alt="Home Page" class="carousel-image">
      <img src="/assets/images/buzzstring/request.png" alt="Stringing Request Page" class="carousel-image">
      <img src="/assets/images/buzzstring/progress.png" alt="Live Progress Page" class="carousel-image">
      <img src="/assets/images/buzzstring/stringer.png" alt="Stringer Page" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption">Login Page</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlide(1)"></span>
      <span class="indicator" onclick="currentSlide(2)"></span>
      <span class="indicator" onclick="currentSlide(3)"></span>
      <span class="indicator" onclick="currentSlide(4)"></span>
      <span class="indicator" onclick="currentSlide(5)"></span>
    </div>
  </div>
</div>








<div class="project" id="buzzbrief">
  <h2>BuzzBrief</h2>
  <p class="project-date">September 2025</p>
  <p>A mobile app that transforms Gmail inboxes into an entertaining TikTok-style video feed. It securely connects via Google OAuth, uses AI to summarize emails into short scripts, and generates engaging video clips with narration, visuals, and subtitles–making daily email review fast, interactive, and fun. Built in a team of three during the HackGT 12 hackathon.</p>
  <p><strong>Tech:</strong> React Native, Expo Go, Supabase, FastAPI, Python, FFmpeg, OpenAI APIs, GmailAPI</p>
  <a href="https://devpost.com/software/buzz-brief?ref_content=my-projects-tab&ref_feature=my_projects" target="_blank">Devpost</a> | 
  <a href="https://youtube.com/shorts/oFaW2A6t9D0?si=toXqmR_C9-8pnrmo" target="_blank">Demo</a> | 
  <a href="https://github.com/buzz-brief/buzz-brief" target="_blank">Code</a>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideBuzzBrief(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideBuzzBrief(1)">›</button>
    
    <div class="carousel-container" id="carousel-buzzbrief">
      <img src="/assets/images/buzzbrief/login.png" alt="Login Screen" class="carousel-image">
      <img src="/assets/images/buzzbrief/cat.png" alt="Squad Manager Message" class="carousel-image">
      <img src="/assets/images/buzzbrief/fish.png" alt="Project Debrief Message" class="carousel-image">
      <img src="/assets/images/buzzbrief/baby.png" alt="Flagged a Video" class="carousel-image">
      <img src="/assets/images/buzzbrief/steve.png" alt="Project Update Required Message" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-buzzbrief">Login Screen</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideBuzzBrief(1)"></span>
      <span class="indicator" onclick="currentSlideBuzzBrief(2)"></span>
      <span class="indicator" onclick="currentSlideBuzzBrief(3)"></span>
      <span class="indicator" onclick="currentSlideBuzzBrief(4)"></span>
      <span class="indicator" onclick="currentSlideBuzzBrief(5)"></span>
    </div>
  </div>
</div>










<div class="project" id="dermascan">
  <h2>DermaScan</h2>
  <p class="project-date">February 2025</p>
  <p>An interactive web app that lets users upload skin images for AI-powered cancer risk detection and condition-based recommendations. Built with a Streamlit interface for real-time predictions, it also includes a clinic locator to connect users with nearby dermatologists. Developed in a 4-person team during the UGAHacks 10 hackathon.</p>
  <p><strong>Tech:</strong> Python, TensorFlow, Streamlit, Google Maps API, Deep Learning</p>
  <a href="https://devpost.com/software/dermascan-a0i8c7" target="_blank">Devpost</a> | 
  <a href="https://devpost.com/software/dermascan-a0i8c7" target="_blank">Live Website</a> | 
  <a href="https://github.com/n-m-gitrepos/DermaScan" target="_blank">Code</a>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideDermaScan(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideDermaScan(1)">›</button>
    
    <div class="carousel-container" id="carousel-dermascan">
      <img src="/assets/images/dermascan/home.png" alt="Home Page" class="carousel-image">
      <img src="/assets/images/dermascan/advice.png" alt="Personalized Skincare Tips Page" class="carousel-image">
      <img src="/assets/images/dermascan/detection.png" alt="Dermatological Condition Detection Page" class="carousel-image">
      <img src="/assets/images/dermascan/find.png" alt="Find Dermatologists Page" class="carousel-image">
      <img src="/assets/images/dermascan/quiz.png" alt="Skin Type Quiz" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-dermascan">Home Page</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideDermaScan(1)"></span>
      <span class="indicator" onclick="currentSlideDermaScan(2)"></span>
      <span class="indicator" onclick="currentSlideDermaScan(3)"></span>
      <span class="indicator" onclick="currentSlideDermaScan(4)"></span>
      <span class="indicator" onclick="currentSlideDermaScan(5)"></span>
    </div>
  </div>
</div>





<div class="project" id="wandersync">
  <h2>WanderSync Navigation App</h2>
  <p class="project-date">August 2024 - November 2024</p>
  <p>An Android app for real-time location tracking and user collaboration, built with MVVM architecture and Firebase for scalability. Features include secure authentication and dynamic user invitations for instant shared navigation. Developed in an Agile team.</p>
  <p><strong>Tech:</strong> Java, Firebase, MVVM, Android Studio</p>
  <a href="https://n-m-gitrepos.github.io/" target="_blank">Website</a> | 
  <a href="https://github.com/n-m-gitrepos/CS2340C_Team50" target="_blank">Code</a>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideWanderSync(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideWanderSync(1)">›</button>
    
    <div class="carousel-container" id="carousel-wandersync">
      <img src="/assets/images/wandersync/signup.png" alt="Sign Up Page" class="carousel-image">
      <img src="/assets/images/wandersync/destination.png" alt="Destinations Page" class="carousel-image">
      <img src="/assets/images/wandersync/accomodations.png" alt="Accommodations Page" class="carousel-image">
      <img src="/assets/images/wandersync/reservations.png" alt="Dining Reservations Page" class="carousel-image">
      <img src="/assets/images/wandersync/invite.png" alt="Invite User Collaboration" class="carousel-image">
      <img src="/assets/images/wandersync/logistics.png" alt="Logistics Page" class="carousel-image">
      <img src="/assets/images/wandersync/note.png" alt="Note Page" class="carousel-image">
      <img src="/assets/images/wandersync/community.png" alt="Community Page" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-wandersync">Sign Up Page</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideWanderSync(1)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(2)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(3)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(4)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(5)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(6)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(7)"></span>
      <span class="indicator" onclick="currentSlideWanderSync(8)"></span>
    </div>
  </div>
</div>









<div class="project" id="fractaltreevisualizer">
  <h2>Fractal Tree Visualizer</h2>
  <p class="project-date">March 2024</p>
  <p>An interactive Java application built with Swing to visualize fractal trees. Includes sliders and controls for dynamic adjustments, demonstrating recursive stack behavior with a custom linked list stack to modify branch thickness, layers, and angles.</p>
  <p><strong>Tech:</strong> Java, Swing, Maven, Data Structures</p>
  <a href="https://github.com/jonagil1661/FractalTreeApp" target="_blank">Code</a>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideFractal(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideFractal(1)">›</button>
    
    <div class="carousel-container" id="carousel-fractal">
      <img src="/assets/images/fractaltreevisualizer/complex.png" alt="Complex Tree" class="carousel-image">
      <img src="/assets/images/fractaltreevisualizer/gui.png" alt="GUI Controls" class="carousel-image">
      <img src="/assets/images/fractaltreevisualizer/black.png" alt="Black Background Tree" class="carousel-image">
      <img src="/assets/images/fractaltreevisualizer/thick.png" alt="Thick Branches Tree" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-fractal">Complex Tree</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideFractal(1)"></span>
      <span class="indicator" onclick="currentSlideFractal(2)"></span>
      <span class="indicator" onclick="currentSlideFractal(3)"></span>
      <span class="indicator" onclick="currentSlideFractal(4)"></span>
    </div>
  </div>
</div>









<div class="project" id="geographywebgame">
  <h2>Geography Web Game</h2>
  <p class="project-date">February 2024 - March 2024</p>
  <p>A web app built in a two-person team that quizzes users on country flags, tracks scores, and helps improve geographic knowledge. Integrated the RestCountries API to fetch flag images and names, supporting gameplay with both official and common country names via a dynamic JavaScript array.</p>
  <p><strong>Tech:</strong> HTML, CSS, Javascript, RestCountries API</p>
  <a href="https://github.com/jonagil1661/GeographyGame" target="_blank">Code</a>
  <br>
  
  <div class="image-carousel">
    <button class="carousel-nav carousel-prev" onclick="changeSlideGeography(-1)">‹</button>
    <button class="carousel-nav carousel-next" onclick="changeSlideGeography(1)">›</button>
    
    <div class="carousel-container" id="carousel-geography">
      <img src="/assets/images/geographywebgame/usa.png" alt="Starting Screen" class="carousel-image">
      <img src="/assets/images/geographywebgame/kenya.png" alt="Positive Score" class="carousel-image">
      <img src="/assets/images/geographywebgame/gambia.png" alt="Negative Score" class="carousel-image">
    </div>
    
    <div class="carousel-caption" id="caption-geography">Starting Screen</div>
    <div class="carousel-indicators">
      <span class="indicator active" onclick="currentSlideGeography(1)"></span>
      <span class="indicator" onclick="currentSlideGeography(2)"></span>
      <span class="indicator" onclick="currentSlideGeography(3)"></span>
    </div>
  </div>
</div>