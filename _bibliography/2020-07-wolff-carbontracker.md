---
author: Lasse F. Wolff Anthony, Benjamin Kanding, Raghavendra Selvan
journal: Arxiv
title: "Carbontracker: Tracking and Predicting the Carbon Footprint of Training Deep Learning Models"
year: 2020
doi: 10.48550/arXiv.2007.03051
preprint: https://arxiv.org/abs/2007.03051
replication-package: https://github.com/lfwa/carbontracker
abstract: "Deep learning (DL) can achieve impressive results across a wide variety of tasks, but this often comes at the cost of training models for extensive periods on specialized hardware accelerators. This energy-intensive workload has seen immense growth in recent years. Machine learning (ML) may become a significant contributor to climate change if this exponential trend continues. If practitioners are aware of their energy and carbon footprint, then they may actively take steps to reduce it whenever possible. In this work, we present Carbontracker, a tool for tracking and predicting the energy and carbon footprint of training DL models. We propose that energy and carbon footprint of model development and training is reported alongside performance metrics using tools like Carbontracker. We hope this will promote responsible computing in ML and encourage research into energy-efficient deep neural networks."
bibtex: |-
  @article{DBLP:journals/corr/abs-2007-03051,
    author       = {Lasse F. Wolff Anthony and
                  Benjamin Kanding and
                  Raghavendra Selvan},
    title        = {Carbontracker: Tracking and Predicting the Carbon Footprint of Training
                  Deep Learning Models},
    journal      = {CoRR},
    volume       = {abs/2007.03051},
    year         = {2020},
    url          = {https://arxiv.org/abs/2007.03051},
    eprinttype    = {arXiv},
    eprint       = {2007.03051},
    timestamp    = {Sat, 23 Jan 2021 01:11:16 +0100},
    biburl       = {https://dblp.org/rec/journals/corr/abs-2007-03051.bib},
    bibsource    = {dblp computer science bibliography, https://dblp.org}
  }
# image: "garciamartin-estimation.png"
tags:
  - Deep Learning
  - Carbon emissions
annotation: |-
  The paper introduces an open-source tool to measure and predict the energy usage and carbon emissions of training a neural network. To do so, the tool measures energy consumption for a small number of epochs using Intel RAPL to measure CPU and DRAM power usage and NVIDIA Management Library to measure GPU power usage. It reports a prediction on energy usage by extrapolating to the total number of epochs, and an estimation of carbon emissions by consulting regional Carbon Intensity through an API.

  The paper also provides some suggestions for reducing the carbon footprint of training a model. For example, the model can be trained during hours when the region has a lower Carbon Intensity, or in regions with a lower Carbon Intensity overall. The authors also suggest using efficient algorithms and efficient hardware settings.
thoughts: |-
  The paper provides a useful tool for machine learning developers to gauge the carbon impact of their model. However, I find limiting the impact of Machine Learning on carbon emissions a bit reductionistic. For example, the suggestion of running the training in regions with low Carbon Intensity would not scale properly. The power that renewable energy can provide is limited. If everyone decides to move their training to specific regions with lower carbon emissions, data centers might not be able to support the increased load. I think this tool is useful to increase awareness of the energy impact of Machine Learning but the main focus should be on improving efficiency in terms of power and energy, which should end up reducing carbon emissions too.
show-thoughts: true
---