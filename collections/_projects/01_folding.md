---
layout: page
title: Protein Folding
banner: folding.jpg
description: Digital stage design using real-time projections
permalink: /projects/folding
---

After I received my doctoral degree in Mathematics at the [Universidad Nacional del Sur](http://uns.edu.ar/){:target="_blank"} in Bahía Blanca, Argentina, I carried out research at the [University of Chicago](https://www.uchicago.edu/){:target="_blank"} (in the groups of professors Tobin Sosnick, Karl Freed, and Steve Berry) on the so-called [Protein Folding Problem](https://en.wikipedia.org/wiki/Protein_structure_prediction){:target="_blank"}, where the goal is to predict, using computational methods, the three-dimensional structure of a protein molecule given its amino-acid sequence: 

<img width="740" src="http://portfolio.andrescolubri.net/images/protein-folding.jpg" style="background:none; border:none; box-shadow:none"/>

The video below gives a nice non-expert introduction to the protein folding folding problem, and its implications in biotechnology and medicine:

{% include youtube.html id="cAJQbSLlonI"  width="100%" %}

I created algorithms that folded proteins with fewer computational resources than traditional methods by using a simplified, or coarse-grained, representation of the protein molecule:


<img width="740" src="http://portfolio.andrescolubri.net/images/folding-algorithm.jpg" style="background:none; border:none; box-shadow:none"/>

These folding algorithms predicted structures that were fairly close to the real structure of small, globular proteins, as seen in the image below (the ribbon diagrams on the left represent the 3D structure of the predicted and real molecules, and the scatter plots on the right show the "energy" of the simulated structures in the vertical axis versus the distance between the simulated structure and the target structure):

<img width="740" src="http://portfolio.andrescolubri.net/images/folding-results.jpg" style="background:none; border:none; box-shadow:none"/>

I published a number of academic papers on that subject, such as [this one](http://portfolio.andrescolubri.net/articles/jmb2006_intrabasin_colubri.pdf){:target="_blank"} summarizing most of my research at the University of Chicago. All the software tools I developed at that time to run our "coarse-grained" folding algorithms, including the Protein Library, a general and extensible C library and utilities to implement simulations of macromolecules, are available online [here](http://protlib.uchicago.edu/){:target="_blank"}.


