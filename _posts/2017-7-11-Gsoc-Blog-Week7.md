---
layout: post
title: Week 7
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.png
---

In the last week, I worked on PRs in both Gensim and shorttext repositories.

In Gensim, I worked on [PR #1445](https://github.com/RaRe-Technologies/gensim/pull/1445) to include *u_mass* mode in the *score* function for *SklLdaModel* class. I also
updated the IPython notebook for scikit-learn integration with examples to explain the usage of the newly added code.
I also worked on adding a scikit-learn wrapper for Gensim's Doc2Vec class in [PR #1462](https://github.com/RaRe-Technologies/gensim/pull/1462). The same PR also
adds unittests for the new wrapper class.
I also created [PR #1473](https://github.com/RaRe-Technologies/gensim/pull/1473) to refactor the code for all the existing sklearn-api classes. This refactoring included renaming
wrapper classes, updating unittests, rephrasing docstrings and updating corresponding IPython notebook examples.

The changes that I made to shorttext during the last week were primarily focused around adding support for the changes made in [PR #1248](https://github.com/RaRe-Technologies/gensim/pull/1248) in Gensim. Regarding this, I worked on [PR #9](https://github.com/stephenhky/PyShortTextCategorization/pull/9) which fixed a bug in the code 
to load the value of *with_gensim* variable from the saved json file and also updated docstrings for the save and load functions for *VarNNEmbeddedVecClassifier* class.
I also created [PR #10](https://github.com/stephenhky/PyShortTextCategorization/pull/10) which added support for the changes made in [PR #1248](https://github.com/RaRe-Technologies/gensim/pull/1248) by adding the codepath along *with_gensim=True* to the classes *shorttext.classifiers.embed.nnlib.frameworks.DoubleCNNWordEmbed* and *shorttext.classifiers.embed.nnlib.frameworks.CLSTMWordEmbed*.
