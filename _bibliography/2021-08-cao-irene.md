---
author: Qingqing Cao, Yash Kumar Lal, Harsh Trivedi, Aruna Balasubramanian, Niranjan Balasubramanian
journal: IJCNLP
title: "IrEne: Interpretable Energy Prediction for Transformers"
year: 2021
doi: 10.18653/v1/2021.acl-long.167
replication-package: https://github.com/StonyBrookNLP/irene
abstract: "Existing software-based energy measurements of NLP models are not accurate because they do not consider the complex interactions between energy consumption and model execution. We present IrEne, an interpretable and extensible energy prediction system that accurately predicts the inference energy consumption of a wide range of Transformer-based NLP models. IrEne constructs a model tree graph that breaks down the NLP model into modules that are further broken down into low-level machine learning (ML) primitives. IrEne predicts the inference energy consumption of the ML primitives as a function of generalizable features and fine-grained runtime resource usage. IrEne then aggregates these low-level predictions recursively to predict the energy of each module and finally of the entire model. Experiments across multiple Transformer models show IrEne predicts inference energy consumption of transformer models with an error of under 7% compared to the ground truth. In contrast, existing energy models see an error of over 50%. We also show how IrEne can be used to conduct energy bottleneck analysis and to easily evaluate the energy impact of different architectural choices. We release the code and data at https://github.com/StonyBrookNLP/irene."
bibtex: |-
  @inproceedings{DBLP:conf/acl/CaoLTBB20,
    author       = {Qingqing Cao and
                  Yash Kumar Lal and
                  Harsh Trivedi and
                  Aruna Balasubramanian and
                  Niranjan Balasubramanian},
    editor       = {Chengqing Zong and
                  Fei Xia and
                  Wenjie Li and
                  Roberto Navigli},
    title        = {IrEne: Interpretable Energy Prediction for Transformers},
    booktitle    = {Proceedings of the 59th Annual Meeting of the Association for Computational
                  Linguistics and the 11th International Joint Conference on Natural
                  Language Processing, {ACL/IJCNLP} 2021, (Volume 1: Long Papers), Virtual
                  Event, August 1-6, 2021},
    pages        = {2145--2157},
    publisher    = {Association for Computational Linguistics},
    year         = {2021},
    url          = {https://doi.org/10.18653/v1/2021.acl-long.167},
    doi          = {10.18653/V1/2021.ACL-LONG.167},
    timestamp    = {Mon, 09 Aug 2021 16:25:37 +0200},
    biburl       = {https://dblp.org/rec/conf/acl/CaoLTBB20.bib},
    bibsource    = {dblp computer science bibliography, https://dblp.org}
    }

# image: "garciamartin-estimation.png"
tags:
  - Transformer Models
  - Energy prediction
annotation: |-
  The paper proposes a model to estimate the energy consumption of Transformer-based NLP models. They achieve this by abstracting the model into a tree, dividing its components into modules (e.g. BertSelfAttention), which can be composed by other submodules, Machine Learning primitives (e.g. LayerNorm), and these are formed by math operations (e.g matrix multiplication). 

  The model is run once using just-in-time (JIT) instrumentation to build the tree using Pytorch API and extract relevant features from each of the nodes. These features are hardware-independent, like batch-size or floating point operations, and hardware-dependent, like GPU clock speed or GPU driver energy. Regression models are trained for each of the leaves of the tree using these features, and the estimation for parent nodes is computed bottom-up, using a weighted sum that is learned using node features.
show-thoughts: false
---