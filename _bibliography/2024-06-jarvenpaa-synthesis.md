---
layout: publication
author: Heli Järvenpää, Patricia Lago, Justus Bogner, Grace Lewis, Henry Muccini, Ipek Ozkaya
journal: ICSE-SEIS
title: "A Synthesis of Green Architectural Tactics for ML-Enabled Systems"
year: 2024
doi: 10.1145/3639475.3640111
abstract: "The rapid adoption of artificial intelligence (AI) and machine learning (ML) has generated growing interest in understanding their environmental impact and the challenges associated with designing environmentally friendly ML-enabled systems. While Green AI research, i.e., research that tries to minimize the energy footprint of AI, is receiving increasing attention, very few concrete guidelines are available on how ML-enabled systems can be designed to be more environmentally sustainable. In this paper, we provide a catalog of 30 green architectural tactics for ML-enabled systems to fill this gap. An architectural tactic is a high-level design technique to improve software quality, in our case environmental sustainability. We derived the tactics from the analysis of 51 peer-reviewed publications that primarily explore Green AI, and validated them using a focus group approach with three experts. The 30 tactics we identified are aimed to serve as an initial reference guide for further exploration into Green AI from a software engineering perspective, and assist in designing sustainable ML-enabled systems. To enhance transparency and facilitate their widespread use and extension, we make the tactics available online in easily consumable formats. Wide-spread adoption of these tactics has the potential to substantially reduce the societal impact of ML-enabled systems regarding their energy and carbon footprint."
bibtex: |-
  @inproceedings{10.1145/3639475.3640111,
    author = {J\"{a}rvenp\"{a}\"{a}, Heli and Lago, Patricia and Bogner, Justus and Lewis, Grace and Muccini, Henry and Ozkaya, Ipek},
    title = {A Synthesis of Green Architectural Tactics for ML-Enabled Systems},
    year = {2024},
    isbn = {9798400704994},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3639475.3640111},
    doi = {10.1145/3639475.3640111},
    abstract = {The rapid adoption of artificial intelligence (AI) and machine learning (ML) has generated growing interest in understanding their environmental impact and the challenges associated with designing environmentally friendly ML-enabled systems. While Green AI research, i.e., research that tries to minimize the energy footprint of AI, is receiving increasing attention, very few concrete guidelines are available on how ML-enabled systems can be designed to be more environmentally sustainable. In this paper, we provide a catalog of 30 green architectural tactics for ML-enabled systems to fill this gap. An architectural tactic is a high-level design technique to improve software quality, in our case environmental sustainability. We derived the tactics from the analysis of 51 peer-reviewed publications that primarily explore Green AI, and validated them using a focus group approach with three experts. The 30 tactics we identified are aimed to serve as an initial reference guide for further exploration into Green AI from a software engineering perspective, and assist in designing sustainable ML-enabled systems. To enhance transparency and facilitate their widespread use and extension, we make the tactics available online in easily consumable formats. Wide-spread adoption of these tactics has the potential to substantially reduce the societal impact of ML-enabled systems regarding their energy and carbon footprint.},
    booktitle = {Proceedings of the 46th International Conference on Software Engineering: Software Engineering in Society},
    pages = {130–141},
    numpages = {12},
    keywords = {software architecture, architectural tactics, ML-enabled systems, environmental sustainability, green AI},
    location = {Lisbon, Portugal},
    series = {ICSE-SEIS'24}
  }
# image: "tactics.png"
tags:
  - Architectural Tactics
  - ML systems
annotation: |-
  In this paper, the authors present a compilation of 30 green architectural tactics to improve the energy efficiency of Machine Learning systems. The tactics are organized by categories based on the different aspects of the development cycle of ML software. They compiled this list by analyzing 51 scientific papers on Green AI and with a discussion with experts in a focus group. 

  | ---------------------------------------------------------------------------------------------------------------------- |
  | **Data-centric**       | **Algorithm design**                                  | **Model optimization**                        | **Model training**                              | **Deployment**                                          | **Management**                       |
  | ---------------------- | ---------------------------------------------------- | -------------------------------------------- | ------------------------------------------------ | ------------------------------------------------------ | ------------------------------------ |
  | **T1**: Apply sampling techniques  | **T6**: Choose an energy-efficient algorithm        | **T12**: Set energy consumption as a model constraint | **T18**: Use quantization-aware training         | **T21**: Consider federated learning                   | **T28**: Use informed adaptation   |
  | **T2**: Remove redundant data      | **T7**: Choose a lightweight algorithm alternative | **T13**: Consider graph substitution          | **T19**: Use checkpoints during training         | **T22**: Use computation partitioning                 | **T29**: Retrain the model if needed |
  | **T3**: Reduce number of data features | **T8**: Decrease model complexity               | **T14**: Enhance model sparsity                | **T20**: Design for memory constraints         | **T23**: Apply cloud fog network architecture         | **T30**: Monitor computing power    |
  | **T4**: Use input quantization      | **T9**: Consider reinforcement learning for energy efficiency | **T15**: Consider energy-aware pruning        |                                                  | **T24**: Use energy-efficient hardware                |                                      |
  | **T5**: Use data projection         | **T10**: Use dynamic parameter adaptation         | **T16**: Consider transfer learning            |                                                  | **T25**: Use power capping                            |                                      |
  |                                    | **T11**: Use built-in library functions          | **T17**: Consider knowledge distillation       |                                                  | **T26**: Use energy-aware scheduling                  |                                      |
  |                                    |                                                  |                                                |                                                  | **T27**: Minimize referencing to data               |                                      |

  The data-centric tactics focus on reducing the size of the data, either by reducing the total amount of samples by applying sampling techniques and removing redundant data, or reducing the size of the samples by removing unnecessary features that don't provide more accuracy or using smaller precision floating points. Having less data directly translates into less computation and therefore less energy usage.

  For algorithm design, some recommendations are choosing efficient and lightweight alternatives for algorithms. Depending on your problem and data, some algorithms might be overkill, and more efficient options are available. For model design, most tactics go again through reducing the size and computation needed, by decreasing model complexity, enhancing model sparsity, and pruning weights with small contributions to the final results. Another relevant tactic is to consider energy consumption as a constraint in the model and optimize for it in the same way as accuracy. During training, some suggestions are to quantize and use lower precision weights, and use checkpoints to avoid repeating the whole training in case of failure.

  For the usage of ML in deployment, most recommendations are derivatives of sharing the training/inference workload between different devices. For example, using federated learning and saving energy on data transfer, or partitioning the computation process between different devices according to their capabilities and power constraints. Some other suggestions are to set up power caps and use energy-aware scheduling to run certain processes based on current system conditions. For the management of the ML model during its lifetime, some tactics are to use informed adaptation and modify the model only when concept drift is detected. Also, when concept drift is detected, retraining on new data is usually preferable to redesigning the whole model.

  While an overview of these tactics is useful, they are not generalizable, and domain expertise is needed to determine which tactics can be applied to specific projects. However, they are a good starting point for a ML project that wants to optimize not only for accuracy, buy also for energy efficiency.
show-thoughts: false
---


