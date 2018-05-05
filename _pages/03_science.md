---
layout: page
title: Science
permalink: /science/
---

I do research in exploratory data analysis and predictive modeling of infectious diseases.

My original background is in mathematics applied to the simulation of biopolymers (proteins and RNA). I obtained my PhD from the [department of Mathematics](http://www.matematica.uns.edu.ar/default.php){:target="_blank"} at the Universidad Nacional del Sur in Bahía Blanca, Argentina, in 2002, for my work on the coarse-graining of stochastic processes to describe the folding of protein molecules ([thesis pdf]({{ site.url }}/assets/science/colubri-phd_thesis-uns.pdf), in Spanish).

### Selected publications

<ul>
{% for pub in site.scipublications %}
  <li><a href="{{ pub.url | prepend: site.baseurl }}">{{ pub.title }}</a>. {{ pub.authors }}.
  <i>{{ pub.journal }}</i>. {{ pub.info }}.</li>
{% endfor %}    
</ul>

For a complete list of publications, refer to my [Google Scholar profile](https://scholar.google.com/citations?user=wvvJioMAAAAJ&hl=en){:target="_blank"}.

### Teaching and mentoring

<ul>
{% for course in site.sciteaching %}
  <li><a href="{{ course.url | prepend: site.baseurl }}">{{ course.title }}</a>:
  {{ course.description }}</li><br>
{% endfor %}    
</ul>

<!-- Current projects
================

* Differentially-Private Machine Learning for fast outbreak response: Creating and evaluating new ML algorithms that can allow model sharing in infectious disease reearch and outbreak response while protecting patient privacy.

* Unbiased visual exploration of biomedical data: Developing new statistical measures of false discovery that can be applied to exploratory data analysis.

* Predictive modeling of infectious diseases: Using clinical metadata to find patterns of disease manifestation and predictors of outcome.

Past projects
=============

* Protein folding prediction: Coarse-grained models to simulate ab-initio folding of protein molecules. -->
