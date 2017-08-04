---
layout: post
title: Week 9 and 10
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.png
---

In the last two weeks, I worked mainly on updating and adding sklearn API for models in Gensim and updating tests in shorttext. I was not able to add a blog in the previous week since my college semester has now commenced and I was travelling at the time.

In [PR #1473](https://github.com/RaRe-Technologies/gensim/pull/1473), I removed the *BaseTransformer* class and refactored the code for API classes accordingly. I updated the unittests to ensure the after calling *set_params()* and *fit()* function, the parameter values are set for the actual Gensim model as well. I also changed *transform()* function to use *sparse2full()* while creating the output matrix for the function. In the same PR, I added *testConsistencyWithGensimModel()* unittest for LDA and Word2Vec transformers. In [PR #1462](https://github.com/RaRe-Technologies/gensim/pull/1462), I added API classes for Gensim's Hdp and Phrases models along with the corresponding unittests. In [PR 1445](https://github.com/RaRe-Technologies/gensim/pull/1445), I updated the example for *score()* function for LDA model in the IPython notebook *sklearn_wrapper.ipynb*.

In shorttext, I added [PR #15](https://github.com/stephenhky/PyShortTextCategorization/pull/15) for restructuring the tests. I also created [PR #16](https://github.com/stephenhky/PyShortTextCategorization/pull/16) for updating the documentation in *docs.tutorial_nnlib*. In [PR #18](https://github.com/stephenhky/PyShortTextCategorization/pull/18), I modified the test conditions to make sure tests pass for all valid scenarios. 
