---
layout: post
title: Week 2
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.png
---

This week, I worked on developing scikit-learn wrappers for Gensim's Random Projections ([PR #1395](https://github.com/RaRe-Technologies/gensim/pull/1395)), LDASeq ([PR #1405](https://github.com/RaRe-Technologies/gensim/pull/1405)) and Author Topic ([PR #1403](https://github.com/RaRe-Technologies/gensim/pull/1403)) models. I also refactored the existing scikit-learn wrappers for LDA and LSI models in [PR #1398](https://github.com/RaRe-Technologies/gensim/pull/1398) by incorporating changes such as using composite design pattern, removing unnecessary attributes and updating the associated unit-tests.

Apart from this, I worked on [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) which computes the training loss for Gensim's Word2Vec model. For doing this, I needed to add code for computing the training loss in both Python and Cython code associated with the Word2Vec model. I am now working on getting useful benchmarks about the change in performance with-respect-to the time taken and memory used, as a result of the newly added code for training loss computation.

As mentioned in the last blogpost, I have also opened [PR #7](https://github.com/stephenhky/PyShortTextCategorization/pull/7) for incorporating the changes made in Gensim in [PR #1248](https://github.com/RaRe-Technologies/gensim/pull/1248) in shorttext's existing code. This PR is a work in progress and I hope to wrap it up within this week.

In the coming week, I plan to develop scikit-learn wrappers for Gensim's Word2Vec, Doc2Vec, Text to Bag-of-words and Tf-Idf models. I am also aiming to wrap up [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) and [PR #7](https://github.com/stephenhky/PyShortTextCategorization/pull/7) in the coming week.