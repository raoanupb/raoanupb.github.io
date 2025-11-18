---
layout: default
excerpt_separator: <!--more-->
title: 
description: A visual breakdown of how to use the ET jekyll theme
permalink: /index.html
date: 2018-01-14
---

<figure>
<img loading="lazy" src="{{ site.baseurl }}/images/me.jpg" width='250px' />
<span>  <p> I am a research scientist at Adobe Research.</p>

<p> I received my bachelors degree in engineering physics from IIT Bombay. I obtained my MS and PhD from the department of mathematics at Yale University under the guidance of <a href="http://cs-www.cs.yale.edu/homes/spielman/">Daniel Spielman</a>. I was later a postdoctoral fellow in the School of Computer Science at Georgia Tech with <a href="https://www.cc.gatech.edu/~vempala/">Santosh Vempala</a> where I also worked with <a href="https://www.cc.gatech.edu/~rpeng/">Richard Peng</a>. 
</p>

<p> My research focuses on <strong>machine learning, experimental design, and causal inference</strong>, with applications to generative AI, treatment effect estimation, and optimization. I develop algorithms with provable guarantees for real-world problems.</p>

<p style="margin-top: 1rem;">
  <a href="https://scholar.google.com/citations?user=pkwXPU0AAAAJ&hl=en">Google Scholar</a> ·
  <a href="https://research.adobe.com/person/anup-rao/">Adobe Research</a>
</p>
</span>
</figure>

<h2>Selected Publications</h2>

<br>
{% assign publications = site.publications | sort: "date" | reverse %}
{% for pub in publications %}
<div class="pubitem">
  <div>
    <span class="venue-badge {{ pub.venue_class }}">{{ pub.venue }} {{ pub.date | date: "%Y"}}</span>
  </div>
  <h3 class="pub-title">{{ pub.title }}</h3>
  <div class="pub-authors">{{ pub.authors }}</div>

  {% if pub.excerpt %}
  <details class="pub-abstract">
    <summary>Abstract & Links</summary>
    <p>{{ pub.excerpt }}</p>
    <div class="pub-links">
      {% if pub.paperurl %}<a href="{{ pub.paperurl }}" target="_blank">Paper</a>{% endif %}
    </div>
  </details>
  {% endif %}
</div>
{% endfor %}






