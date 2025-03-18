---
author: Roberto Verdecchia, June Sallou, Luís Cruz
journal: WIDM
title: "A systematic review of Green AI"
year: 2023
doi: 10.1002/widm.1507
abstract: "With the ever-growing adoption of artificial intelligence (AI)-based systems, the carbon footprint of AI is no longer negligible. AI researchers and practitioners are therefore urged to hold themselves accountable for the carbon emissions of the AI models they design and use. This led in recent years to the appearance of researches tackling AI environmental sustainability, a field referred to as Green AI. Despite the rapid growth of interest in the topic, a comprehensive overview of Green AI research is to date still missing. To address this gap, in this article, we present a systematic review of the Green AI literature. From the analysis of 98 primary studies, different patterns emerge. The topic experienced a considerable growth from 2020 onward. Most studies consider monitoring AI model footprint, tuning hyperparameters to improve model sustainability, or benchmarking models. A mix of position papers, observational studies, and solution papers are present. Most papers focus on the training phase, are algorithm-agnostic or study neural networks, and use image data. Laboratory experiments are the most common research strategy. Reported Green AI energy savings go up to 115%, with savings over 50% being rather common. Industrial parties are involved in Green AI studies, albeit most target academic readers. Green AI tool provisioning is scarce. As a conclusion, the Green AI research field results to have reached a considerable level of maturity. Therefore, from this review emerges that the time is suitable to adopt other Green AI research strategies, and port the numerous promising academic results to industrial practice."
bibtex: |-
  @article{https://doi.org/10.1002/widm.1507,
    author = {Verdecchia, Roberto and Sallou, June and Cruz, Luís},
    title = {A systematic review of Green AI},
    journal = {WIREs Data Mining and Knowledge Discovery},
    volume = {13},
    number = {4},
    pages = {e1507},
    keywords = {artificial intelligence, environmental sustainability, Green AI, systematic literature review},
    doi = {https://doi.org/10.1002/widm.1507},
    url = {https://wires.onlinelibrary.wiley.com/doi/abs/10.1002/widm.1507},
    eprint = {https://wires.onlinelibrary.wiley.com/doi/pdf/10.1002/widm.1507},
    year = {2023}
  }

# image: "garciamartin-estimation.png"
tags:
  - Green AI
  - Literature Review
annotation: |-
  This study performs a systematic literature review of the field of Green AI. They analyze 98 studies in the field of Green AI, and report a number of relevant statistics about the field.

  Most papers published to date propose **solutions** to tackle energy efficiency in AI, and focus more on **monitoring** and **benchmarking** energy consumption of AI models or **hyperparameter tuning** to improve energy efficiency of the model.

  The majority of work does **not focus on a specific domain**, and from those who do, they tend to focus on **edge computing**. This is reasonable, since edge devices are more energy limited, so energy efficient becomes a more relevant problem in the area. 

  This exhaustive review also highlights areas where more research is necessary. For example, there is little research on **estimation** of energy consumption, which can be helpful for developers to have an approximate idea on how the model will perform. Most studies are also run in laboratory settings and controlled environments. Given the extent of academic results, it would be helpful to translate some of these result into studies in industry and live environments.
show-thoughts: false
---