---
layout: single
title: "Experience"
permalink: /experience/
author_profile: true
---

<style>
.experience-nav {
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

.experience-nav h4 {
  margin-top: 0;
  color: #495057;
  font-size: 16px;
  border-bottom: 1px solid #dee2e6;
  padding-bottom: 10px;
}

.experience-nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.experience-nav li {
  margin: 8px 0;
}

.experience-nav a {
  color: #007bff;
  text-decoration: none;
  font-size: 14px;
  padding: 5px 8px;
  border-radius: 4px;
  transition: background-color 0.2s;
}

.experience-nav a:hover {
  background-color: #e9ecef;
  text-decoration: none;
}

.experience {
  margin: 40px 0;
  padding: 30px;
  border: 1px solid #dee2e6;
  border-radius: 8px;
  background: #fff;
}

.experience h2 {
  color: #495057;
  margin-bottom: 5px;
}

.experience-date {
  color: #6c757d;
  font-size: 14px;
  margin-bottom: 15px;
  font-style: italic;
}

.experience ul {
  margin-top: 15px;
}

.experience li {
  margin-bottom: 10px;
  line-height: 1.6;
}

.experience-aad {
  background-image: url('/assets/images/experience/aad.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
}

.experience-aad::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255, 255, 255, 0.75);
  border-radius: 8px;
  z-index: 0;
}

.experience-aad > * {
  position: relative;
  z-index: 1;
}

.experience-robojackets {
  background-image: url('/assets/images/experience/robojackets.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
}

.experience-robojackets::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255, 255, 255, 0.75);
  border-radius: 8px;
  z-index: 0;
}

.experience-robojackets > * {
  position: relative;
  z-index: 1;
}

.experience-roboinvesting {
  background-image: url('/assets/images/toxicsentimentanalysis/stocks.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
}

.experience-roboinvesting::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255, 255, 255, 0.75);
  border-radius: 8px;
  z-index: 0;
}

.experience-roboinvesting > * {
  position: relative;
  z-index: 1;
}

@media (max-width: 768px) {
  .experience-nav {
    position: static;
    transform: none;
    margin-bottom: 30px;
    width: 100%;
  }
}
</style>

<div class="experience-nav">
  <h4>Experience</h4>
  <ul>
    <li><a href="#datascienceclub">Data Science Club</a></li>
    <li><a href="#aad">Automated Algorithm Design</a></li>
    <li><a href="#robojackets">RoboJackets</a></li>
  </ul>
</div>

<div class="experience experience-roboinvesting" id="datascienceclub">
  <h2>RoboInvesting Subteam Member</h2>
  <h3>GT Data Science Club</h3>
  <p class="experience-date">August 2025 – Present</p>
  
  <ul>
    <li>Developed modular backtesting engine to simulate algorithmic trading strategies</li>
    <li>Built AI Persona Signal Engine that aggregates investment signals to determine most reliable signal per stock</li>
    <li>Created flexible experimentation framework to evaluate trading strategies across multiple tickers</li>
    <li>Enhanced risk-adjusted decision-making, integrating portfolio capital management into strategy loop</li>
    <li>Implemented trading mechanics to control drawdowns</li>
    
  </ul>
</div>

<div class="experience experience-aad" id="aad">
  <h2>Undergraduate Research Assistant</h2>
  <h3>GT Automated Algorithm Design</h3>
  <p class="experience-date">January 2025 – Present</p>
  <a href="@https://vip.gatech.edu/teams/entry/1312/ ">VIP Team Page</a>
  
  <ul>
    <li>Minimized error by 20% and optimized model complexity by implementing genetic programming and multi-objective optimization, including symbolic regression and Pareto front analysis, by utilizing the DEAP Python library.</li>
    <li>Achieved greater accuracy than traditional ML models by leveraging NSGA-II selection and optimizing 92 generations, enabled by automating the machine learning algorithm design on the Titanic dataset.</li>
    <li>Facilitated 5 Monte Carlo trials to evaluate and score algorithm performance by enabling a local computer to function as a worker process within an evolutionary framework via a server connection through SQL.</li>
  </ul>
</div>

<div class="experience experience-robojackets" id="robojackets">
  <h2>RoboCup Software Subteam Member</h2>
  <h3>GT RoboJackets</h3>
  <p class="experience-date">August 2024 – May 2025</p>
  
  <ul>
    <li>Integrated multi-agent adversarial strategies and enhanced motion planning algorithms for six autonomous soccer robots using C++ and ROS2 in an Agile team.</li>
    <li>Improved decision-making efficiency in the stack by optimizing robotic strategy through dynamically adjusting behavior in simulation using rqt.</li>
  </ul>
</div>
