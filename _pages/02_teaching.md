---
layout: page
title: Teaching
permalink: /teaching/
---

### Scientific mentoring and teaching

<ul>
{% for course in site.sciteaching %}
  <li><a href="{{ course.url | prepend: site.baseurl }}">{{ course.title }}</a>:
  {{ course.description }}</li><br>
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

### Google Summer of Code

Since 2014, I have mentored students participating in the [Google Summer of Code](https://summerofcode.withgoogle.com/){:target="_blank"} (GSoC) program, under the sponsorship of the [Processing Foundation](https://processingfoundation.org/){:target="_blank"}:

* GSoC 2018: [GLSL Editor for PDE](https://summerofcode.withgoogle.com/dashboard/organization/4915113891463168/proposal/5269541785960448/){:target="_blank"} by Izza Tariq

* GSoC 2017: [Build system migration from Ant to Gradle](https://procandsoc17.wordpress.com/){:target="_blank"} by Rupak Das, and [VR Mode Demo in Processing for Android](https://picorana.github.io/blog){:target="_blank"} by Sara Di Barolomeo (co-mentored with [Gottfried Haider](http://ghai.xyz/){:target="_blank"})

* GSoC 2015: [Enhancements in Processing’s Android mode](http://omerjerk.in/index.php/2015/08/15/gsoc-2015-the-processing-foundation/){:target="_blank"} by Umair Khan.

* GSoC 2014: [Android Mode for Processing 3.0](https://www.google-melange.com/archive/gsoc/2014/orgs/processing/projects/imilka.html){:target="_blank"} by Imil Ziyaztdinov, and [New video library using GStreamer 1.x](https://github.com/gstreamer-java/gir2java/wiki/GSOC-2014-report){:target="_blank"} by Roland Elek.

