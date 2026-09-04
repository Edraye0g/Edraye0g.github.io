---
layout: post
title: "AI and its struggle with 'What if?'"
date: 2026-09-03
categories: complex
---

Human *brain* and *learning* has a different type of relationship. From different point of view, this looks like a tug-of-war. The play is between focus vs diffuse. To process memory, human brain asks question. However, with AI people stopped asking questions to Stack Overflow but that's not it. We evaluate those questions, inside our mind, based on our prior experience and our ability to predict. But, there is another thing. We can ask the question **"What if?"**. 

![](/assests/causal0.png)

AI, right now, has evolved to think and talk like human but lacks the counterfactual questions. To understand that, we have to understand causality and the ladder of causality. Causality is the study of cause-and-effect relationships, focusing on why things happen rather than simply observing statistical correlations (e.g. if it rains, people will generally take umbrella). Causal inference is the methods used to extract causal information from data, allowing answering critical questions. The ladder of causality simply refers to the level of causation human naturally indulge into. It comprises **Association, Intervention, and Counterfactuals.** We naturally encounter situations from associating with our prior experience. Therefore, we climb up the ladders one by one. 

But AI, on the other hand, cannot do this. AI follows *Monte Carlo* method to pull and see patterns of prior knowledge. Anything outside of the pattern breaks down the whole system of thinking. AI does not have causal direction. It is stucked only at the association unit. It understands statistics by observing facts and patterns. But, outside that domain, if it jumps upper floor by the ladder it constantly faces randomized trials. Real world is never perfect. While simulating lateral airflow of a formula 1 racing car in an engine, it tries to make the boundary conditions as close as possible but never perfect. There are pitch condition, nonlinear air traffic, other car-tire junks and other things. However, a simulation scientist makes the condition as close as possible in the engine. The point is, it is not possible to replicate the real world. Hence, it is not possible to predict it either. It is bunch of Bayesian probabilistic distribution. In the intervention section, AI need to do the *'doing'* tasks. Then, there is *counterfactuals* floor. Here, AI need to imagine things. But, to imagine, a machine has to think outside of the box, countering probabilities and going against the flow. This is the problem with statistical machine learning. 

![](/assests/causal2.png)

![](/assests/causal3.png)

> Statistical machine learning relies heavily on large-scale pattern recognition within independent and identically distributed

Statistical factorization is disconnected from the physical mechanism of the system. If any single condition changes with *intervention*, the whole model will collapse and the AI prediction will fail. A causal model actually escapes this trap of entanglement. By adopting this disentangled approach, causal models benefit from the Sparse Mechanism Shift (SMS) hypothesis. An SMS only dictates a localized change in response to a small change in the environment. This disentanglement allows any model to reason about *interventions* and *counterfactuals.*


But, escaping statistical model and manifesting causal model is not that easy. There is a secondary trap.

#### Debate of Determinism 

A long standing debate exists between Judea Pearl and A. Philip Dawid regarding the necessity of determinism in causal models.

> Determinism means outcomes are fully fixed by prior causes, every event/thought/decision is the result of prior causes. 

There are two frameworks formally responsible for causal study. 

**Rubin Causal Model**
 This is also known as the potential outcomes framework. It explains that to understand causality, we must understand what would happen if the event never have occurred (a different scenario). This would explain if the causation-correlation claim justifies or not. But there is some limitation. At a time, it is only possible to observe one potential outcome. Because, multiple outcomes cannot be seen at the same time. This works best for binary outcomes.

![](/assests/causal4.jpg)

**Structure Causal Model**
 This is refurbishes RCM by structurally explaining and connecting how variables influence each other. It is formal than Rubin's model. It uses mathematical algorithm and directed graphs to map the causation. Variables are stated as exogenous (background factor impacting hidden outcome), endogenous (Variable inside the system), structural function (how endogenous variable is generated) and probability distribution.  

![](/assests/causal5.jpg)


Judea Pearl, who made the SCM, positioned himself by saying that any probabilistic model can be transformed into a deterministic model by adding unobserved "response variables." But Dawid criticized his stance. He rejected that assumption of universal causal determinism. Pearl assumes that world is causally deterministic.Pearl extends the SCM by adding response variables in the model to compute counterfactuals. He inputs hidden variables into the system and made that deterministic. But Dawid said, this is not possible or he used the specific words like "Unwanted Metaphysical Assumption." If response variables are realistic, then the Laplacian deterministic framework Pearl used has already failed. This means already a non-deterministic model exists. This is a sign of unverified property of real world. He argues against relying on response/hidden variables.   

Based on Sander Becker's paper "Causal Counterfactuals Reconsidered" proposed a middle ground between Pearl and Dawid. He agreed with Dawid that universal deterministic model using response variable just to do the Math must be rejected. But he also agrees to Pearl's standard semantics. But what Pearl did was assuming. But Becker said that it is possible to build a rigorous model without assuming which is formal and generalized. Instead of forcing deterministic probabilities, he simply just asked a realistic and causally complete potential counterfactual thinking. 

#### Conclusion
 We can see the journey of how machine learning models has changed, yet remained entangled to statistical trap. Causal inference decomposes the reality into causal mechanisms with SMS hypothesis. However, Pearl vs Dawid ultimately came to a middle ground with Becker's causal counterfactuals that we bridge the gap between statistical correlation and true physical understanding. The ultimate goal of AI development is to increase reasoning ability into **What if?** domain. 


#### Sources

[Causal ELI5: Ladder of Causality - Causify Blog](https://blog.causify.ai/causal-eli5-ladder-of-causality/)

[Causal Inference in Statistics: A Primer - Wiley](https://www.wiley.com/en-us/shop/general-introductory-statistics/causal-inference-in-statistics-a-primer-p-9781119186861)

[Causality (book) - Wikipedia](https://en.wikipedia.org/wiki/Causality_(book))

[Introduction to Judea Pearl's Do-Calculus](https://arxiv.org/abs/1305.5506)

 







