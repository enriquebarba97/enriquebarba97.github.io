---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

[PDF version]({{ '/files/CV_EnriqueBarbaRoque.pdf' | relative_url }})

Education
======
* Ph.D in Green AI, TU Delft, 2024 -- 2029 (expected)
* MsC in Computer Science - Software Technologies, TU Delft, 2022 -- 2024
* BsC in Compupter Science - Software Engineering, University of Seville, 2017 -- 2021

Work experience
======
* October 2022 -- March 2023: **Part-time Fullstack Developer @ Rotate** (Utrecht, The Netherlands)
  * Development from scratch of the new web application for analysis of air cargo capacities and revenues for airlines.
  * Active participation in the design process, providing suggestions on UI decisions, and testing different frameworks and libraries to choose the one to use.
  * Angular App with Fuse for user interface, and NestJS for an API used both by the frontend and customers of the company.
  * Application deployed using Amazon Web Services: Amplify with Cognito for user management.
  * Data integration with Databricks through headless BI tool CubeJS, and chart creation with Apache Echarts.

* September 2021 -- August 2022: **Full-time Junior Java Developer @ Ayesa Advanced Technologies** (Sevilla, Spain)
  * Maintenance and development of enterprise applications for the Andalusian Statistics and Cartography Institute and Culture and Historic Conservation Agency.
  * Worked in different teams of various sizes (2-7 people) in a Scrum environment. Multidisciplinar teams with analysts, architects, and developers.
  * Position and responsibilities: Fullstack Java web development using Spring Framework and JSP with Thymeleaf or Angular. Development of new features, testing, updating documentation, and deliverables.
  * Also worked on improving the quality of the different projects through refactoring and bug fixing. Around 30\% of the code had to be fixed or redone, and multiple vital functionalities had to be developed. Successfully delivered numerous versions to the clients, all met with satisfaction on their end.

* September 2018 -- June 2019: **Student Research Assistant @ University of Seville** (Sevilla, Spain)
  * Research into API Documentations to classify dependencies between parameters for a [paper](https://personal.us.es/sergiosegura/files/papers/martinlopez19-icsoc.pdf) by a PhD student. This experience eventually lead to my bachelor thesis in the subject, implementing automatic code generation for APIs considering these dependencies.
  
Projects
======
* **Discovering energy inefficiencies in Docker through tracing** \| Master Thesis
  * Research project on Sustainable Software Engineering (SSE) about the energy consumption of different Docker images
  * Design a methodology to explain observed energy inefficiencies in Docker images, finding suboptimal implementations of core library functions
  * Found previously unknown energy inefficiencies in the Alpine C standard library
  * Presented our results in a [KDE Eco community meeting]({{ '/talks/2024-06-12-kde-talk' | relative_url }}) to a panel of experts in SSE who agreed with the relevance of the results
  * [Thesis report](https://repository.tudelft.nl/islandora/object/uuid:86008575-a117-4bac-94b5-11525321103c?collection=education)
  
<!-- Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3 -->

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
<!-- Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul> -->
  
<!-- Service and leadership
======
* Currently signed in to 43 different slack teams -->
