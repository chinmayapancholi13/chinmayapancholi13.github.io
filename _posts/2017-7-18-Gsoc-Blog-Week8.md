---
layout: post
title: Week 8
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.jpeg
---

During the last week, I continued to work on my PRs in both shorttext and Gensim repositories.

In Gensim, I worked on [PR #1445](https://github.com/RaRe-Technologies/gensim/pull/1445) to fix error handling in the function *topic_coherence.direct_confirmation_measure* in case a top-n topic word for the training corpus is not present in the corpus being used to compute the topic-coherence value. I also added examples in *docs.notebooks.sklearn_wrapper.ipynb* for various scoring function modes for LdaModel's API class. I continued to work on [PR #1473](https://github.com/RaRe-Technologies/gensim/pull/1473) to refactor the exising code after removing functions *get_params()*, *set_params()* and *partial_fit()* from the base API class. As part of [PR #1462](https://github.com/RaRe-Technologies/gensim/pull/1462), I added code and unitests for Text-to-BOW and Tf-Idf models in Gensim.

In shorttext, I created [PR #12](https://github.com/stephenhky/PyShortTextCategorization/pull/12) to integrate the repository with Travis CI. So, we can now add unittests to make sure new code changes don't break the functioning of the existing code (yay!). I also created [PR #13](https://github.com/stephenhky/PyShortTextCategorization/pull/13) to add unittests for the classes *CNNWordEmbed*, *DoubleCNNWordEmbed* and *CLSTMWordEmbed* present in *classifiers.embed.frameworks*.
