---
layout: post
title: Week 5
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.jpeg
---

This week, I worked on creating new scikit-learn wrappers for Gensim models. In addition to that, I worked further on older unmerged PRs like [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) and [PR #7](https://github.com/stephenhky/PyShortTextCategorization/pull/7).

I created [PR #1437](https://github.com/RaRe-Technologies/gensim/pull/1437) which adds an sklearn wrapper for Gensim’s Word2Vec model along with relevant unit-tests. Except a few minor suggestions which need to be incorporated in the code, the PR is merge-ready. I also worked further on [PR #1403](https://github.com/RaRe-Technologies/gensim/pull/1403) which adds an sklearn wrapper for Gensim’s Author-Topic model. Some unit-tests like integration with sklearn Pipeline were earlier missing from the PR and this has now been merged.

For [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201), the ongoing confusion about the apparent difference in training loss values obtained from Python and Cython paths got resolved after further discussion and I am currently working on adding useful benchmarks for the PR so that we get a clear idea about the effect on training time due to this code modification.

In shorttext, [PR #7](https://github.com/stephenhky/PyShortTextCategorization/pull/7), which incorporates the change corrsponding to [PR #1248](https://github.com/RaRe-Technologies/gensim/pull/1248) in Gensim, has now been merged. However, some changes corresponding to saving and loading of models still need to be implemented which I plan to complete in the coming week.

I am also currently working on [PR #1445](https://github.com/RaRe-Technologies/gensim/pull/1445) which creates scorer functions for sklearn wrappers for models such as LDA, LSI etc so that the user doesn’t need to write a custom scoring function for tasks like *GridSearch* in scikit-learn.

In the coming week, I would be working on creating sklearn wrappers for Doc2Vec, Text to Bag-of-words and Tf-Idf models in Gensim. I also plan to finish the work left in [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) and get it merged soon. 🙂