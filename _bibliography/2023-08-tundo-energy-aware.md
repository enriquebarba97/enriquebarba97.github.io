---
author: Alessandro Tundo, Marco Mobilio, Shashikant Ilager, Ivona Brandić, Ezio Bartocci, Leonardo Mariani
journal: ASE
title: "An Energy-Aware Approach to Design Self-Adaptive AI-based Applications on the Edge"
year: 2023
doi: 10.1109/ASE56229.2023.00046
abstract: "The advent of edge devices dedicated to machine learning tasks enabled the execution of AI-based applications that efficiently process and classify the data acquired by the resource-constrained devices populating the Internet of Things. The proliferation of such applications (e.g., critical monitoring in smart cities) demands new strategies to make these systems also sustainable from an energetic point of view. In this paper, we present an energy-aware approach for the design and deployment of self-adaptive AI-based applications that can balance application objectives (e.g., accuracy in object detection and frames processing rate) with energy consumption. We address the problem of determining the set of configurations that can be used to self-adapt the system with a meta-heuristic search procedure that only needs a small number of empirical samples. The final set of configurations are selected using weighted gray relational analysis, and mapped to the operation modes of the self-adaptive application. We validate our approach on an AI-based application for pedestrian detection. Results show that our self-adaptive application can outperform non-adaptive baseline configurations by saving up to 81% of energy while loosing only between 2% and 6 % in accuracy."
bibtex: |-
  @inproceedings{tundo2023energy,
    title={An Energy-Aware Approach to Design Self-Adaptive AI-based Applications on the Edge},
    author={Tundo, Alessandro and Mobilio, Marco and Ilager, Shashikant and Brandi{\'c}, Ivona and Bartocci, Ezio and Mariani, Leonardo},
    booktitle={2023 38th IEEE/ACM International Conference on Automated Software Engineering (ASE)},
    pages={281--293},
    year={2023},
    organization={IEEE}
  }
# image: "garciamartin-estimation.png"
tags:
  - Deep Learning
  - Adaptative configuration
  - Operation modes
annotation: |-
  The paper proposes a new framework for developing Energy-Aware Self-Adaptative AI applications. These applications can dynamically switch between different sets of configurations based on perceived conditions to prioritize different objectives, like switching from a low-energy, low-accuracy mode to a high-energy high-accuracy mode depending on the current circumstances. The authors use a pedestrian detection scenario to exemplify and evaluate the framework, that tries to balance energy usage, accuracy, and frame processing rate.

  The framework starts by defining a State-Based Adaptation Logic for the scenario in the form of a Finite State Machine defined by an engineer, which includes the different operation modes with the desirable characteristics. For their scenario, the authors define four states: power-saving, low-energy, high-energy, and high-rate, with transitions depending on the number of pedestrians detected.

  To determine the specific objectives for each of the states, and the configurations that optimize these objectives, the next step in the framework is to solve a Multi-Objective Optimization Problem. For the pedestrian scenario, the objectives are minimizing energy usage and maximizing accuracy and framerate. The parameters for the search space are the camera resolution, frame rate, object detection model, detection threshold, and usage of a hardware accelerator. The NSGA-II algorithm is used to find a Pareto front with the most optimal trade-offs, which can find optimal solutions without the need for an exhaustive search. 

  The parameters that reach these optimal solutions are extracted using a weighted gray relational analysis. Here, a weight is assigned to each of the objectives for each of the desired operation modes, giving them more or less importance, as well as a set of thresholds to guarantee a minimum desired performance. This algorithm yields the specific configuration values to be applied in each of the states.

  For the evaluation of the framework, the authors deploy the model designed for the pedestrian scenario into a Raspberry Pi with a camera and an external hardware accelerator. They compare the performance of the different objectives to four non-adaptative applications, with configuration fixed to each of the four states. The results show that the adaptative application outperforms three out of four non-adaptative applications in terms of energy consumption and frame processing rate. For accuracy, it only outperforms the non-adaptative power saving application, but the difference in accuracy with the other three is minimal, with an accuracy loss from 2% to 6%.
show-thoughts: false
---