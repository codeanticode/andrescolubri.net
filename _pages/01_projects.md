---
layout: projects
title: Projects
permalink: /projects/
---

This is a selection of individual and collaborative projects across science, art, and technology:<br><br>

<div class="portfolio-container">
  {% for project in site.projects reversed %}
  <div class="portfolio-element">
    <a href="{{ project.url | prepend: site.baseurl }}" target="_blank"><img class="portfolio-image" src="http://portfolio.andrescolubri.net/banners/{{ project.banner }}" alt="image"></a>
    <p class="portfolio-caption">{{ project.title }}</p>
  </div>
  {% endfor %}
</div>
