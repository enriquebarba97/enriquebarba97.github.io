---
author: Timur Babakol, Yu David Liu
journal: ICSE
title: "Tensor-Aware Energy Accounting"
year: 2024
doi: 10.1145/3597503.3639156
abstract: "With the rapid growth of Artificial Intelligence (AI) applications supported by deep learning (DL), the energy efficiency of these applications has an increasingly large impact on sustainability. We introduce Smaragdine, a new energy accounting system for tensor-based DL programs implemented with TensorFlow. At the heart of Smaragdine is a novel white-box methodology of energy accounting: Smaragdine is aware of the internal structure of the DL program, which we call tensor-aware energy accounting. With Smaragdine, the energy consumption of a DL program can be broken down into units aligned with its logical hierarchical decomposition structure. We apply Smaragdine for understanding the energy behavior of BERT, one of the most widely used language models. Layer-by-layer and tensor-by-tensor, Smaragdine is capable of identifying the highest energy/power-consuming components of BERT. Furthermore, we conduct two case studies on how Smaragdine supports downstream toolchain building, one on the comparative energy impact of hyperparameter tuning of BERT, the other on the energy behavior evolution when BERT evolves to its next generation, ALBERT."
bibtex: |-
  @inproceedings{DBLP:conf/icse/BabakolL24,
    author       = {Timur Babakol and
                  Yu David Liu},
    title        = {Tensor-Aware Energy Accounting},
    booktitle    = {Proceedings of the 46th {IEEE/ACM} International Conference on Software
                  Engineering, {ICSE} 2024, Lisbon, Portugal, April 14-20, 2024},
    pages        = {93:1--93:12},
    publisher    = {{ACM}},
    year         = {2024},
    url          = {https://doi.org/10.1145/3597503.3639156},
    doi          = {10.1145/3597503.3639156},
    timestamp    = {Mon, 24 Jun 2024 15:20:25 +0200},
    biburl       = {https://dblp.org/rec/conf/icse/BabakolL24.bib},
    bibsource    = {dblp computer science bibliography, https://dblp.org}
  }
# image: "garciamartin-estimation.png"
tags:
  - Green Deep Learning
  - Energy monitoring
annotation: |-
  The paper presents *SMARAGDINE*, an energy accounting system for Deep Learning models built with TensorFlow. Opposite to other similar systems, which are black or grey box systems (only report total energy consumption or consumption by hardware device), *SMARAGDINE* can collect the energy and power used by the different logical components of the Neural Network. The network modules can be hierarchically measured, from layers to individual tensor operations.

  One of the challenges that this system must overcome is a *Semantic Gap*: mapping the energy measurements from the hardware devices into the logical units of the DL model. To solve this, the authors perform a trace-based alignment. The system collects traces from events that take place during the logical execution of the model, using TensorFlow API and callbacks, and traces from the power usage of the hardware devices, using Intel RAPL for CPU measurements and NVML for GPU measurements. An event trace refers to calls inside the TensorFlow session, and records the type of operation, starting time, duration, and the device where the operation runs, and it is collected when TensorFlow sends a callback. A power only contains a timestamp and power measured in that timestamp. These are recorded continuously in 4 ms intervals.

  After recording, both traces are aligned. For an event trace, the power traces collected during the duration of such event are aggregated and total energy and average power for the event are computed. The events with their corresponding energy can then be hierarchically organized in the different layers and elements of the model.

  The system is evaluated using BERT and its alternative ALBERT, one of the first transformer-based NLP models. The energy is measured for all stages of the model (pre-training, fine-tuning, and prediction). Their findings show that backward passes are the most energy-hungry and, inside the model, the self-attention layers account for most of the energy usage of the model. They also experiment with modifying hyperparameters, namely the number of transformer layers and the number of hidden embeddings. They find that, for BERT, the number of hidden embeddings is dominant in terms of power consumption. Increasing the number of hidden embeddings has a much greater effect on total energy usage than increasing the number of layers. Finally, in their comparison with ALBERT, they have the same findings in terms of relative energy usage, with self-atention layers using most of the energy, but ALBERT manages to use almost half the energy in some of its modules.
show-thoughts: false
---


