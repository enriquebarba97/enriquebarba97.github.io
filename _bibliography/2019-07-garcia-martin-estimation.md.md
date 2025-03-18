---
author: Eva García-Martín, Crefeda Faviola Rodrigues, Graham Riley, Håkan Grahn
journal: Journal of Parallel and Distributed Computing
title: "Estimation of energy consumption in machine learning"
year: 2019
doi: 10.1016/j.jpdc.2019.07.007
abstract: "Energy consumption has been widely studied in the computer architecture field for decades. While the adoption of energy as a metric in machine learning is emerging, the majority of research is still primarily focused on obtaining high levels of accuracy without any computational constraint. We believe that one of the reasons for this lack of interest is due to their lack of familiarity with approaches to evaluate energy consumption. To address this challenge, we present a review of the different approaches to estimate energy consumption in general and machine learning applications in particular. Our goal is to provide useful guidelines to the machine learning community giving them the fundamental knowledge to use and build specific energy estimation methods for machine learning algorithms. We also present the latest software tools that give energy estimation values, together with two use cases that enhance the study of energy consumption in machine learning."
bibtex: |-
  @article{garcia2019estimation,
    title={Estimation of energy consumption in machine learning},
    author={Garc{\'\i}a-Mart{\'\i}n, Eva and Rodrigues, Crefeda Faviola and Riley, Graham and Grahn, H{\aa}kan},
    journal={Journal of Parallel and Distributed Computing},
    volume={134},
    pages={75--88},
    year={2019},
    publisher={Elsevier}
  }
# image: "garciamartin-estimation.png"
tags:
  - ML Energy Estimation
  - Literature Review
annotation: |-
  The paper does an extensive literature review of the different techniques for estimating energy consumption in machine learning and deep learning software. It starts by reviewing existing energy usage estimation methods for general software: from software-level estimation with performance counters, simulation, or instruction-level estimation to hardware-level measurements. It also presents existing tools for measuring energy usage, like Intel RAPL or ARM Streamline.

  Next, they present how some of the previous techniques are being applied to the domain of machine learning. Most of these models focus on measuring different metrics from the neural network, from higher-level parameters, like the number of weights or layers in the network, to more fine-grained metrics, like the number of matrix multiplication operations or memory access count. The different metrics can be benchmarked to obtain the approximate energy used, and total energy is obtained by applying regression to the metrics collected.

  Finally, the paper presents two use cases. The first use case measures the difference in accuracy and energy consumption of concept drift, using RAPL through Intel Power Gadget. They compare VFDT, which cannot handle concept drift, and HAT, which can detect and compensate for it. They test both algorithms using two datasets, one without concept drift and another without concept drift. They find that HAT uses 11% more energy and obtains ~10% more accuracy in the concept drift dataset. However, HATdoes not present significant accuracy improvements over VFDT for the concept drift-free dataset, while keeping the same difference in energy usage.

  The second use case uses the SyNERGY approach to predict the energy usage of three different architectures of convolutional neural networks, MobileNet, Inception-v3, and DenseNet, with the first being more energy efficient. The SyNERGY approach prediction understimated the real energy consumption, with a relative accuracy of ~69%, but it correctly predicted the most efficient model.
show-thoughts: false
---