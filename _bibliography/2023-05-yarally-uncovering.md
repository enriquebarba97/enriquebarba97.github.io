---
author: Tim Yarally, Luís Cruz, Daniel Feitosa, June Sallou, and Arie van Deursen
journal: CAIN
title: "Uncovering Energy-Efficient Practices in Deep Learning Training: Preliminary Steps Towards Green AI"
year: 2023
doi: 10.1109/CAIN58948.2023.00012
abstract: "Modern AI practices all strive towards the same goal: better results. In the context of deep learning, the term \"results\" often refers to the achieved accuracy on a competitive problem set. In this paper, we adopt an idea from the emerging field of <span style=\"color:green\"> Green AI </span> to consider energy consumption as a metric of equal importance to accuracy and to reduce any irrelevant tasks or energy usage. We examine the training stage of the deep learning pipeline from a sustainability perspective, through the study of hyperparameter tuning strategies and the model complexity, two factors vastly impacting the overall pipeline’s energy consumption. First, we investigate the effectiveness of grid search, random search and Bayesian optimisation during hyperparameter tuning, and we find that Bayesian optimisation significantly dominates the other strategies. Furthermore, we analyse the architecture of convolutional neural networks with the energy consumption of three prominent layer types: convolutional, linear and ReLU layers. The results show that convolutional layers are the most computationally expensive by a strong margin. Additionally, we observe diminishing returns in accuracy for more energy-hungry models. The overall energy consumption of training can be halved by reducing the network complexity. In conclusion, we highlight innovative and promising energy-efficient practices for training deep learning models. To expand the application of <span style=\"color:green\">Green AI</span>, we advocate for a shift in the design of deep learning models, by considering the trade-off between energy efficiency and accuracy."
bibtex: |-
  @inproceedings{yarally2023uncovering,
    title={Uncovering energy-efficient practices in deep learning training: Preliminary steps towards green ai},
    author={Yarally, Tim and Cruz, Lu{\i}s and Feitosa, Daniel and Sallou, June and Van Deursen, Arie},
    booktitle={2023 IEEE/ACM 2nd International Conference on AI Engineering--Software Engineering for AI (CAIN)},
    pages={25--36},
    year={2023},
    organization={IEEE}
  }
# image: "garciamartin-estimation.png"
tags:
  - Deep Learning
  - Training optimization
annotation: |-
  The paper goes back to the drawing board and analyzes the optimization of Neural Networks not only from the point of view of getting maximum accuracy at any cost but also considering the energy demand of training. To do this, the authors choose the popular FashionMNIST and CIFAR-10 datasets, as well as popular CNN networks included in Pytorch. These have been extensively studied from an accuracy optimization perspective, but this paper is the first to consider the energy usage of the methods. Concretely, the paper focuses on the impact on accuracy and energy efficiency of 1. different hyperparameter optimization methods 2. architecture of the model, and the energy impact of the different types of layers.

  The paper experiments with three methods for hyperparameter optimization: grid search, random search, and Bayesian optimization. For each technique, three networks are trained (DensePolyNN, DenseLinearNN, and SimpleCNN) while optimizing for three or five hyperparameters. The techniques are run for 64 optimization rounds where, for each round, the network is trained and a new set of hyperparameters is determined using the optimization technique. The energy efficiency of each method is evaluated by how many optimization rounds it takes to converge to an optimal accuracy.

  The experiment shows that Bayesian optimization is the most efficient hyperparameter optimization method, taking an average of 27 rounds to reach optimum accuracy, except for a couple of outliers. However, for these outliers the improvement after round 27 is minimal. Comparing grid search and random search, there is no clear winner between the two, and both take longer than 27 rounds to reach optimum accuracy, with much larger jumps than Bayesian optimization after round 27.

  To measure the effect of network architecture on energy consumption, the second experiment tests the SimpleCNN model with different numbers of each type of layer: linear, convolutional, and ReLU layers. The results show that the convolutional layers have the most impact on energy consumption. When reducing the number of convolutional layers to one, the model manages to maintain the accuracy for FashionMNIST while using around 50% energy on average. For the CIFAR-10 dataset, given that it is a more complex dataset, this same setup obtains 6% less average accuracy, with a drop of 12% in maximum accuracy.

  The paper presents relevant new approaches to training neural networks with energy efficiency in mind. It does not introduce any relevant new concepts or more advanced models. Rather, the authors take proven and well-established models and datasets and provide new practices that consider accuracy and energy efficiency, which can be applied to more complex models.
show-thoughts: false
---