[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/scibert-pretrained-contextualized-embeddings/named-entity-recognition-bc5cdr)](https://arxiv.org/pdf/2004.08795.pdf)  
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/scibert-pretrained-contextualized-embeddings/named-entity-recognition-bc5cdr)](https://github.com/maszhongming/MatchSum)  

# Extractive Summarization as Text Matching
### Authors: Ming Zhong et al. (Fudan University)

- Formulating the extractive summarization task as a semantic text matching problem.
- In "Semantic Text Matching", a source document and candidate summaries will be (extracted from the original text) matched in a semantic space.
- The prior work focused on extracting salient source sentences, unlike this work.

## Introduction
- Previous work are inherently sentence-level extractors, rather than considering semantics of summary-level sentences.
- Sentence-level extractors also suffer from redundancy issue between multiple sentences. Prior work have utilized some approaches such as Auto-regressive decoders and tri-gram blocking to overcome this issue.
-  This work propose a novel summary-level
framework (MATCHSUM, Figure 1) and conceptualize extractive summarization as a semantic text
matching problem.
- Principle idea: a good
summary should be more semantically similar as a
whole to the source document than the unqualified
summaries
- Siamese-BERT: a BERT architecture proposed to compute the
similarity between the source document and the
candidate summary.
- __Contributions:__
  - Instead of scoring and extracting sentences
one by one to form a summary, we formulate extractive summarization as a *semantic text matching* problem and propose a novel summary-level
framework.
  - We conduct an analysis to investigate whether
extractive models must do summary-level extraction based on the property of dataset, and attempt
to quantify the inherent gap between sentence-level
and summary-level methods.
  - Achieving SOTA on CNN/DailyMail.


## Method
  - 


## Results
  - The HAPN could achieve highest accuracies on two experimental datasets. 
  
    <p align="center"><img src="https://github.com/sajastu/papers-I-read/blob/master/EMNLP/pictures/HAPN-3.png" width="350"></p>
    
  - Hierachical Attention effect; Although "mother" and "child" class are similar to each other, but the HAPN model can effectively classify the query instance to "mother" class.
  <p align="center"><img src="https://github.com/sajastu/papers-I-read/blob/master/EMNLP/pictures/HAPN-1.png" width="550"></p>
 
- Same features extracted by feature-level attention (CNN) have different weights for different classes.
<p align="center"><img src="https://github.com/sajastu/papers-I-read/blob/master/EMNLP/pictures/HAPN-2.png" width="450"></p>
    
- Acurracy with increasing number of shots (instances):    
<p align="center"><img src="https://github.com/sajastu/papers-I-read/blob/master/EMNLP/pictures/HAPN-4.png" width="450"></p>

- Training convergence time:    
<p align="center"><img src="https://github.com/sajastu/papers-I-read/blob/master/EMNLP/pictures/HAPN-5.png" width="450"></p>
