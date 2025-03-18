---
author: Mohit Kumar, Xingzhou Zhang, Liangkai Liu, Yifan Wang, Weisong Shi
journal: IPDPSW
title: "Energy-Efficient Machine Learning on the Edges"
year: 2020
doi: 10.1109/IPDPSW50202.2020.00153
replication-package: https://github.com/mohitkumar14/JEPO
abstract: "Machine learning-based software is vital for future Internet of Things (IoT) applications and Connected and Autonomous Vehicles (CAVs) as it provides the core value of these services by leveraging the enormous amount of data collected on the edge. These services utilize various machine learning models which make it computationally intensive on the edges. There has been a lot of work to make the hardware efficient. No matter how efficient is the hardware, an inefficient machine learning model can account for high energy consumption and overheating problem. However, there are very few tools available that can help software developers or researchers to make the machine learning models energy efficient.Our main contributions of this paper are two-fold: First, we summarize the state-of-the-art techniques about energy-efficient machine learning on the edges. Second, targeting specific Java programming language, we present an Eclipse plugin named Java Energy Profiler & Optimizer (JEPO) which can help in profiling and optimizing machine learning source code written in Java. JEPO can automatically measure the energy consumption of source code at method granularity. It provides energy efficiency suggestions for data types, operators, control statements, String, exception, objects, and Arrays in Java. JEPO evaluation has shown up to 14.46% improvement in energy consumption when used to optimize the machine learning software WEKA with only 0.48% drop in accuracy."
bibtex: |-
  @inproceedings{9150337,
    author={Kumar, Mohit and Zhang, Xingzhou and Liu, Liangkai and Wang, Yifan and Shi, Weisong},
    booktitle={2020 IEEE International Parallel and Distributed Processing Symposium Workshops (IPDPSW)}, 
    title={Energy-Efficient Machine Learning on the Edges}, 
    year={2020},
    volume={},
    number={},
    pages={912-921},
    keywords={Software;Machine learning;Hardware;Energy consumption;Image edge detection;Java;Machine learning algorithms;CAVs;IoT;Software;Java;Energy-Efficiency;Eclipse Plugin},
    doi={10.1109/IPDPSW50202.2020.00153}
  }
# image: "garciamartin-estimation.png"
tags:
  - Energy efficiency
  - Code suggestions
annotation: |-
  An Eclipse plugin that offers code suggestions to improve the energy efficiency of machine learning code in Java. Although the paper presents the tool and suggestions in the context of machine learning, the rules target built-in Java functionality, like the best primitive types or best methods to copy or compare arrays. Additionally, the plugin can instrument the code to obtain energy measurements using Intel RAPL. However, it does not specify the OS or architectures supported by this feature.

  The plugin is evaluated using the Machine Learning library WEKA, by modifying its source code according to the plugin's suggestions. For different algorithms, the evaluation is run 10 times, and outliers are replaced by new measurements.

  The evaluation shows an improvement of up to 14.46% in energy consumption. However, this number is for the Random Forest algorithm, and the rest of the algorithms see much smaller improvements, with an average improvement of 4.6%.

  Some of the suggestions involve changing primitive types (*double* to *float* or *long* to *int*) which can affect model accuracy. According to the evaluation, the accuracy lost is only 0.48% in the worst case, but it could be worse for other untested models. However, since the suggestions provided by the plugin focus on general Java functionality, they could be applied to other types of software, not only machine learning. Therefore the plugin could shine in other applications, where precision is not as important.
thoughts: |-
  I find this kind of code companion tool the the most interesting approach to improving the sustainability of AI, even if this implementation can be improved in certain areas. In general, I think most developers are unaware of the energy impact of the different decisions they make. A tool that pops up code suggestions or general information about the library methods being used can be useful during the development cycle, where there is more flexibility for changes in design.

  In a similar way, a catalog of recommendations would be useful for the AI developer starting a project. Do you want to do image classification? These are the algorithms that showed the best energy performance compared to accuracy, and these data types give enough precision.
show-thoughts: true
---