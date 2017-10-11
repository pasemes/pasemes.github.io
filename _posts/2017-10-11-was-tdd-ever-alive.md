---
layout: post
title: "Was Test-Driven Development ever alive?"
subtitle: "The reality regarding its impacts on the productivity and software quality"
tags: [meta-analysis, synthesis, test first, test-driven development]
bigimg: /img/blog/stop_light.jpg
date: 2017-10-11 12:00:00 -0300
permalink: /blog/was-tdd-ever-alive/
layout: post
comments: true
show-share: true
show-subscribe: true
---

> This is the first post presenting evidence of a software development practice. I have chosen TDD as the first topic because of the recent controversy regarding its benefits and the remarkable devotion dedicated to it by a significant part of software developers. The text begins recalling the recent controversy involved in this theme, but readers interested in just the results of TDD compared to automated unit testing in general can go directly to the [corresponding section](#the-reality-results-from-27-empirical-studies). 

# The origin and the expected benefits of TDD 

TDD was rediscovered by Kent Beck and thoroughly presented in his famous book "Test Driven Development: By Example". It was initially put among the cornerstone practices of the Extreme Programming (XP) development process, but it became so popular that was adopted as a stand-alone agile practice. In a period when software testing was regarded as something for mature organizations performed usually at the end of lengthy releases, the rediscovery of TDD was an important instrument to support the introduction of some agile principles emerging at the time.  The basic idea attributed to TDD is to provide a continuous feedback regarding the current state of your development process in terms of the source code design improvement and defect expectancy reduction. As a result, TDD is essential for several agile practices particularly those concerned with the short iterative nature of agile methods such as welcoming changes, maintaining a constant pace, and assessing the progress of working software. For this reason, its main expected benefits are:

* Work with confidence;
* Work on a series of achievable steps instead of tackling a big problem all at once;
* Ensure that software design meets the need of the actual code;
* Leave behind a suite of tests to help preserve the integrity of the code.

Despite the advantages associated with TDD, there are several possible drawbacks which are seldom discussed. Most of them are concerned with two main aspects: *testing before code* and the design aspects associated with it by the means of *refactoring*. The level of *automation* in terms of testing coverage is also a target of discussions, but it is not particular to TDD. Those drawbacks remained hidden for several years mostly because of the religiosity to which most developers devoted to the so-called "red-green-refactor cycle." It was not up until 2014 that David Heinemeier Hanson posted in his blog the article entitled [TDD is dead. Long live testing](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html) which is to the best of my knowledge the first with a great prestige in the open source community to touch this subject with emphasis.  

# The controversy: is TDD dead?

The David's posts and talks generated a lot of fuss. To the point that he, Kent Beck, and Martin Fowler came together to discuss the subject. They produced a five-part series that were broadcast on YouTube. The first video of the series has more than a hundred thousand views. The topics addressed in the series are summarized below. This was based on the [post](https://martinfowler.com/articles/is-tdd-dead/) from Martin Fowler in which he reports their conversation.

**Confidence:** TDD is one way to programmers feel confident that their code works.  However, developers should *not* mix up the concepts of TDD and self-testing code (i.e., testing automation). One of the benefits of TDD includes producing self-testing code. Thus, TDD is not the only option to improve confidence. Furthermore, TDD is commonly practiced in a heavy mocking style, and people usually make bad trade-offs regarding the evaluation of whether it is worth making intermediate results testable. 

**Design damage:** TDD puts an evolutionary pressure on the design. Most of the time it requires unnecessary indirection and complexity to make it easier to test. There are divergences regarding whether TDD is the only cause for that. For instance, is not this a general problem of software design, particularly concerning cohesion and coupling? Nevertheless, in some situations, the isolation and modularity are solely induced by TDD.

**Feedback and QA:** TDD provides feedback of three different aspects: (i) is the software doing something useful for the user? (ii) have I broken anything? (ii) is my code-base healthy? This feedback in the developers' hands is one of the most important elements of TDD (and self-testing code). However, the TDD's success had led to a neglect of QA. The other issue is that there is an emphasis on TDD benefits without a clear understanding of its costs. The conclusion is that TDD is probably better than the old dysfunctional relationship in which developers simply viewed QA as a someone else problem. But definitely not better than an effective QA team.  Still, it is the absence of a QA team can be important in some situations such as in the case of most startups. 

**Costs:** over-testing is the main concern in this aspect. The primary cause for over-testing seems to be the notion that "a line of code should not be written without a failing test." this means that when one needs to change behavior, there is more code to change. It is hard to get the amount of testing just right, sometimes one will overshoot and sometimes undershoot. Thus, there is no worry to overshoot from time to time. Furthermore, one should not use the ratio of lines of test code to lines of production, since some situations require strict quality criteria (e.g., compilers). 

Although I deliberately did not cite the names in the above summary in order to make it succinct, it is possible to see that the debaters were very opinionated in their views. David brought several problems that he experienced using TDD during Ruby on Rails construction whereas Kent pondered the arguments restating the TDD benefits. For instance, it was David who mentioned the "evolutionary pressure on the design" and Kent answered it observing that the developers should consider "whether it is worth making intermediate results testable." Martin provided perspectives and thoughts which aptly complemented the discussion with his experiences as a consultant. As an example, in the costs of over-testing theme, Martin mentioned ThoughtWorks has a strong testing culture. For this reason, it was certain that they have some over-tested code, but this not necessarily represents a problem.

It is clear that all the discussion is based on their experiences. However, even though they are experienced and well-known, this does *not* represent evidence of TDD. That is, their observations were accumulated from a long period of time and thus are certainly subject to bias. For this reason, these opinions cannot be taken as evidence for either benefits or drawbacks of TDD.   

# The reality: results from 27 empirical studies 
In what follows, I will show the main results of a [meta-analysis study regarding TDD](http://ieeexplore.ieee.org/document/6197200/). Using the appropriate statistics, a meta-analysis combines the results of quantitative studies, which we call primary studies -- the study that combines primary studies is called secondary study. **The primary studies compare TDD with either "iterative testing", i.e., interleaved with coding, or "test last", i.e., after major parts of or the full system was implemented.** 

Two analyses were necessary according to the data present in the studies. Both analyses are used to estimate the *effect size*, which is represented by a number that tells you how much one group differs from another (i.e., TDD and test last). The standardized analysis uses the [Hedges' statistic](http://www.statisticshowto.com/hedges-g/), which requires that the primary study reports the mean and standard deviation for each group. Otherwise, when these data are not present, the unstandardized analysis is applied, which is a basic percentage comparison -- it does not consider, for instance, the mean, the standard deviation, and the groups' size. **A positive effect size means represents a result favoring TDD whereas a negative one favors the compared approach (iterative or last).**

Due to limitations of the evidence found, the meta-analysis only considers two aspects of TDD: productivity and external quality. Also, the primary studies have different contexts. Some used students and, for this reason, are referred to as academic studies while others were conducted in a real-world environment with professionals and are named industrial studies. There were differences regarding the compared testing approach as well, i.e., "test last" or Waterfall and "iterative testing". Besides, several studies included other agile practices such as pair programming.

## Results on external quality
The external quality aspect was evaluated using different metrics:
* number of defects/bugs/trouble reports/defect cases that were found;
* defects per KLOC/defect density;
* number/percentage of acceptance/black-box/external tests passed;
* number/percentage of unit tests passed, and quality mark given by client.

Eleven standardized and twenty-four unstandardized effect sizes were obtained for external quality. 

The data for the **standardized analysis shows that there is no difference regarding TDD and the compared groups with an effect size of -0.010.** However, among the eleven standardized effect sizes, **only one study was from industrial settings, which had an effect size of 0.309.** The remaining ten studies were conducted in the academic settings and had a combined effect size of -0.049. Effect sizes with an *absolute* value in the range 0.0-0.37, 0.38-1.0, and 1.0 and above can be considered as small, medium, and large sized effects, respectively. And a positive value favors TDD whereas a negative one favors the compared approach (iterative or last).

There were more effect sizes from industrial settings in the case of the **unstandardized analysis** -- a total of 8 from the 24. The results show an **improvement of 52% in favor of TDD in industrial settings.** This value drops to 10% in the case of academic studies. **An overall improvement of 24% is obtained** when all effect sizes are considered together. 

> In summary, TDD is *moderately superior* to the compared tested strategies (iterative testing or test last) regarding external quality in industrial settings. However, when it is isolated from other agile practices or used by inexperienced developers no difference was found.

## Results on productivity
The productivity aspect was evaluated using different metrics:
* Development time/person hours spent/task time;
* Total LOC divided by total effort, or the number of LOC per hour;
* Total noncommented LOC;
* Number of delivered stories per unit effort (or implemented user stories per hour);
* Delivered noncommented LOC per unit development effort (or effort per ideal programming hour); 
* Hours per feature/development effort per LOC.

Ten standardized and twenty-three unstandardized effect sizes were obtained for productivity.

The data for the **standardized analysis shows that there is no difference regarding TDD and the compared groups with an effect size of 0.048.** Again, repeating the pattern found in the external quality, **only one study was from industrial settings, however, in this case, it favors the compared approach with an effect size of -1.111.** The remaining nine studies were conducted in the academic settings and had a combined effect size of 0.187. As aforementioned, effect sizes with an *absolute* value in the range 0.0-0.37, 0.38-1.0, and 1.0 and above can be considered as small, medium, and large sized effects, respectively. And a positive value favors TDD whereas a negative one favors the compared approach (iterative or last).

The results of the **unstandardized analysis show a decrease of -22% in productivity when using TDD in industrial settings**, represented by eight effect sizes. This value increases to 19% when considering the remaining 15 effect sizes of the academic studies. **Combining all effect sizes, there is practically no difference between TDD and the compared approaches** -- an increase of 4% was found. 

> In summary, TDD is *moderately inferior* to the compared tested strategies (iterative testing or test last) regarding productivity in industrial settings. However, when it is isolated from other agile practices no difference was found. And when it is used by inexperienced developers it tends to favor the productivity.

# Not dead but definitely not super alive, either
Most of the controversy regarding TDD's benefits and drawbacks discussed in blogs and promoted in conferences are based on personal opinions and experiences. The results based on *empirical* evidence add facts to the discussion, making the evaluation of TDD objective. I hope that this post can convince you how the evidence-based practice can eliminate opinionated disputes and "flame-wars." 

Unfortunately, there still no evidence regarding the TDD effects on the design, which is an important aspect of the practice. The same is true for the costs although it is directly related to productivity.  

**Given the results, we can conclude that TDD favors the external quality to the detriment of productivity.** Personally, I was not expecting that TDD would reduce the defect density (i.e., improve the external quality) when compared to the other approaches since they were also implemented as automated unit tests (just not before the production code).

At last, it should be stated that, even though it is expected that a secondary study is considerably more reliable than expert opinions, this kind of result is also subject to different issues denominated validity threats. In a secondary study, the threats are associated with the aggregation procedure itself and also can be carried over from the primary studies. For more details about the validity threats please refer to the  [paper](http://ieeexplore.ieee.org/document/6197200/).