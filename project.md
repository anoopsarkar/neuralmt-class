---
layout: default
img: tensorflow
img_link: "https://www.tensorflow.org/"
caption: "Tensor Flow is a popular open source library for building RNNs (and other useful things)."
title: "Project"
active_tab: project
---

Final Project
-------------

The goal for each final project is a submission to a conference at the end of the semester (perhaps with some more work on the paper in the Spring semester).

## Software

### lamtram/cnn

[lamtram](https://github.com/neubig/lamtram): A toolkit for neural language and translation modeling

### Tensor Flow

https://www.tensorflow.org/

### nematus/Theano

[nematus](https://github.com/rsennrich/nematus) based on Kyunghun Cho's [dl4mt tutorial](https://github.com/nyu-dl/dl4mt-tutorial).

## Project Ideas

### Scaling to larger vocabulary size

* More scalable softmax computation.

### Different RNNs for NMT

* Stack RNN (equivalently LSTM) for NMT. Stack RNNs have been used for transition based dependency parsing. See Goldberg tutorial explanation of stack RNN.
* Use a multilingual corpus. Fix alignments using HMM aligner. Use alignments to train RNN. Extract paraphrases using multilingual RNN. (see papers by Callison-Burch and collaborators for extracting paraphases)

### Ensemble Models for NMT

* Explore different ways to create ensemble models for NMT

### Multilingual NMT

* Use word embeddings for low-resource languages. Improve performance on a language pair such as Haitian Kreyol to English where there is insufficient data for training a neural MT model.

### Complex reorderings in neural MT

* Go beyond the attention model to capture more complex reorderings and experiment on language pairs such as Chinese-English.
* Better attention models for complex reordering.

### Improve SGD

* Use SAG (Schmidt et al, 2015) to improve SGD for RNN-LM or NMT.

### Global sequence to sequence learning

Improve upon bidirectional RNNs by exploring global inference and complex non-differentiable loss functions such as BLEU scores. Currently the state of the art is to have a layer on top of a bidirectional sequence model which does global reordering.

An interesting first step might be to take the alignments learned by a (neural) HMM alignment model and use the entire distribution of alignments within a decoder.

### Decipherment using neural LMs

Can we improve on computational decipherment methods by using neural LMs and going beyond HMMs for scoring the cipher keys.
A more ambitious idea is to map images of text to language models bypassing the possibly error-prone human element in converting
the visual script to machine readable text. For instance, scans of the Voynich manuscript are available from the Yale library.
Can they be mapped to another language for which we have a language model.

### Brown clustering and RNNs

* Use Brown clusters to initialize word vectors for RNN-LM.
