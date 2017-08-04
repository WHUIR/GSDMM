# GSDMM
Our implementation of collapsed Gibbs Sampling algorithm for Dirichlet Multinomial Mixture model (GSDMM), as described in KDD 2014 paper:

**A Dirichlet Multinomial Mixture Model-based Approach for
Short Text Clustering**

The GSDMM is a short text clustering algorithm.

## Description

This repository doesn't contain the preprocess steps. So if you want to use this code, you should prepare the data by yourself. 

The data format is described as follows:
>word word word

Each line represents a document, the words in document are separated by a single blank space.

You also need to provide word2id file for launching the program, the data format is described as follows:
> word id

Each line represents a word , the word and its id is separated by a blank space

**example**:
> apple 0

## Parameter Explanation

`beta`: the hyper-parameter beta, and the alpha is calculated as 50/numTopic.

`numIter`: the number of iteration for gibbs sampling progress

## Model Result Explanation
`*_pdz.txt`: the topic-level representation for each document. Each line is a topic distribution for one document. This is used for classification task.

`*_phi.txt`: the word-level representation for each topic. Each line is a word distribution for one topic. This is used for PMI Coherence task.

`*_words.txt`: word, wordID map information.





