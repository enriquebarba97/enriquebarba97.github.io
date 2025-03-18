---
author: Stefanos Georgiou, Maria Kechagia, Tushar Sharma, Federica Sarro, Ying Zou
journal: ICSE
title: "Green AI: do deep learning frameworks have different costs?"
year: 2022
doi: 10.1145/3510003.3510221
abstract: "The use of Artificial Intelligence (ai), and more specifically of Deep Learning (dl), in modern software systems, is nowadays widespread and continues to grow. At the same time, its usage is energy demanding and contributes to the increased CO2 emissions, and has a great financial cost as well. Even though there are many studies that examine the capabilities of dl, only a few focus on its green aspects, such as energy consumption.
This paper aims at raising awareness of the costs incurred when using different dl frameworks. To this end, we perform a thorough empirical study to measure and compare the energy consumption and run-time performance of six different dl models written in the two most popular dl frameworks, namely PyTorch and TensorFlow. We use a well-known benchmark of dl models, DeepLearningExamples, created by nvidia, to compare both the training and inference costs of dl. Finally, we manually investigate the functions of these frameworks that took most of the time to execute in our experiments.
The results of our empirical study reveal that there is a statistically significant difference between the cost incurred by the two dl frameworks in 94% of the cases studied. While TensorFlow achieves significantly better energy and run-time performance than PyTorch, and with large effect sizes in 100% of the cases for the training phase, PyTorch instead exhibits significantly better energy and run-time performance than TensorFlow in the inference phase for 66% of the cases, always, with large effect sizes. Such a large difference in performance costs does not, however, seem to affect the accuracy of the models produced, as both frameworks achieve comparable scores under the same configurations. Our manual analysis, of the documentation and source code of the functions examined, reveals that such a difference in performance costs is under-documented, in these frameworks. This suggests that developers need to improve the documentation of their dl frameworks, the source code of the functions used in these frameworks, as well as to enhance existing dl algorithms."
bibtex: |-
  @inproceedings{10.1145/3510003.3510221,
    author = {Georgiou, Stefanos and Kechagia, Maria and Sharma, Tushar and Sarro, Federica and Zou, Ying},
    title = {Green AI: do deep learning frameworks have different costs?},
    year = {2022},
    isbn = {9781450392211},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3510003.3510221},
    doi = {10.1145/3510003.3510221},
    booktitle = {Proceedings of the 44th International Conference on Software Engineering},
    pages = {1082–1094},
    numpages = {13},
    keywords = {APIs, deep learning, energy consumption, run-time performance},
    location = {Pittsburgh, Pennsylvania},
    series = {ICSE '22}
  }
# image: "garciamartin-estimation.png"
tags:
  - DL frameworks
  - Energy monitoring
annotation: |-
  The main contribution of the paper is to compare the energy efficiency of TensorFlow and PyTorch, two popular Python frameworks for Deep Learning. To do so, the authors run multiple benchmarks on both frameworks using the `DeepLearningExamples` collection from NVIDIA, which includes multiple models implemented in both frameworks. They select different models that cover the tasks of Recommender Systems, Natural Language Processing, and Computer Vision.

  The experiments are run using an execution framework that guarantees the validity of the results and facilitates reproducibility. The framework sets up the environment automatically and runs the experiments multiple times, measuring the accuracy and energy consumption (using Intel RAPL and NVIDIA SMI) of the models for both DL frameworks. With these experiments, the paper aims to answer which framework is more energy efficient, and more accurate and which parts of their API are less runtime efficient.

  In terms of accuracy, both frameworks obtain comparable results, and there is not a large significant difference. In terms of energy efficiency, the results obtained are very varied. In the training phase, TensorFlow is more efficient than PyTorch in training a model for Recommender Systems, being 2.1x faster and 1.5x more energy efficient. A similar trend is observed in the Computer Vision models, being 1.2x, 1.1x, and 3.1x more energy efficient for the three models tested. For NLP PyTorch outperforms TensorFlow, using 1.5x and 2.8x less energy for the transformer-based models tested. However, these results do not translate to inference, where PyTorch outperforms TensorFlow for all but two models. These results make it hard to extrapolate general recommendations for developers.

  To investigate the runtime performance of the different parts of the API, the authors use `cprofile` to trace the number of calls to the different functions in the framework, as well as their runtime. They find that, in most cases, there is a single specific function in both frameworks that takes the majority of the training runtime (`autograd.backward` for PyTorch and `Session.run` for TensorFlow). These are interesting results since they can lead the developers of both frameworks to possible points of improvement. The same execution and tracing framework proposed can even be applied to other frameworks and models to study their performance.
show-thoughts: false
---