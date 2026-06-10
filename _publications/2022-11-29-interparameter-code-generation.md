---
title: "Specification-Driven Code Generation for Inter-parameter Dependencies in Web APIs"
authors:
    - Saman Barakat
    - Enrique Barba Roque
    - Ana Belén Sánchez
    - Sergio Segura
collection: publications
category: conferences
permalink: /publication/2022-11-29-interparameter-code-generation
excerpt: 'Automatic code generation for APIs considering inter-parameter dependencies.'
date: 2022-11-29
venue: 'Service-Oriented Computing – ICSOC 2022 Workshops'
paperurl: 'https://ebarba.com/files/ICSOC_Automated_Code_Generation_Tool_for_Inter_parameters_in_Web_APIs.pdf'
citation: 'Barakat, S., Barba-Roque, E., Sánchez, A.B., Segura, S. (2022). &quot;Secification-Driven Code Generation for Inter-parameter Dependencies in Web APIs.&quot; <i>Service-Oriented Computing – ICSOC 2022 Workshops</i>.'
bibtex: |-
  @inproceedings{DBLP:conf/icsoc/BarakatRSS22,
  author       = {Saman A. Barakat and
                  Enrique Barba Roque and
                  Ana Bel{\'{e}}n S{\'{a}}nchez and
                  Sergio Segura},
  editor       = {Javier Troya and
                  Raffaela Mirandola and
                  Elena Navarro and
                  Andrea Delgado and
                  Sergio Segura and
                  Guadalupe Ortiz and
                  Cesare Pautasso and
                  Christian Zirpins and
                  Pablo Fern{\'{a}}ndez and
                  Antonio Ruiz{-}Cort{\'{e}}s},
  title        = {Specification-Driven Code Generation for Inter-parameter Dependencies
                  in Web APIs},
  booktitle    = {Service-Oriented Computing - {ICSOC} 2022 Workshops - ASOCA, AI-PA,
                  FMCIoT, {WESOACS} 2022, Sevilla, Spain, November 29 - December 2,
                  2022 Proceedings},
  series       = {Lecture Notes in Computer Science},
  pages        = {261--273},
  publisher    = {Springer},
  year         = {2022},
  url          = {https://doi.org/10.1007/978-3-031-26507-5\_21},
  doi          = {10.1007/978-3-031-26507-5\_21},
  timestamp    = {Sun, 16 Apr 2023 20:30:30 +0200},
  biburl       = {https://dblp.org/rec/conf/icsoc/BarakatRSS22.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
  }
---

The generation of code templates from web API specifications is a common practice in the software industry. However, existing tools neglect the dependencies among input parameters (so called inter-parameter dependencies), extremely common in practice and usually described in natural language. As a result, developers are responsible for implementing the corresponding validation logic manually, a tedious and error-prone process. In this paper, we present an approach for the automated generation of code for inter-parameter dependencies in web APIs. Specifically, we exploit the IDL4OAS extension for specifying inter-parameter dependencies as a part of OpenAPI Specification (OAS) files. To make our approach applicable in practice, we present an extension of the popular OpenAPI Generator tool ecosystem, automating the generation of Java and Python code for the management of inter-parameter dependencies in both servers and clients. Evaluation results show the effectiveness of the approach in accelerating the development of APIs, generating up to 9.4 times more code than current generators, while making APIs potentially more reliable.
