---
title: "Specification-Driven Code Generation for Inter-parameter Dependencies in Web APIs"
collection: publications
category: conferences
permalink: /publication/2022-11-29-interparameter-code-generation
excerpt: 'Automatic code generation for APIs considering inter-parameter dependencies.'
date: 2022-11-29
venue: 'Service-Oriented Computing – ICSOC 2022 Workshops'
paperurl: 'https://ebarba.com/files/ICSOC_Automated_Code_Generation_Tool_for_Inter_parameters_in_Web_APIs.pdf'
citation: 'Barakat, S., Barba-Roque, E., Sánchez, A.B., Segura, S. (2022). &quot;Secification-Driven Code Generation for Inter-parameter Dependencies in Web APIs.&quot; <i>Service-Oriented Computing – ICSOC 2022 Workshops</i>.'
---

The generation of code templates from web API specifications is a common practice in the software industry. However, existing tools neglect the dependencies among input parameters (so called inter-parameter dependencies), extremely common in practice and usually described in natural language. As a result, developers are responsible for implementing the corresponding validation logic manually, a tedious and error-prone process. In this paper, we present an approach for the automated generation of code for inter-parameter dependencies in web APIs. Specifically, we exploit the IDL4OAS extension for specifying inter-parameter dependencies as a part of OpenAPI Specification (OAS) files. To make our approach applicable in practice, we present an extension of the popular OpenAPI Generator tool ecosystem, automating the generation of Java and Python code for the management of inter-parameter dependencies in both servers and clients. Evaluation results show the effectiveness of the approach in accelerating the development of APIs, generating up to 9.4 times more code than current generators, while making APIs potentially more reliable.
