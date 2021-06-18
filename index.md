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
<span>  <p> I am a Research Scientist at Adobe Research.</p>

<p> I received my bachelors degree in engineering physics from IIT Bombay. I obtained my MS and PhD from the department of mathematics at Yale University under the guidance of <a href="http://cs-www.cs.yale.edu/homes/spielman/">Daniel Spielman</a>. I was later a Postdoctoral Fellow in the School of Computer Science at Georgia Tech with <a href="https://www.cc.gatech.edu/~vempala/">Santosh Vempala</a> where I also worked with <a href="https://www.cc.gatech.edu/~rpeng/">Richard Peng</a>. 
</p>

<p> My main interest is in design of fast algorithms with provable guarantees, and their application to machine learning and causal inference.</p>
</span>
</figure>

<h2>Selected Publications</h2>

<br>
{% assign publications = site.publications | sort: "date" | reverse %}
{% for pub in publications %}
<div class="pubitem">
  <div>{{ pub.title }}, <i> {{ pub.venue }}, </i> {{ pub.date | date: "%Y"}} </div>
  <div>{{ pub.authors }} </div>
  <br>
</div>


{% endfor %}






