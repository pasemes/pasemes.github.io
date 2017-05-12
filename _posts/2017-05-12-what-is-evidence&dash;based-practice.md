---
layout: post
title: "What is evidence-based practice?"
tags: [evidence-based software engineering]
#bigimg: /img/blog/welcome-to-the-blog/evidence.jpg
date: 2017-05-12 12:00:00 -0300
permalink: /blog/what-is-evidence-based-practice/
layout: post
comments: true
show-share: true
show-subscribe: true
---

# A little bit of history

Did you know that you are subject to the evidence-based practice (EBP) whenever you visit a doctor? Have you ever wondered why you are (usually =) so confident that your physician has the right treatment for you? Implicitly, it seems that all of us assume that the treatment is selected based on one or more (factual) reasons for believing that it will have positive effects on our illness. Not by chance, this is precisely the definition of evidence[^1].

Isn't that interesting? We expect that physicians base their practice on evidence, but we in the software community seem to prefer to argue about whether a practice brings *happiness* or a framework provide an *elegant* solution for a problem. Not that these aspects aren't important, but you got the point. I have never met a software developer (outside the academic circle) that is aware of the EBP. If you are one, please leave a comment! I would be glad to know who (and how many) you are.

The notion of EBP dates from the beginning of the 1990s in the Medicine discipline. In 1990, Dr. Gordon Guyatt introduced a new concept called "Scientific Medicine" to describe a new method of teaching medicine at the bedside, using the critical appraisal techniques from Dr. David Sackett. One year later the term "Evidence-Based Medicine" (EBM) was coined in the ACP Journal Club Editorial[^2]. The basic idea of EBM is to bring more certainty to clinical decision making. Before EBM, "clinical practice was historically viewed as the 'art of medicine.' Expert opinion, experience, and authoritarian judgment were the foundation for decision making. The use of scientific methodology, as in biomedical research, and statistical analysis, as in epidemiology, were rare in the world of medicine."[^3] Looks familiar, eh? 

> In the case of Medicine, the basic idea of the EBP is to bring more certainty to clinical decision making.

Since its proposal, EBM received huge attention. The term was then generalized from EBM to EBP. And several fields have adopted EBP aiming at improving its decision-making process such as Administration, Nursing, Marketing, and, of course, Software Engineering. In our case, EBP was brought in 2004 by Barbara Kitchenham and her colleagues in the International Conference on Software Engineering[^4]. Still, even though this was the first mention of EBP in Software Engineering, which was then denominated Evidence-Based Sofware Engineering (EBSE), the field promotes the evidence (through experimentation) since 1978. The general research topic under which experimentation and evidence are investigated is called Empirical Software Engineering.  

# Evidence-Based Software Engineering (in the view of researchers)

Ok, so now that you know the origin of EBP and what it is about, it is time to understand how EBP can help our field to get out of the fashion-oriented industry to a real engineering field. Before presenting my view about how EBP should be in software engineering, I'll present it "as is" (in the view of researchers). Based on the definition from Medicine, the EBSE is defined as follows[^4]:

> To provide the means by which current best evidence from research can be integrated with practical experience and human values in the decision-making process regarding the development and maintenance of software.

To achieve this goal, researchers from Empirical Software Engineering operationalize ESBE in five steps[^5]:

1. Convert a relevant problem or information need into an answerable question;
2. Search the literature for the best available evidence to answer the question;
3. Critically appraise the evidence for its validity, impact, and applicability;
4. Integrate the appraised evidence with practical experience and the customer's values and circumstances to make decisions about practice;
5. Evaluate performance and seek ways to improve it.

The EBP is about asking the right question (to able to search for the evidence available --- step 1). Thus, instead of look for the "hype of the moment", EBP should enable us to seek for the reasons to believe that a software development technology will provide the support we expect from it. But how you can find the evidence?

I'll try to be succinct here since the steps do not make this clear. They only hint that you will find the answer for your problem in the literature. However, surveying the literature is a hard task. There are a huge amount of scientific articles published  --- which must be screened to obtain the answer. To perform this orderly, systematic review is proposed as a procedure to translate the "right question" into a search string and the criteria to appraise the evidence (steps 2 and 3). Fortunately, several topics in software engineering have been targeted of systematic reviews (up until 2010 there were 67 reviews covering 24 topics[^6]). After that you are on your own (steps 4 and 5), it is expected that you understand the papers and can extract the necessary information to integrate the evidence with your practical experience. As one can see, this is not an easy task as well. Below, I'll explore this and other aspects regarding the researcher view of EBSE.

# Why EBSE isn't widely adopted by software engineers?

Based on these definitions, I can't blame you for not knowing what ESBE is. I could list a number of arguments for that, but there is one which in my view is sufficient to explain the situation. It says that you must search the best evidence from *research*, which "for a good understander"[^7] means that software engineers do not know how they can provide evidence for technologies. Yes, it says that you can integrate it with practical experience, but it is clear that evidence (from research) is what is important. After all, the practice is called *Evidence*-Based Software Engineering. 

> Strictly speaking, the EBSE imposes an artificial hierarchy between researchers and software engineers, which obviously is not going to be accepted by the latter. Why would software engineers have to accept prescriptions regarding how we should work, even in the form of evidence?

As if that was not enough, precisely because most researchers impose this segregation between who investigate and who apply the findings, it is common to find results that are not directly applicable or are not relevant to the practice. Not to mention that when they are applicable, the results are usually "buried" in a highly technical propositional text written with the maximum rigor in mind, but not necessarily readability.  

In addition to these issues, which I consider the most salient, there are several other discussions regarding the utility of EBP. For instance, some issues that are directly translatable from the critics of EBM. "Some claim that it transforms the complex process of clinical decision making, which includes data gathering, years of medical knowledge, experience, and astute intuition into an algorithmic exercise that is not individualized for specific clinical scenarios and therefore subject to error in patient care".

# How can we change that? 

The EBP is clearly not a panacea. Still, apart from the issues discussed, I hope that you are convinced that it is imperative we stop creating new technologies without any evidence regarding its utility and potential benefits. Hence, it is also urgent that we find the means to build a body of evidence that is readily available for software engineers. In my view, there are three main areas that we must act upon: (i) software engineers producing evidence from their practice, (ii) a description format[^8] for evidence, and (iii) an infrastructure to support searching and managing the available evidence. With these areas addressed, the EBP culture can flourish, and our community will benefit from informed decisions which will contribute to increasing our focus on software development technologies that (really) support our work.

> We must act upon three areas: (i) software engineers producing evidence from their practice, (ii) a description format[^8] for evidence, and (iii) an infrastructure to support searching and managing the available evidence.

In this blog, I expect to contribute to all these areas. Regarding the item (i), it is my intention to make this blog a reference for how you can produce (and use) evidence. For the second item, I'll present evidence published in scientific journals, concentrating --- and translating if necessary --- on the relevant aspects to inform decisions on practice. By the way, if you have any theme you are interested in what is there in terms of evidence, please leave a comment. I also intend to discuss the description format itself. The last item is a community endeavor; I'm optimistic that we can start this together.

[^1]: Evidence represents "one or more (factual) reasons for believing that something is or is not true". This definition was discussed on the previous [post].(http://www.evidencebasedpractice.se/blog/welcome-to-the-blog/).
[^2]: [Evidence-based medicine](http://www.acpjc.org/Content/114/2/issue/ACPJC-1991-114-2-A16.htm)
[^3]: [History of evidence-based medicine](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3263217/).
[^4]: [Evidence-Based Software Engineering](http://dl.acm.org/citation.cfm?id=998675.999432).
[^5]: [Evidence-based software engineering for practitioners](http://ieeexplore.ieee.org/document/1377125/).
[^6]: [Six years of systematic literature reviews in software engineering: An updated tertiary study](http://www.sciencedirect.com/science/article/pii/S0950584911001017).
[^7]: Here in Brazil we use this expression to denote that the text or speak has an implicit meaning, which is easily deduced. The full proverb is: "for a good understander half word is enough" (literally translated from portuguese).
[^8]: In Medicine, there is a research field dedicated to this theme. It is called [Knowledge Translation](http://ph.cochrane.org/knowledge-translation).
