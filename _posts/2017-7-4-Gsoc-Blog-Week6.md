---
layout: post
title: Week 6
tags: [gsoc, python, programming]
comments: true
image:
 feature: gsoc.png
---

During the previous week, I mainly worked on [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201), [PR #1437](https://github.com/RaRe-Technologies/gensim/pull/1437) and [PR #1445](https://github.com/RaRe-Technologies/gensim/pull/1445).

I was finally able to get [PR #1201](https://github.com/RaRe-Technologies/gensim/pull/1201) merged after obtaining the relevant benchmark values to analyze the effect on the time required for training a Word2Vec model due to the loss-computation code added in the pull-request.

In this week, a large chunk of my time and effort was devoted to working on [PR #1445](https://github.com/RaRe-Technologies/gensim/pull/1445), which implements *score* function for the scikit-learn wrapper class for LDA model. The *perplexity* mode of the function has been implemented and I am currently working on how to implement other modes (i.e. *c_v*, *c_uci*, *c_npmi* and *u_mass*) which use topic-coherence as a measure for computing the score value. However, as of now, there are certain issues with the implementation of these 4 modes. For the sliding-window based modes i.e. *c_v*, *c_uci* and *c_npmi*, we need *Texts* parameter of the class *CoherenceModel* in order to compute the topic-coherence values. However, this parameter is not needed as such for the LDA model’s sklearn wrapper so we are having to input extra information just for implementing the *score* function associated with the class, which is not a desirable scenario. For *u_mass* mode of computing topic-coherence, I am getting a *ZeroDivisionError* because of *w_star_count* value being zero in this line, which computes the pointwise mutual information between word-pairs formed from the top-n words representing the topics. The reason for this is the fact that count of words, which represent the topics obtained for training data, may be zero in the testing data. A solution for both these issues is adding an additional optional attribute to the wrapper class for LDA model so that the user can store the value of Texts and pass it to the score function. However, this solution has not been finalized till now and the implementation details of this PR are still being discussed.