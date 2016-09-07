---
layout: default
img: escherbabel
img_link: http://en.wikipedia.org/wiki/Tower_of_Babel_(M._C._Escher)
caption: "1928 woodcut by M. C. Escher showing the Tower of Babel."
title: "Project"
active_tab: project
---

Final Project
-------------

The goal for each final project is a submission to a conference at the end of the semester (perhaps with some more work on the paper in the Spring semester).

## Project Ideas

### Multilingual embeddings for low-resource languages

Improve performance on a language pair such as Haitian Kreyol to English where there is insufficient data for training a neural MT model.

### Complex reorderings in neural MT

Go beyond the attention model to capture more complex reorderings and experiment on language pairs such as Chinese-English.

### Global sequence to sequence learning

Improve upon bidirectional RNNs by exploring global inference and complex non-differentiable loss functions such as BLEU scores. Currently the state of the art is to have a layer on top of a bidirectional sequence model which does global reordering.

An interesting first step might be to take the alignments learned by a (neural) HMM alignment model and use the entire distribution of alignments within a decoder.

### Decipherment using neural LMs

Can we improve on computational decipherment methods by using neural LMs and going beyond HMMs for scoring the cipher keys.
A more ambitious idea is to map images of text to language models bypassing the possibly error-prone human element in converting
the visual script to machine readable text. For instance, scans of the Voynich manuscript are available from the Yale library.
Can they be mapped to another language for which we have a language model.


