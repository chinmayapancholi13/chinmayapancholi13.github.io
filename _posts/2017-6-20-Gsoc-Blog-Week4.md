---
layout: post
title: Week 4
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.jpeg
---

During the last week, I continued working on creating scikit-learn wrappers for Gensim’s LDA ([PR #1398](https://github.com/RaRe-Technologies/gensim/pull/1398)), LSI ([PR #1398](https://github.com/RaRe-Technologies/gensim/pull/1398)), RandomProjections ([PR #1395](https://github.com/RaRe-Technologies/gensim/pull/1395)) and LDASeq ([PR #1405](https://github.com/RaRe-Technologies/gensim/pull/1405)) models. After making several changes including updating wrapper class-methods and adding unit-tests for features like model persistence, integration with sklearn’s Pipeline, incorporating NotFittedError as well as fixing some of the older unit-tests, these PRs have now been accepted and merged. 🙂 I also created [PR #1428](https://github.com/RaRe-Technologies/gensim/pull/1428), which updates the IPython notebook sklearn_wrapper.ipynb explaining the usage of sklearn wrappers for the four Gensim models mentioned above.

Integration with sklearn PipelineI also worked further on [PR #7](https://github.com/stephenhky/PyShortTextCategorization/pull/7) in shorttext by refactoring the code to reduce redundancy by getting rid of unnecessary files and classes. I am now working on updating the load and save methods associated with the modified classes.

In the last week, I had added Python and Cython code for computation of training loss for [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201). However, I have been getting different values of training loss when the code uses Python path and when it uses Cython path for the exact same input while training. I am currently investigating the reason for this difference in values. Once I have this figured out, I plan to get some useful benchmarks to see the effect of the newly added code.

During the last week, I had to devote more time for the existing wrappers than I had anticipated so I couldn’t get started with working on newer wrappers. So in the coming week, I would be creating scikit-learn wrappers for Word2Vec, Doc2Vec and Text to Bag-of-words models in Gensim. I also plan to finish the remaining work in [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) and [PR #7](https://github.com/stephenhky/PyShortTextCategorization/pull/7) in the following week.