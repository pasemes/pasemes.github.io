---
layout: post
title: "Was Test-Driven Development ever alive? The reality regarding its impacts on the productivity and software quality"
tags: [meta-analysis, synthesis, test first, test-driven development]
bigimg: /img/blog/DecisonMakingTree.jpg
date: 2017-05-12 12:00:00 -0300
permalink: /blog/was-tdd-ever-alive/
layout: post
comments: true
show-share: true
show-subscribe: true
---

#The origin and the expected benefits of TDD

TDD was rediscovered by Kent Beck and thoroughly presented in his famous book "Test Driven Development: By Example". It was initially put among the cornerstone practices of the Extreme Programming (XP) development process, but it became so popular that was adopted as a stand-alone agile practice. In a period when software testing was regarded as something for mature organizations performed usually at the end of lengthy releases, the rediscovery of TDD was an important instrument to support the introduction of some agile principles emerging at the time.  The basic idea attributed to TDD is to provide a continuous feedback regarding the current state of your development process in terms of the source code design improvement and defects expectancy reduction. As a result, TDD is extremely useful for several agile practices particularly those concerned with the short iterative nature of agile methods such as welcoming changes, maintaining a constant pace, and assessing the progress of working software. For this reason, its main expected benefits are:

* Work with confidence;
* Work on a series of achievable steps instead of tackling a big problem all at once;
* Ensure that software design meets the need of the actual code;
* Leave behind a suite of tests to help preserve the integrity of the code.

Despite the improvements associated with TDD, there are several possible drawbacks which are seldom discussed. Most of them are concerned with two main aspects: *testing before code* and the design aspects associated with it by the means of *refactoring*. The level of *automation* in terms of testing coverage is also a target of discussions. Those drawbacks remained hidden for several years mostly because of the religiosity to which most developers devoted to the so-called "red-green-refactor cycle." It was not up until 2014 that David Heinemeier Hanson posted in his blog the article entitled [TDD is dead. Long live testing](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html) which is to the best of my knowledge the first with a great prestige in the open source community to touch this subject.  

#The controversy: is TDD dead?

The David's posts and talks generated a lot of fuss. To the point that he, Kent Beck, and Martin Fowler came together to discuss the subject. They produced a five-part series that were broadcast on YouTube. The first video of the series has more than a hundred thousand views. The topics addressed in the series are summarized below. This was based on the [post](https://martinfowler.com/articles/is-tdd-dead/) from Martin Fowler in which he reports their conversation.

**Confidence:** TDD is one way to programmers feel confident that their code works.  However, developers should *not* mix up the concepts of TDD and self-testing code. One of the benefits of TDD includes producing self-testing code. Thus, TDD is not the only option to improve confidence. Furthermore, TDD is commonly practiced in a heavy mocking style, and people usually make bad trade-offs regarding the evaluation of whether it is worth making intermediate results testable. 

**Design damage:** TDD puts an evolutionary pressure on the design. Most of the time it requires unnecessary indirection and complexity to make it easier to test. There are divergences regarding whether TDD is the only cause for that. For instance, is not this a general problem of software design, particularly concerning cohesion and coupling? Nevertheless, in some situations, the isolation and modularity are solely induced by TDD.

**Feedback and QA:** TDD provides feedback of three different aspects: (i) is the software doing something useful for the user? (ii) have I broken anything? (ii) is my code-base healthy? This feedback in the developers' hands is one of the most important elements of TDD (and self-testing code). However, the TDD's success had led to a neglect of QA. The other issue is that there is an emphasis on TDD benefits without a clear understanding of its costs. The conclusion is that TDD is probably better than the old dysfunctional relationship in which developers simply viewed QA as a someone else problem. But definitely not better than an effective QA team.  Still, it is the absence of a QA team can be important in some situations such as in the case of most startups. 

**Costs:** 







