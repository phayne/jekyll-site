---
layout: page
title: research
permalink: /research/
description:
---

<style>
.research-intro {
  margin-bottom: 2rem;
  line-height: 1.6;
}

.research-section {
  margin-bottom: 2.5rem;
}

.research-section h2 {
  border-bottom: 2px solid #333;
  padding-bottom: 0.3rem;
  margin-bottom: 1rem;
  font-size: 1.4rem;
}

.research-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
  gap: 1rem;
}

.research-item {
  text-align: center;
}

.research-item a {
  text-decoration: none;
  color: inherit;
  display: block;
}

.research-item a:hover {
  opacity: 0.8;
}

.research-icon {
  width: 80px;
  height: 80px;
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 0.4rem;
  border: 1px solid #ddd;
}

.research-item-label {
  font-size: 0.85rem;
  line-height: 1.3;
}

.mission-category {
  margin-bottom: 1.5rem;
}

.mission-category h3 {
  font-size: 1rem;
  color: #555;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.mission-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem 1.5rem;
  list-style: none;
  padding: 0;
  margin: 0;
}

.mission-list li {
  font-size: 0.9rem;
}

.mission-list a {
  color: #0066cc;
  text-decoration: none;
}

.mission-list a:hover {
  text-decoration: underline;
}

.data-section {
  margin-bottom: 1.5rem;
}

.data-section h3 {
  font-size: 1rem;
  color: #555;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.data-list {
  list-style: disc;
  padding-left: 1.5rem;
  margin: 0;
}

.data-list li {
  font-size: 0.9rem;
  margin-bottom: 0.3rem;
}

.data-list a {
  color: #0066cc;
  text-decoration: none;
}

.data-list a:hover {
  text-decoration: underline;
}

.nested-list {
  list-style: circle;
  padding-left: 1.2rem;
  margin-top: 0.2rem;
}
</style>

<div class="research-intro">
Research in the EPIC group spans a range of planetary bodies, unified by a focus
on ice and volatiles. We use numerical methods to model planetary surfaces and 
atmospheres, making and testing predictions using remote sensing data.
</div>

<!-- PLANETARY BODIES -->
<div class="research-section">
  <h2>Planetary Bodies</h2>
  <div class="research-grid">
    <div class="research-item">
      <a href="{{ site.baseurl }}/projects/10_moon/">
        <img class="research-icon" src="{{ site.baseurl }}/assets/img/research/moon.jpg" alt="Moon"/>
        <div class="research-item-label">Moon</div>
      </a>
    </div>
    <div class="research-item">
      <a href="{{ site.baseurl }}/projects/11_mars/">
        <img class="research-icon" src="{{ site.baseurl }}/assets/img/research/mars.jpg" alt="Mars"/>
        <div class="research-item-label">Mars</div>
      </a>
    </div>
    <div class="research-item">
      <a href="{{ site.baseurl }}/projects/12_satellites/">
        <img class="research-icon" src="{{ site.baseurl }}/assets/img/research/satellites.jpg" alt="Satellites"/>
        <div class="research-item-label">Satellites of the Giant Planets</div>
      </a>
    </div>
    <div class="research-item">
      <a href="{{ site.baseurl }}/projects/13_asteroids/">
        <img class="research-icon" src="{{ site.baseurl }}/assets/img/research/asteroids.jpg" alt="Asteroids"/>
        <div class="research-item-label">Asteroids &amp; Comets</div>
      </a>
    </div>
  </div>
</div>

<!-- MISSIONS -->
<div class="research-section">
  <h2>Missions</h2>
  
  <div class="mission-category">
    <h3>Moon</h3>
    <ul class="mission-list">
      <li><a href="{{ site.baseurl }}/projects/14_missions/#lro">Lunar Reconnaissance Orbiter</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#lunar-flashlight">Lunar Flashlight</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#lunar-vise">CLPS CP-21: Lunar-VISE</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#l-ciris">CLPS CP-22: L-CIRiS</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#l-maps">Lunar Terrain Vehicle: L-MAPS</a></li>
    </ul>
  </div>
  
  <div class="mission-category">
    <h3>Mars</h3>
    <ul class="mission-list">
      <li><a href="{{ site.baseurl }}/projects/14_missions/#mro">Mars Reconnaissance Orbiter</a></li>
    </ul>
  </div>
  
  <div class="mission-category">
    <h3>Asteroids</h3>
    <ul class="mission-list">
      <li><a href="{{ site.baseurl }}/projects/14_missions/#ema">Emirates Mission to the Asteroid Belt</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#janus">Janus</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#dawn">Dawn</a></li>
    </ul>
  </div>
  
  <div class="mission-category">
    <h3>Outer Solar System</h3>
    <ul class="mission-list">
      <li><a href="{{ site.baseurl }}/projects/14_missions/#europa-clipper">Europa Clipper</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#cassini">Cassini</a></li>
      <li><a href="{{ site.baseurl }}/projects/14_missions/#galileo">Galileo</a></li>
    </ul>
  </div>
</div>

<!-- DATASETS AND MODELS -->
<div class="research-section">
  <h2>Datasets and Models</h2>
  
  <div class="data-section">
    <h3>Datasets</h3>
    <ul class="data-list">
      <li><a href="{{ site.baseurl }}/projects/20_diviner-h-parameter/">Diviner H-parameter</a> (thermal inertia)</li>
      <li><a href="{{ site.baseurl }}/projects/21_lamp-water/">LAMP water detections</a></li>
      <li><a href="{{ site.baseurl }}/projects/22_cassini-vims-titan/">Cassini VIMS Titan occultation spectra</a></li>
      <li><a href="{{ site.baseurl }}/projects/23_galileo-nims-europa/">Galileo NIMS Europa hyperspectral images</a></li>
      <li><a href="{{ site.baseurl }}/projects/24_galileo-ppr/">Galileo PPR thermal maps</a></li>
    </ul>
  </div>
  
  <div class="data-section">
    <h3>Models</h3>
    <ul class="data-list">
      <li>Thermophysical models:
        <ul class="nested-list">
          <li><a href="https://github.com/phayne/heat1d" target="_blank">heat1d</a></li>
          <li><a href="https://github.com/phayne/PTM3D" target="_blank">PTM3D</a></li>
        </ul>
      </li>
      <li><a href="https://github.com/phayne/atmospheric-rt" target="_blank">Atmospheric radiative transfer</a></li>
      <li><a href="https://github.com/phayne/spectroscopy" target="_blank">Reflectance and emission spectroscopy</a></li>
    </ul>
  </div>
</div>
