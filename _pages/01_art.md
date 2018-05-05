---
layout: page
title: Art
permalink: /art/
---

My art projects seek to incorporate spontaneous human interaction and intuition into algorithmic systems. I also develop software tools to create code-based artworks.

In 2009, I received an MFA degree from the [Design Media Arts Department](http://dma.ucla.edu/){:target="_blank"} at the University of California, Los Angeles. My thesis project was about the use of digital drawing and real-time video in live performance. The written thesis is available [here]({{ site.url }}/assets/art/colubri-mfa_thesis-ucla.pdf).

Follow [this link]({{ site.url }}/portfolio) for an online slideshow of my projects, or check the selected projects below:

<ul>
{% for proj in site.artprojects %}
  <li><a href="{{ proj.url | prepend: site.baseurl }}">{{ proj.title }}</a>:
  {{ proj.description }}</li><br>
{% endfor %}    
</ul>

### Art workshops and courses

I have also taught some workshops on art and code:

<ul>
{% for course in site.artteaching %}
  <li><a href="{{ course.url | prepend: site.baseurl }}">{{ course.title }}</a>:
  {{ course.description }}</li><br>
{% endfor %}    
</ul>
