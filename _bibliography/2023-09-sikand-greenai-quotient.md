---
author: Samarth Sikand, Vibhu Saujanya Sharma, Vikrant Kaulgud, Sanjay Podder
journal: ASE
title: "Green AI Quotient: Assessing Greenness of AI-based software and the way forward"
year: 2023
doi: 10.1109/ASE56229.2023.00115
abstract: "As the world takes cognizance of AI's growing role in greenhouse gas(GHG) and carbon emissions, the focus of AI research & development is shifting towards inclusion of energy efficiency as another core metric. Sustainability, a core agenda for most organizations, is also being viewed as a core non-functional requirement in software engineering. A similar effort is being undertaken to extend sustainability principles to AI-based systems with focus on energy efficient training and inference techniques. But an important question arises, does there even exist any metrics or methods which can quantify adoption of “green” practices in the life cycle of AI-based systems? There is a huge gap which exists between the growing research corpus related to sustainable practices in AI research and its adoption at an industry scale. The goal of this work is to introduce a methodology and novel metric for assessing “greenness” of any AI-based system and its development process, based on energy efficient AI research and practices. The novel metric, termed as Green AI Quotient, would be a key step towards AI practitioner's Green AI journey. Empirical validation of our approach suggest that Green AI Quotient is able to encourage adoption and raise awareness regarding sustainable practices in AI lifecycle."
bibtex: |-
  @inproceedings{10298412,
    author = {S. Sikand and V. Sharma and V. Kaulgud and S. Podder},
    booktitle = {2023 38th IEEE/ACM International Conference on Automated Software Engineering (ASE)},
    title = {Green AI Quotient: Assessing Greenness of AI-based software and the way forward},
    year = {2023},
    volume = {},
    issn = {},
    pages = {1828-1833},
    keywords = {measurement;training;industries;organizations;carbon dioxide;energy efficiency;software},
    doi = {10.1109/ASE56229.2023.00115},
    url = {https://doi.ieeecomputersociety.org/10.1109/ASE56229.2023.00115},
    publisher = {IEEE Computer Society},
    address = {Los Alamitos, CA, USA},
    month = {sep}
  }
# image: "garciamartin-estimation.png"
tags:
  - Green AI in Industry
  - Green AI Practices
annotation: |-
  The paper proposes an approach to characterize the sustainability of AI projects in industry. While there has been an increase in research on Green AI in academia, this increase has barely translated into industry application, with most industry AI projects not adopting sustainability practices proposed by research. The authors claim that there is a lack of awareness and knowledge material in the industry, and research is not easily consumable by most industry AI developments. Additionally, some industry projects tend to use external and closed source AI systems, which makes measuring their environmental impact difficult.

  To tackle this problem, the authors propose a questionnaire-based approach called Grenn AI Quotient. They selected and studied 40 research works in Green AI, and derived a corpus of 25 questions that cover all the stages of the AI lifecycle. These questions are divided into Project Characterization, collecting information like task domain (e.g. What kind of task is the AI model solving?), and Core Questions, with ordinal responses extracted from the studied works and gauge the use of Green AI technique (e.g. Have you considered the energy mix of cloud or on-premise data-centers when planning to deploy your AI model?) 

  The responses are scored and aggregated by weighting, and the final score is normalized between 0 and 1, with 0 meaning there are no sustainable practices in the project, and 1 meaning the project follows all Green AI recommended practices. The system also recommends which practices to apply, based on the responses and type of project.
thoughts: |-
  The proposed system is a good solution to make Green AI and sustainability practices more approachable for industry developers, who are often unaware of the developments in academia. However, their deployment is proprietary, and they did not release the full questionnaire and scoring and recommendation methods. The evaluation of the system is also not extensive, limited to two in-house projects.

  Despite this, I believe this can be a good approach to increase the level of adoption of Green AI practices. We should strive towards making our findings easily digestible for people outside of academia, who account for the greatest share in the environmental impact of AI.
show-thoughts: true
---


