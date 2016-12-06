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

<p class="text-muted">Due on December 15, 2016</p>

The goal for each final project is a submission to a conference at the end of the semester (perhaps with some more work on the paper in the Spring semester).

* You must turn in two things:
  1. A write-up that explains what you accomplished in your course project. It should be written in a clear, scientific style and contain enough information for another student to replicate your results. More information about the write-up is given below.
  1. Your code. The code should be self-contained, self-documenting, and easy to use. Please include a detailed description of how to run your code.
* Each group should assign one member to upload the write-up and source code to [Coursys](https://courses.cs.sfu.ca) as a single tarball or zip files as the submission for Final Project. 

### Write-up

Your write-up is the most important part of your project. It **must** have the following sections:

* Motivation 
    * Which aspect of the translation system did your group choose to improve and reasons for your choice.
* Approach 
    * Describe the algorithms and machine learning models used in your project. Use a clear mathematical style to explain your model(s).
* Data 
    * Exactly which data files were used; also include here any external data that was not provided to you.
* Code
    * Describe which homework code you used in your project. Provide exactly which code was used in your project not written by your group (e.g. use of an aligner from an open-source project).
* Experimental Setup
    * Describe what kind of evaluation you are doing and which methods you are comparing against each other.
* Results 
    * Include a detailed comparison of different methods.
* Analysis of the Results
    * Did you improve over the baseline. Why or why not?
* Future Work
    * What could be fixed in your approach. What you did not have time to finish, but you think would be a useful addition to your project.

## Submission Format

For your write-up, you can use plain ASCII but for math equations
and tables it is better to use either
[latex](http://www.latex-project.org/) or
[kramdown](https://github.com/gettalong/kramdown).  Do __not__ use
any proprietary or binary file formats such as Microsoft Word.

If you use latex then use the following style files:

* [acl2012.sty]({{ site.baseurl }}/assets/project/acl2012.sty)
* [acl2012.bst]({{ site.baseurl }}/assets/project/acl2012.bst)

Here is an example of using these style files:

* [Example latex file]({{ site.baseurl }}/assets/project/project.tex)
* [project.bib]({{ site.baseurl }}/assets/project/project.bib)

To get a PDF file you should run the following commands (which assume you have installed LaTeX on your system):

    pdflatex project
    bibtex project
    pdflatex project
    pdflatex project

You can then open `project.pdf` using any PDF viewer. Please submit
the LaTeX source and the PDF file along with your source code when
you submit your project to Coursys.

## Grading system

The final projects will be graded using the following criteria:

* Originality 
* Substance (amount of work done for the project)
* Well documented use of prior results from research papers
* Clarity of the writing
* Quality of experimental design
* Quality of evaluation and results
* (Re)Use of existing homework code
* Overall score (based on the above criteria)

## Examples

Here are some examples of good project submissions. They are both published papers but give you a good idea of 
how to write your project report. You can take inspiration for how to write a polished report from these
examples but make sure you have the sections required by the Write-up section above.

* [Example 1 by David Chiang and Steve DeNeefe and Michael Pust]({{ site.baseurl }}/assets/project/P11-2080.pdf)
* [Example 2 by Dong Song and Anoop Sarkar]({{ site.baseurl }}/assets/project/sighan08.pdf)

## Data

* [NLP class data](http://anoopsarkar.github.io/nlp-class/project.html) from Anoop Sarkar's NLP class.
* [WMT 2015 data](http://www.statmt.org/wmt15/) from the Workshop on MT 2015 Shared Task on Translation.
* [CSLM Paper Data](http://www-lium.univ-lemans.fr/~schwenk/cslm_joint_paper/) by Holger Schwenk.

## Software

### lamtram/cnn

[lamtram](https://github.com/neubig/lamtram): A toolkit for neural language and translation modeling

### Tensor Flow

[Tensor Flow](https://www.tensorflow.org/): follow the seq2seq tutorial.

### nematus/Theano

[nematus](https://github.com/rsennrich/nematus) based on Kyunghun Cho's [dl4mt tutorial](https://github.com/nyu-dl/dl4mt-tutorial).

### NMT with Coverage and Context Gating

[NMT with Coverage](https://github.com/tuzhaopeng/NMT) by Zhaopeng Tu built on top of Groundhog and Theano.

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
* Pivot based NMT.

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

### Latent variable RNN-LMs

* Latent variable RNN-LMs. See paper by Saul and Pereira.
* Use Brown clusters to initialize word vectors for RNN-LM.

### Visualization of hidden context vectors

* Build a visualizer to enable debugging of NMT systems.

