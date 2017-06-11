---
layout: page
title: Teaching
permalink: /teaching/
---

I have been teaching and mentoring students for several years, across different topics (computational arts, bioinformatics, engineering) and settings (college and graduate school, summer programs, internships). Sharing knowledge and experience is one of my most rewarding experiences, and one where I believe I learned as much as my students did.

Follow the links in the list below to get more details about these courses, workshops, and internships I taught and mentored, including slides and other course materials:

<ul>
{% for course in site.teaching %}
  <li><a href="{{ course.url | prepend: site.baseurl }}">{{ course.title }}</a>:
  {{ course.description }}</li><br>
{% endfor %}    
</ul>