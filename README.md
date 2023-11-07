<!-- TOC -->
* [SRoBERTa: An enhanced Siamese RoBERTa-Networks for Semantic Textual Similarity](#sroberta-an-enhanced-siamese-roberta-networks-for-semantic-textual-similarity)
  * [Introduction](#introduction)
  * [Installation](#installation)
  * [Semantic Textual Similarity](#semantic-textual-similarity)
    * [Pretrained-models](#pretrained-models)
<!-- TOC -->

# SRoBERTa: An enhanced Siamese RoBERTa-Networks for Semantic Textual Similarity

## Introduction
The final project of the Statistical Machine Learning subject for Graduate Course

This framework provides an easy method to compute dense vector representations for **sentences** apply for Semantic Similarity task. 
The models are based on transformer networks RoBERTa and achieve effective performance.
Text is embedded in vector space such that similar text are closer and can efficiently be found using cosine similarity.

The following publications are integrated in this framework:

- [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084) (EMNLP 2019)
- [Making Monolingual Sentence Embeddings Multilingual using Knowledge Distillation](https://arxiv.org/abs/2004.09813) (EMNLP 2020)
- [Augmented SBERT: Data Augmentation Method for Improving Bi-Encoders for Pairwise Sentence Scoring Tasks](https://arxiv.org/abs/2010.08240) (NAACL 2021)
- [The Curse of Dense Low-Dimensional Information Retrieval for Large Index Sizes](https://arxiv.org/abs/2012.14210) (arXiv 2020)
- [TSDAE: Using Transformer-based Sequential Denoising Auto-Encoder for Unsupervised Sentence Embedding Learning](https://arxiv.org/abs/2104.06979) (arXiv 2021)
- [BEIR: A Heterogenous Benchmark for Zero-shot Evaluation of Information Retrieval Models](https://arxiv.org/abs/2104.08663) (arXiv 2021)

## Installation


**Install with pip**

Install the *sentence-transformers* with `pip`:

```
pip install -U sentence-transformers
```

**Install with conda**

You can install the *sentence-transformers* with `conda`:

```
conda install -c conda-forge sentence-transformers
```

## Semantic Textual Similarity

Semantic Textual Similarity (STS) assigns a score on the similarity of two texts. In this work, we use the [STSbenchmark](https://ixa2.si.ehu.es/stswiki/index.php/STSbenchmark) as training data to fine-tune our network.

### Pretrained-models
- **[training_stsbenchmark.py](training_stsbenchmark.py)** - Create a SentenceTransformer model from scratch by using a pre-trained transformer model together with a pooling layer.
- **[training_stsbenchmark_continue_training.py](training_stsbenchmark_continue_training.py)** - Continue training on STS data for a previously created & trained SentenceTransformer model. Load a model trained on [NLI data](../nli/README.md).
