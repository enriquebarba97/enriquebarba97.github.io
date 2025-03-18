---
author: Yue Wang, Ziyu Jiang, Xiaohan Chen, Pengfei Xu, Yang Zhao, Yingyan Lin, Zhangyang Wang
journal: "NIPS"
title: "E2-Train: Training State-of-the-art CNNs with Over 80% Energy Savings"
year: 2019
full-text: https://proceedings.neurips.cc/paper_files/paper/2019/file/663772ea088360f95bac3dc7ffb841be-Paper.pdf
doi: 10.48550/arXiv.1910.13349
replication-package: https://github.com/GATECH-EIC/E2Train
abstract: "Convolutional neural networks (CNNs) have been increasingly deployed to edge devices. Hence, many efforts have been made towards efficient CNN inference on resource-constrained platforms. This paper attempts to explore an orthogonal direction: how to conduct more energy-efficient training of CNNs, so as to enable on-device training? We strive to reduce the energy cost during training, by dropping unnecessary computations, from three complementary levels: stochastic mini-batch dropping on the data level; selective layer update on the model level; and sign prediction for low-cost, low-precision back-propagation, on the algorithm level. Extensive simulations and ablation studies, with real energy measurements from an FPGA board, confirm the superiority of our proposed strategies and demonstrate remarkable energy savings for training. For example, when training ResNet-74 on CIFAR-10, we achieve aggressive energy savings of >90% and >60%, while incurring a top-1 accuracy loss of only about 2% and 1.2%, respectively. When training ResNet-110 on CIFAR-100, an over 84% training energy saving is achieved without degrading inference accuracy."
bibtex: |-
  @inproceedings{DBLP:conf/nips/WangJC0ZLW19,
  author       = {Yue Wang and
                  Ziyu Jiang and
                  Xiaohan Chen and
                  Pengfei Xu and
                  Yang Zhao and
                  Yingyan Lin and
                  Zhangyang Wang},
  editor       = {Hanna M. Wallach and
                  Hugo Larochelle and
                  Alina Beygelzimer and
                  Florence d'Alch{\'{e}}{-}Buc and
                  Emily B. Fox and
                  Roman Garnett},
  title        = {E2-Train: Training State-of-the-art CNNs with Over 80{\%} Energy Savings},
  booktitle    = {Advances in Neural Information Processing Systems 32: Annual Conference
                  on Neural Information Processing Systems 2019, NeurIPS 2019, December
                  8-14, 2019, Vancouver, BC, Canada},
  pages        = {5139--5151},
  year         = {2019},
  url          = {https://proceedings.neurips.cc/paper/2019/hash/663772ea088360f95bac3dc7ffb841be-Abstract.html},
  timestamp    = {Mon, 16 May 2022 15:41:51 +0200},
  biburl       = {https://dblp.org/rec/conf/nips/WangJC0ZLW19.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
  }
# image: "garciamartin-estimation.png"
tags:
  - Training Efficiency
  - Edge AI
annotation: |-
  This paper presents three techniques to improve the energy efficiency of training Convolutional Neural Networks in edge devices by dropping and reducing unnecessary computations during the training phase. They propose 3 techniques at different levels: data, model, and algorithm, and manage to obtain a reduction of up to 80% in energy usage with minimal.

  At the data level, the authors propose a surprisingly simple strategy called Stochastic mini-batch dropping or SMD. This strategy effectively reduces the training set to half, by skipping a mini-batch with a 0.5 probability. This technique effectively reduces training computation cost by half, and according to their results, comes to a negligible cost in accuracy, sometimes even slightly improving it.

  At the model level, the paper introduces a technique called Input-dependent Selective Layer Update (SLU). This technique introduces a gating mechanism with a small RNN for each of the layers. This gate receives the same input as its corresponding CNN layer and outputs a probability of skipping such layer. These gates are trained together with the CNN model, and learn which inputs are more valuable for their respective layers. These gates are sufficiently small and cost less than 0.04% operations than the base model, so their consumption is negligible.

  Finally, the paper introduces a modified algorithm to reduce the computing costs of the gradient called Predictive Sign Gradient Descent. For this, instead of computing the full gradient to backpropagate to the weights, the algorithm predicts the sign of the gradient with low-precision computations and propagates only this sign to update the weights. If the predictors are built with proper precision, the method is very likely to predict the correct sign.

  They evaluate these 3 methods with the CIFAR-10 and CIFAR-100 datasets and on the ResNet-110 and MobileNetV2 models. To make the scenario more realistic, they run the evaluation on an FPGA board. The paper reports energy savings between 46% to 93%, with very small accuracy drops (0.56% to 2%). However, the paper does not report total energy numbers or total training times, both of which are relevant for low-powered edge devices.
show-thoughts: false
---