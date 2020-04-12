[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/scibert-pretrained-contextualized-embeddings/named-entity-recognition-bc5cdr)](https://arxiv.org/pdf/1805.11080.pdf)  
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/scibert-pretrained-contextualized-embeddings/named-entity-recognition-bc5cdr)](https://github.com/ChenRocks/fast_abs_rl)  

# Fast Abstractive Summarization with Reinforce-Selected Sentence Rewriting (ACL, 2018)
### Authors: Yen-Chun Chen and Mohit Bansal (UNC Chapel Hill)
- an accurate and
fast summarization model that first selects
salient sentences and then rewrites them
abstractively (i.e., compresses and paraphrases) to generate a concise overall summary
- achieving the new state-of-theart on all metrics (including human evaluation) on the CNN/Daily Mail dataset, as
well as significantly higher abstractiveness
scores
- by first operating at
the sentence-level and then the word-level,
we enable parallel decoding of our neural
generative model that results in substantially faster (10-20x) inference speed as
well as 4x faster training convergence than
previous long-paragraph encoder-decoder
models.
- also demonstrate the generalization of our model on the test-only DUC2002 dataset, where we achieve higher
scores than a state-of-the-art model

## Introduction
  - Abstractive models can be more concise
by performing generation from scratch, but they
suffer from slow and inaccurate encoding of very
long documents
  -  Abstractive models also suffer from redundancy (repetitions), especially when generating multi-sentence
summary.
  - To address both these issues and combine
the advantages of both paradigms, we propose a hybrid extractive-abstractive architecture,
with policy-based reinforcement learning (RL) to
bridge together the two networks.
  - Similar to how
humans summarize long documents, our model
first uses an extractor agent to select salient sentences or highlights, and then employs an abstractor network to rewrite (i.e., compress and paraphrase) each of these extracted sentences.
  - extractor
combines reinforcement learning and pointer networks, 
  - abstractor is a simple encoder-aligner-decoder model (with copying) and is trained on pseudo
document-summary sentence pairs obtained via
simple automatic matching criteria
  - This also avoids almost all redundancy issues because the model has already chosen non-redundant salient sentences to abstractively summarize
   - __*Contributions*__
     1.  we propose a novel sentence-level RL technique
for the well-known task of abstractive summarization, effectively utilizing the word-then-sentence
hierarchical structure without annotated matching sentence-pairs between the document and ground
truth summary.
      2. our model achieves the
new state-of-the-art on all metrics of multiple versions of a popular summarization dataset (as well
as a test-only dataset) both extractively and abstractively, without loss in language fluency (also
demonstrated via human evaluation and abstractiveness scores).
      3. our parallel decoding results in a significant 10-20x speed-up over the previous best neural abstractive summarization system with even better accuracy

## Model

-  Our overall model
consists of these two submodules, the extractor
agent and the abstractor network
- *Extractor Agent*: can be thought of as extracting salient sentences
from the document.
- a hierarchical neural model to learn the sentence representations of
the document and a ‘selection network’ to extract
sentences based on their representations.
- 
