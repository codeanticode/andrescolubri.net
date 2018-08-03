---
layout: page
title: Mobile Health
banner: mhealth.jpg
description: Using machine learning and mobile platforms to fight disease
permalink: /projects/mhealth
image_sliders:
  - mhealth_lassa
---

This is my current research project in the [Sabeti lab](https://www.sabetilab.org/){:target="_blank"} at the [Broad Institute](https://www.broadinstitute.org/){:target="_blank"}. It is a multidisciplinary effort that involves the development of systems to collect epidemiological and genomic data of infectious diseases, the creation of new tools to integrate, visualize, and analyze that data, and the implementation of mechanisms by which the insights gained from the data can be used to inform public health interventions. There is a convergence of new technologies that could enable comprehensive platforms for disease surveillance and outbreak response: [next generation genome sequencing](https://www.ncbi.nlm.nih.gov/pubmed/28538734){:target="_blank"}, [mobile platforms for frontline data collection](https://www.dimagi.com/commcare/){:target="_blank"}, [low-cost rapid diagnostic kits](https://www.ncbi.nlm.nih.gov/pubmed/29700266){:target="_blank"}, and [computational approaches](https://privacytools.seas.harvard.edu/differential-privacy){:target="_blank"} to share outbreak data and models while protecting patient privacy. 

I have worked in different aspects of this larger project:

### Using prognosis models to offer tailored supportive care guidelines

Clinical guidelines are important to ensure that patients receive the proper supportive care. Often times these guidelines are made available as documents containing dozens or even [hundred of pages](http://www.who.int/csr/resources/publications/clinical-management-patients/en/){:target="_blank"}. In the context of an infectious disease outbreak, particularly in a resource-constrained region, these materials are not the best way for health care workers to adhere to the protocols and for new personnel to be properly trained. I have developed a mobile app that encapsulates prognosis models for Ebola Virus Disease, generated from data collected during the 2014-16 outbreak in West Africa. The predictions of these models are used to prioritize interventions depending on how much they would reduce illness severity. This app can be easily updated to incorporate better models, or even recommendations pertaining to other viral hemorrhagic fevers. The preprint of the paper describing this work is available on [bioRxiv](http://biorxiv.org/cgi/content/short/294587){:target="_blank"}.

<img img width="800" src="http://portfolio.andrescolubri.net/images/ebolarisk.jpg" style="background:none; border:none; box-shadow:none">
*Screenshots of the prototype app that provides clinical guidelines for Ebola patients.*

### Modeling clinical metadata to understand manifestations of disease

As part of the lab's long collaboration with the Irrua Specialist Teaching Hospital (ISTH) in Nigeria on the [characterization of the Lassa virus](https://www.ncbi.nlm.nih.gov/pubmed/26276630){:target="_blank"}, the causative agent of [Lassa fever](https://www.cdc.gov/vhf/lassa/index.html){:target="_blank"}, I worked closely with the physicians in the Lassa fever ward at ISTH to compile the largest and most detailed dataset of clinical information from Lassa fever patients in Nigeria. The analysis of this dataset allowed us to identify the clinical and laboratory predictors of outcome observed at ISTH for this deadly disease, and the results were published on [The Lancet Infectious Diseases](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(18)30121-X/fulltext){:target="_blank"} journal. We also designed and implemented an app for patient managment using the [CommCare platform](https://www.dimagi.com/commcare/) for mobile data collection. This app will enable the personnel at ISTH to generate reports and update the data much faster than in the past with paper-based records, and eventually to update our current models and analyses with the information from new patients. I wrote [this blog]({{ site.url}}/blog/2018/05/07/lassa_fever_in_nigeria_lessons_learnt.html){:target="_blank"} post about the process that lead to the paper and the clinical app.

{% include slider.html selector="mhealth_lassa" %}