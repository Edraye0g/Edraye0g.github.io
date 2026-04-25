---
layout: post
title: "Inferring Others Strategical Thinking | Mentalization"
date: 2026-04-26
categories: neuroscience
---

Shirts tucked in. Eyes are on the ball. The whole stadium cheering. Nervous but unnerved. Tightening the gloves. Performing the penalty ritual, goalkeeper looks at the striker. His body language, the prior data, the body posture, direction the ball stripes are, everything indicates that the shot will be taken for the top-left bin. Goalkeeper taps the bar over him and spreads his body to fly all the way to the top-left post. The whistle blows and GOOOAAALLLL! 
Typical scenario. Penalty kicks have 50/50 chance of conversion and saved. But development of data-driven match analysis can easily predict where the ball will be bagged, all thanks to the Bayesian inference. Before penalty shootout, every goalkeeper gets a flyer where the conversion probabilities are noted down. Still the decision is on the goalkeeper and the level of strategy the taker and keeper in. We all look at the third dimensional jump and kick moments which gets us at the top of our nerves. However, the game is actually played inside the head. The adaptation and the evaluation of the opponent strategy, inferring the next move. This is called the adaptive mentalization. This not only depends on the interaction with the surrounding but also active strategic level thinking of opponent choice and opponent’s thoughts. A paper from *Nature Neuroscience* shows how human updates the strategy also inferring the strategy the opponent is using the technique called adaptive mentalization. There was previous study on mentalization using static approach which was volatile and limited to a small boundary. But the paper [*A neural signature of adaptive mentalization*]((PDF) A neural signature of adaptive mentalization) dynamic study shows how with time human updates their prior belief continuously with interaction. It not only the interaction but how the brain actively participating in the extreme mental computation. Further, the study showed social brain network of mentalization and how this can differentiate between persons who are actually mentalizing and who are mimicking the game. 
## Experiment
Before diving into the experiment, let’s talk about the basics of the experiment. 
# Static vs Dynamic Study: 
Static study is the simple study of false-belief and theory of mind. Which tells what others think about a situation. However, it is a one-way approach to understand the mind. To get the complex understanding and mathematical reasoning of human mind, the different dimensional approach is necessary where there will be constant change of scenario and updates of a prior belief. This takes us to the fundamental **theory of Bayes** or we can say Bayesian inference. It means prior belief updates with posterior beliefs or newer events. This belief update is what we call learning. The belief update occurs based on the surprising move from opponent which also calls **Action Prediction Error.** It used **KL (Kullback-Leibler) Divergence.** It measures how two different probability distributions are. In the experiment, KL divergence quantifies the amount of belief change with each round. If the divergence is large, the update is big and vice versa. 

# CHASE 
Cognitive Hierarchy assessment integrated cognitive neuroscience learning rules with behavioral economics bounded rationality. Here, participants played RPS or Rock-Paper-Scissor. For mathematical modelling, the game was kept simple by only picking 1,2 and 3 instead of rock-paper-scissors. *Winning rule:* Participants beat opponents if the number they chose comes just before their opponent’s number in a circle (e.g., 2 beats one, 1 beats 3). If the number is same then the game is tie. 
To win this type of game, complete randomness is crucial. However, Nash equilibrium begs to differ. It states that no human is complete random. To some extent, human always follow a specific pattern. If opponents get the strategy or exploit the habit, they can beat the participant. This brings us closer to the strategic level of reasoning. 
**Strategic Level** | **Meaning**
Level 0 | Follows *Markovian updating* where belief update occurs based on only current state. 
Level 1 | Assumes opponent is at level 0 and tries to outsmart the simplest pattern.
Level 2 | Assumes opponent is at level 1. (e.g., What opponent thinks I am doing and exploit with a counter move)
*Participants played with both human and machine/algorithm. They were asked later about the humanness of their opponent. This is important because adaptive mentalization with the perception of genuine interaction with human. This was validated so that participants do not assess a simple machine-learning or non-social problem.*
If a participant think they are simply playing with a computer program, the whole study will just be a static puzzle to be solved. By ensuring the humanness, researchers ensured that participants are actively jumping into recursive reasoning (e.g., “I think that you think…”). Humanness is vital in defining non-strategic play, which is the baseline for the entire CHASE model. researcher further validated that humans naturally track action frequencies to define a non-strategic opponent. Since the CHASE model assumes that human builds their strategy on top of their opponent’s level of reasoning, humanness is what makes the higher-level recursive steps possible. 
**Trial Sequence:** Each round of the game, fMRI session followed a three phase sequence.
-	Fixation Phase: Waiting period to prepare for the trial. 
-	A window where the participant decides next move.
-	A 2 second window to reveal the choice of the opponent. This is where action prediction error and belief update occurs.  
Now coming back to the previous scenario, striker was at level 2 of strategy. He already had in mind that the goalkeeper figured out his move. So, he updated his belief, adapted the scenario and strategize a completely different scenario to score the goal. This shows how prior belief updated to posterior belief, even before that actually occurred. No action prediction error and a wonderful match winner to victory. This is called adaptive mentalization. 

# Computational Cycle
![Fig](/assests/image.png)

# The Social Brain Network
During CHASE model, a gamma parameter was taken to indicate the sensitivity of a person to to their opponent’s strategy shift. This shows individual with higher gamma parameter has significantly stronger functional connectivity with the region rTPJ (right Temporoparietal Junction) to 15 different regions of human brain. 

# Machine Learning Model
The whole-brain fMRI pattern taken from the CHASE model used for further study. Two different technique was deployed for the mathematical computation.
-	**LASSO-PCR:** This algorithm looks at the fine-grained patterns across individual voxels and assign weights to each based on the activity correlates with the BU (Belief Update) value which was derived from the CHASE model (KL divergence). 
-	**Support Vector Machine:** It calculates which level of recursive reasoning the participant is from 0 to 2. 
-	**Dot Product:** The BOLD or Brain Oxygen-Level Dependent responses were detected using the using fMRI. Dot Product of these response data and the learned weight from the LASSO-PCR model was calculated. The result of all voxels were summed up to get a one single numerical value: the magnitude of the neurally predicted belief update. 
**Why the Multivariate Machine Learning?**
-	Multivariate model has superior predictive accuracy. Voxel level decoding nearly doubled  the amount of variance to 67.9% from 34.8% that only looked the average activity at the region. 
-	It captured neural codes like ventral to dorsal spatial gradient rTPJ and center-surround patterns in the dmPFC (Dorsomedial prefrontal cortex).
-	The goal was to create a neural signature that is consistent across a group of individuals. The machine learning model successfully predicted the belief updates of “unseen” participants due to cross-validation using LOSO. 

## Findings
The study showed that adaptive mentalization is not only a job of specialized social brain network which includes regions like rTPJ, dmPFC, AI, dlPFC, dACC and amygdala. But, it is a coexistence of a distributed network engaging multiple cognitive systems. After that, the model was tested on completely different demographic to see how the replication sample performed against the discovery sample. The correlation of predicted BU and actual BU for replication sample reduces from 0.82 to 0.67. This proves a neurobiological signature of human adaptive mentalization. 
## Thoughts
This proves adaptation. How human interacts by inferring the next move of others. Even while listening to someone, human consistently tries to predict what others will say the next second. This is the common scenario. Researcher also added the clinical implication to detect autism disorder where patients have disorders during interaction. This leads to an interesting question what we can achieve using belief update magnitudes? Its significance has big value. How economical decisions especially microeconomic decisions can be analyzed or even understanding a penalty kick conversion using only brain data? Although, no player would let that data to go to public. This led to the most important question of the review, how the brain data will actually be used in the upcoming era if not using it for unjust purpose?

