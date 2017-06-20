---
layout: page
title: Art
permalink: /art/
---

I make individual and collaborative art projects that rely on computer code, user interaction, and data from different sources (typically scientific, although that's not always the case). With these projects, I try to create a personal narrative that brings together my interest in art, science, and technology.

In 2009, I received an MFA degree from the [Design Media Arts Department](http://dma.ucla.edu/){:target="_blank"} at the University of California, Los Angeles. My thesis project was about the practice of live cinema, and the use of different techniques (digital drawing, real-time video) in a performance I created based on memories of the Challenger disaster. The written thesis is available [here]({{ site.url }}/assets/art/colubri-mfa_thesis-ucla.pdf).

Follow [this link]({{ site.url }}/portfolio) for an online slideshow of my projects, or check selected projects below:

<ul>
{% for proj in site.artprojects %}
  <li><a href="{{ proj.url | prepend: site.baseurl }}">{{ proj.title }}</a>:
  {{ proj.description }}</li><br>
{% endfor %}    
</ul>

For work-in-progress documentation and experiments, please take a look at my [vimeo](https://vimeo.com/user1182080) and [tumblr](https://codeanticode.tumblr.com/) pages, as well as my [blog](http://andrescolubri.net/).



