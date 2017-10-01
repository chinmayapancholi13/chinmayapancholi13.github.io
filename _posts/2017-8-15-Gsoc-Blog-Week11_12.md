---
layout: post
title: Week 11 and 12
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.jpeg
---

In the last two weeks, I had been working primarily on adding a Python implementation of Facebook Research's *Fasttext* model to Gensim. I was also simultaneously working on completing the tasks left for adding scikit-learn API for Gensim models.

For adding unsupervised Fasttext in Gensim, I have created [PR #1525](https://github.com/RaRe-Technologies/gensim/pull/1525). Initially, I had been going through the original C++ code for Fasttext and the paper *[Enriching Word Vectors with Subword Information](https://arxiv.org/abs/1607.04606)* to understand the model well before I started implementing it. Now, I have added code for both CBOW & skipgram modes and have also created unittests for checking the basic correctness of the two types of models. We plan to base our evaluation on how close the results given by our implementation are with those given by original Fasttext C++ code for tasks like suggesting the most similar words for the input word.

Regarding adding scikit-learn API for Gensim models, I refactored the code in [PR #1473](https://github.com/RaRe-Technologies/gensim/pull/1473), which modified the code for existing sklearn transformers by renaming transformer classes, removing unnecessary methods, updating *transform()* method and adding examples in the IPython notebook for sklearn. So this PR has now been merged. 

I also updated the code added in [PR #1462](https://github.com/RaRe-Technologies/gensim/pull/1462/) as per the discussion for [PR #1473](https://github.com/RaRe-Technologies/gensim/pull/1473). This included renaming classes, updating unittests and adding examples in the IPython notebook. Also, [PR #1445](https://github.com/RaRe-Technologies/gensim/pull/1445) which adds *score()* function for LDA transformer for sklearn has now been merged.
