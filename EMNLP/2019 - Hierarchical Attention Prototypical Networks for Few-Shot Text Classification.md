[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/scibert-pretrained-contextualized-embeddings/named-entity-recognition-bc5cdr)](https://www.aclweb.org/anthology/D19-1045.pdf)  
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/scibert-pretrained-contextualized-embeddings/named-entity-recognition-bc5cdr)](https://github.com/ChenRocks/fast_abs_rl)  

# Hierarchical Attention Prototypical Networks for Few-Shot Text Classification (EMNLP, 2019)
### Authors: Shengli Sun, Qingfeng Sun, Kevin Zhou, Tengchao Lv (Peking University, Microsoft)

- Supervised training data are few and difficult to be collected, and thus most of current classification models are not working well as they require a large amount of data.
- Proposing a hierarchical attention prototypical networks (HAPN) for few-shot text classification.
-  Designing the feature level, word level, and instance level multi cross attention for our model to enhance the expressive ability of semantic space.
- Evaluating on fewshot text classification datasets - FewRel and CSID, and achieve the state-of-the-art performance. 
- Visualization of hierarchical attention layers illustrates that our model can capture more important features, words, and instances separately.


## Introduction
- Few-shot learning has became an effective approach to solve
this challenge (low-resource setting), it can train a neural network with a
few parameters using few data but achieve good
performance.
- Prototypical networks (Snell et al., 2017), which
averages the vector of few support instances as the
class prototype and computes distance between
target query and each prototype, then classify the
query to the nearest prototype’s class
- Proposing a three-level hierachical attentive prototypical network for few-shot text classificaiton:
  - (1) *Feature-level attention:* CNNs to capture feature scores which differs for each class.
  - (2) *Word-level attention:* Using an attention mechanism for each word's hidden representation to learn their importance within an instance.
  - (3) *Instance-level multi cross attention:* with the help of multi cross attention between
support set and target query, the instance importance can be deterimind within a class. 
- __Contributions__
  - Proposing a hierarchical attention prototypical networks for few-shot text classification.
  - Achieving state-of-the-art performance on
FewRel and CSID datasets.
  - Faster and more extensible models.
  
## Method
- 
