---
layout: post
title: "The Anatomy of Learning"
date: 2026-05-16
categories: neuroscience
---
![](/assests/unc0.png)
Imagine you haven’t studied the whole semester. You sit on the table. Open the book and skim through the topics you need to cover. These are mostly first-time encounter with your brain and the topics. You might strategize what need to study or just try to grasp everything vaguely. Or you can just show the exam a different road and call it a day. 
However, there are few things to observe. One is habit. Secondly, there’s strategy and then comes learning. Human brain perceives everything based on the surrounding - unexpected change in the environment and ignorance. Simultaneously, human brain predicts about the outcome with a future reward and act based on that scenario. A prediction error means a huge shift in the learning curve which eventually makes the brain update the whole belief system. But only prediction error alone does not justify the learning curve. There is another factor known as uncertainly/confidence on the prediction. This is not only what will happen but how much certainly the thing will turn out to be true. 
![](/assests/unc01.png)
You haven’t studied the whole semester makes you a complete stupid from a certain perspective. You may not study because you have strategized and predicted the reward of not studying. Maybe a dopamine surge for doing something else that took you away from exam tension. This is one way to put it. Maybe, you are planning on something else and sure of it. Think of it like, if you are certain that you will get a good job and good salary from a office, why will you study? Ultimately, the world wants workers not knowledge and wisdom. However, there’s another angle and that is bad habit.

## Rascorla-Wagner Model
The paper from *Journal of Neurobiology* naming [*Bayesian reinforcement learning: A basic overview*](https://www.sciencedirect.com/science/article/pii/S1074742724000352?via%3Dihub) shows the exact way of how human brain learn with different angles. It first talked about the RW model also known as **Rescorla-Wagner** model. This model shows that human brain always predicts an outcome/reward linearly and updates the system with errors following. If there’s no error, there’s no belief update. But, modern model like **Kalman filter** establishes certain scenarios based on uncertainty. 
Uncertainty occurs from two distinct phenomena as discussed earlier. And the Bayesian brain reacts to it in two different mathematical modelling:
**Generative model** | Brains internal assumption system based on the surroundings or how the environment is operating
**Recognition model** | This is how human brain perceives uncertainty and prior beliefs update to posterior belief.
![](/assests/unc2.png)

## Kalman Filter
![](/assests/unc3.png)
What Kalman filter denotes is human brain not only updates belief system based on the current prediction error but how much confidently the situation was predicted in the brain and came to a conclusion that there’s a factor called Kalman gain. If prediction error lies and the confidence were low, human brain updates the belief system faster. But slows down and questions the outcome with whys when there’s a higher-certainty-phenomena involved. 
Kalman filter also points toward prior belief system connecting with reward. If different stimuli resulted in a reward, human brain has a positive impact on it. Brain remembers it. However, the same situation occurs but this time a stimulus is absent, human brain updates the system by putting negative correlation value with respect to other stimuli. This is called the seesaw effect with backward blocking with Kalman filter covariance matrix. This can be taken as a recipe analogy. The recipe book says, both sugar and flour is essential for making a great cake. This is a positive correlation. While making, you realized that the sugar seemed unnecessary. The great cake taste only comes from the flour. This generates a negative correlation between sugar and flour. 
The speed of learning curve depends on the adaptivity of the surrounding or how a Bayesian brain actually process the environment. This is connected with the Kalman gain. Volatile environment also known as the true state of how environment is changing. If the rate is high, the unexpected scenario occurs more and human brain wants to learn more effectively. Kalman gain increases with response to it and learning rate increases. There can be effect of random noises. Stochasticity also known as the inherent and irreducible agents in the environment. These are easily spotted and the chances of Kalman gain is less likely to go higher resulting a slow learning rate. 
![](/assests/unc4.png)
## Temporal Difference Learning
But, the Kalman filter is basically a trial-trial process and the neurobiology of brain is a second-by-second scenario. That’s why modern and updated system introduces Kalman-TD (Temporal difference) learning system. It establishes connection with the reward system and the adaptive ability of learning in just a snap. Kalman-TD learning continuously updates valuation over time steps based on the difference between successive prediction of future rewards.
![](/assests/unc5.png)

## Latent Cause Model 
However, the paper points to a very interesting story. Think of it like watching a play. There are different scenes which represents the latent cause of learning. The first scene introduces a garden scene. The scene reflects happiness and joy and pure jolliness. When the scene ended, there was a round of applause. When the 5th scene came onto play, the scenario was intense and emotional. A grooving pain. The act was so good but no one applauded this time. 
![](/assests/unc6.png,/assests/unc7.png)
This happened due to the tendency on human brain perceiving the structure of the environment AKA **Structural learning.** The brain understands the hidden context using latent cause model. It adapts the understanding while also retaining the past memories. It adjusts new expectations and interpretation of the world in a newer way.

## The Neurobiology
![](/assests/unc8.png)

## Bad habit
Now the most important question arises. How is bad habit processed in the brain even though knowing that this is bad? 
**The death of Uncertainty:** People thinks and believes that this is the only way even though chances of negative consequences. This creates zero Kalman gain and eventually zero uncertainty. 
**Exploration vs Exploitation:** Even having negative outcome, people lose the interest of trying new things and exploited by falling a victim to bad habits. 
**Dopamine Hijacking:** Dopamine signals prediction error to Temporal difference learning. A bad habit always provides a huge dopamine surge into the brain resulting false signals about addiction. Telling that, addiction actually means rewarding. 
The paper also says that human brain never actually forgets a bad habit. While rehabilitating from an addiction, the habit was veiled by newer habits and routine. Once the same latent cause that dragged the addiction or bad habit before comes up again, it sends sensory cue to brain that makes relapses again. Brain never actually unlearn things but creates architectural blocks on top of another to suppress the emotion or habit. 

## My thoughts
If we never unlearn anything, does human ever actually change? Human is very bad at suppressing things too. That’s why research says, human brain is all about believing linguistically. What we say is what we believe to us. A person in stress, talks with himself rather than suppressing anxiety makes better visual cues for others surrounding him, as human brain is very good at spotting micro-cues.

## References
[Bayesian reinforcement learning: A basic overview](https://www.sciencedirect.com/science/article/pii/S1074742724000352?via%3Dihub)

