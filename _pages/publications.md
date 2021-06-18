---
layout: default
title: "Publications"
permalink: /publications/
author_profile: true
---

<h1 class="mt-4">Publications</h1>
{% assign publications = site.publications | sort: "year" | reverse %}
{% for pub in publications %}
<div class="pubitem">
  <div>{{ pub.title }}, <i> {{ pub.venue }}, </i> {{ pub.date | date: "%Y"}} </div>
  <div>{{ pub.authors }} </div>
  <br>
</div>


{% endfor %}


