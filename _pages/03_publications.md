---
layout: page
title: Publications
permalink: /publications/
---

### Programming books

* [Processing for Android: Creating mobile, sensor-aware, and VR applications using Processing]({{ site.url }}/androidbook){:target="_blank"}. _Apress_, 2017. ISBN: 978-1-4842-2718-3.

### Selected publications

<ul>
{% for pub in site.scipublications %}
  <li><a href="{{ pub.url | prepend: site.baseurl }}">{{ pub.title }}</a>. {{ pub.authors }}.
  <i>{{ pub.journal }}</i>. {{ pub.info }}.</li><br>
{% endfor %}    
</ul>

For a complete list of publications, check my [Google Scholar profile](https://scholar.google.com/citations?user=wvvJioMAAAAJ&hl=en){:target="_blank"}.


### Design Media Arts MFA Thesis

In 2009, I received an MFA degree from the [Design Media Arts Department](http://dma.ucla.edu/){:target="_blank"} at the University of California, Los Angeles. My thesis project was about the use of digital drawing and real-time video in live performance. The written thesis is available [here]({{ site.url }}/assets/publications/colubri-mfa_thesis-ucla.pdf).


### Mathematics Doctoral Thesis

My original background is in mathematics applied to the simulation of biopolymers (proteins and RNA). I obtained my PhD from the [department of Mathematics](http://www.matematica.uns.edu.ar/default.php){:target="_blank"} at the Universidad Nacional del Sur in Bahía Blanca, Argentina, in 2002, for my work on the coarse-graining of stochastic processes to describe the folding of protein molecules ([thesis pdf]({{ site.url }}/assets/publications/colubri-phd_thesis-uns.pdf), in Spanish).

<!-- Current projects
================

* Differentially-Private Machine Learning for fast outbreak response: Creating and evaluating new ML algorithms that can allow model sharing in infectious disease reearch and outbreak response while protecting patient privacy.

* Unbiased visual exploration of biomedical data: Developing new statistical measures of false discovery that can be applied to exploratory data analysis.

* Predictive modeling of infectious diseases: Using clinical metadata to find patterns of disease manifestation and predictors of outcome.

Past projects
=============

* Protein folding prediction: Coarse-grained models to simulate ab-initio folding of protein molecules. -->
