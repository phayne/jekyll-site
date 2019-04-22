---
layout: page
title: research
permalink: /research/
description:
---

<div class="summary">
Research in the EPIC group spans a range of planetary bodies, unified by a focus
on ice and volatiles. We use numerical methods to model planetary
surfaces and atmospheres, making and testing predictions using remote sensing data.
<br><br>
Below, you will find links to summaries of past and ongoing research projects.
Links to data products are also provided, in the spirit of "open science."
</div>


{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="\_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}

<br>
<u>Data Products:</u>
<ul>Moon
  <li><a href="https://goo.gl/JhMGs5" target="\_blank">Diviner H-parameter</a> (thermal inertia).
  <p>In this directory, you will find maps of the H-parameter in meters, along with latitude and longitude grids.
  These data files are in 32-bit floating point format, 128 pixels per degree (ppd), spanning -70 to +70 degrees latitude.
  Also provided in the same directory are thermal inertia (referenced to 273 K) maps at 10 ppd.</p></li>
</ul>
