---
layout: post
title: Week 2
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.png
---

We are into the second week of GSoC coding period and with regular commits and daily meetings, things seem to be in flow now. I have started working on the integration of Gensim with scikit-learn which would be the first phase of my GSoC work.

In the past, I had worked on [PR #1244](https://github.com/RaRe-Technologies/gensim/pull/1244) which created a scikit-learn wrapper for Gensim’s LSI model. Also, we already had a scikit-learn wrapper for the LDA model (courtesy of [PR #932](https://github.com/RaRe-Technologies/gensim/pull/932)). During the last week I worked on modifying LDA model’s code ([PR #1389](https://github.com/RaRe-Technologies/gensim/pull/1389)) and the associated sklearn wrapper’s code ([PR #1382](https://github.com/RaRe-Technologies/gensim/pull/1382)) slightly. Also, to avoid duplication of code in the wrappers, I also created the abstract class *BaseSklearnWrapper* in [PR #1383](https://github.com/RaRe-Technologies/gensim/pull/1383). I also refactored the code for the existing sklearn wrappers for LDA and LSI models to incorporate this new class. In the same PR, I also fixed the *set_params()* function by using *setattr()* and also added unit-tests so that the issue doesn’t go unnoticed in the future.

Apart from this, nearly two months and 41 commits later (phew!), I finally managed to wrap up [PR #1248](https://github.com/RaRe-Technologies/gensim/pull/1248) which enables one to use Gensim’s Word2Vec model with Keras. Now that this PR has been merged in Gensim’s codebase, I would be incorporating this in shorttext’s code as well. The feedback that I have received for this PR has helped me learn many things about good coding practices as well as about technical writing in general. Hopefully, this is going to be useful in the future as well. 🙂

In the coming week, I plan to complete sklearn wrappers for Random Projections model, Author-Topic model and LDA Seq model. Plus, I also aim to wrap up [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) which has been open for some time now.