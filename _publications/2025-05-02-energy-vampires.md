---
title: "Unveiling the Energy Vampires: A Methodology for Debugging Software Energy Consumption"
authors:
    - Enrique Barba Roque
    - Luis Cruz
    - Thomas Durieux
collection: publications
category: conferences
permalink: /publication/2025-05-02-energy-vampires
excerpt: 'Energy debugging methodology for identifying and isolating energy consumption hotspots in software systems, with Alpine consuming up to 20.2% more power than Ubuntu in certain operations.'
date: 2025-03-17
venue: 'International Conference on Software Engineering, Ottawa, Canada'
award: 'ACM SIGSOFT Distinguished Paper Award'
paperurl: 'https://arxiv.org/abs/2412.10063'
# citation: ''
abstract: "Energy consumption in software systems is becoming increasingly important, especially in large-scale deployments. However, debugging energy-related issues remains challenging due to the lack of specialized tools. This paper presents an energy debugging methodology for identifying and isolating energy consumption hotspots in software systems. We demonstrate the methodology's effectiveness through a case study of Redis, a popular in-memory database. Our analysis reveals significant energy consumption differences between Alpine and Ubuntu distributions, with Alpine consuming up to 20.2% more power in certain operations. We trace this difference to the implementation of the memcpy function in different C standard libraries (musl vs. glibc). By isolating and benchmarking memcpy, we confirm it as the primary cause of the energy discrepancy. Our findings highlight the importance of considering energy efficiency in software dependencies and demonstrate the capability to assist developers in identifying and addressing energy-related issues. This work contributes to the growing field of sustainable software engineering by providing a systematic approach to energy debugging and using it to unveil unexpected energy behaviors in Alpine."
bibtex: |-
  @inproceedings{DBLP:conf/icse/RoqueCD25,
  author       = {Enrique Barba Roque and
                  Luis Cruz and
                  Thomas Durieux},
  title        = {Unveiling the Energy Vampires: {A} Methodology for Debugging Software
                  Energy Consumption},
  booktitle    = {47th {IEEE/ACM} International Conference on Software Engineering,
                  {ICSE} 2025, Ottawa, ON, Canada, April 26 - May 6, 2025},
  pages        = {2406--2418},
  publisher    = {{IEEE}},
  year         = {2025},
  url          = {https://doi.org/10.1109/ICSE55347.2025.00118},
  doi          = {10.1109/ICSE55347.2025.00118},
  timestamp    = {Tue, 01 Jul 2025 06:48:58 +0200},
  biburl       = {https://dblp.org/rec/conf/icse/RoqueCD25.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
  }

---

{% if post.award %}
      <span class="award-badge">🏆 {{post.award}}</span>
{% endif %}

Energy consumption in software systems is becoming increasingly important, especially in large-scale deployments. However, debugging energy-related issues remains challenging due to the lack of specialized tools. This paper presents an energy debugging methodology for identifying and isolating energy consumption hotspots in software systems. We demonstrate the methodology's effectiveness through a case study of Redis, a popular in-memory database. Our analysis reveals significant energy consumption differences between Alpine and Ubuntu distributions, with Alpine consuming up to 20.2% more power in certain operations. We trace this difference to the implementation of the memcpy function in different C standard libraries (musl vs. glibc). By isolating and benchmarking memcpy, we confirm it as the primary cause of the energy discrepancy. Our findings highlight the importance of considering energy efficiency in software dependencies and demonstrate the capability to assist developers in identifying and addressing energy-related issues. This work contributes to the growing field of sustainable software engineering by providing a systematic approach to energy debugging and using it to unveil unexpected energy behaviors in Alpine.

[Paper](https://ieeexplore.ieee.org/document/11029858) - [Pre-print](https://arxiv.org/abs/2412.10063)
