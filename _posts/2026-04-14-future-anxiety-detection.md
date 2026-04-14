---
layout: post
title: "Predicting Possible Anxiety using Machine Learning"
date: 2026-04-14
categories: neuroscience
---

## Keywords
Anxiety onset, GAD, mAD, voting classifier, SMOTE, SHAP, leave-3-groups-out Cross validation, AUROC (Area Under the Receiver Operating curve), Neuroticism, IMAGEN database, Gray matter volume, Striatum, PAG and BNST.   

## Background
Looks like we will soon be in an **utopia** where we will see predictions happening based on the psychometrics. Those we are having now will determine what we will be in after 4 to 6 years. Anxiety, stress and panic seem to be the most misunderstood mental disorder for many. However, a study from Nature journal [Link](https://www.nature.com/articles/s41380-022-01840-z) shows that teen agers of 14, with psychometrics and MRI brain scans, after 4 to 8 years were diagnosed. The IMAGEN database was developed based on two types of data. The psychometrics and the brain images. This data was taken to predict future anxiety. The result was fascinating. The study claimed that 13 traits of emotion and 14 specific regions in the brain that controls fear and emotions can be analyzed to pre-diagnose a potential anxiety patient.  
However, the causation was established based on two different signs. The psychometric evaluation made sure the traits such as neuroticism (drawing towards negative emotion), hopelessness and emotions are responsible for future anxiety (FuA). Brain images suggested that regions such as PAG (periaqueductal gray), striatum and amygdala with larger volume have presence in the clinically diagnosed anxiety patients. Also, a region known as BNST or Bed Nucleus of the Stria Terminalis often signaled that its larger volume only existed in the healthy control group. 

## Experiment
-	**IMAGEN Database:** This is known as the large-scale, longitudinal, European research project designed to study adolescent brain development, behavior, and mental health, focusing specifically on 14-year-olds at baseline. It combines neuroimaging (MRIs), genetics, and detailed psychometric assessments  
-	Using **leave-3-groups-out cross validation**, only five cities of data were taken to train a machine learning model and three cities of data to test on it so that the model can be generalize to new and unseen data.
-	The machine learning model was basically a voting algorithm that included logistic regression, support vector machine and random forest. These models worked together to decide whether any 14 years old has a potential anxiety disorder or not.
-	As the data has significant imbalance, with healthy control group and diagnosed participants, **SMOTE** was used to balance the group to suppress any biasness towards the huge healthy control group. 
-	Finally, **SHAP or Shapley Additive Explanation** was used to see exactly how much each specific clue (e.g. neuroticism, hopelessness or brain region volume) influenced the risk score. SHAP basically tagged a weight to any of the variable of interest based on the contribution. A positive SHAP meaning the feature pushed the value toward **future anxiety**. Negative SHAP represented the opposite.

__ | **Pooled Anxiety** | **GAD** | **mAD**
**Primary Driver** | psychometrics | Striatum | Mixed
**Top Risk Feature** | neuroticism, hopelessness | caudate, pallidum | neuroticism, PAG
**Top Protective Feature** | BNST | Insula, Mid- cingulate | Caudate 


## Findings
-	**General (Pooled) anxiety:** Predictions almost entirely relied on the psychometric evaluation. The brain MRI data didn’t improve the AUROC for general category. 
-	**GAD:** Unlike the previous one, brain structure was a key predictor here. Larger gray matter volumes in caudate and pallidum and parts of striatum played significant role to future diagnosis. 
-	**mAD:** Those who developed more than one disorder, a brain region known as periaqueductal gray emerged as a significant predictor alongside neuroticism. 
-	Healthy control group had larger volume of BNST as previously mentioned. 

## Thoughts
Mostly, personality trait is the main decoder that has clear connection with the future diagnosis. With recent development and improvement of AI, it is possible to go beyond that. In the world of social media, where each day we have new trends to compare us. It is possible for people to generate new types of anxiety symptoms out of bolt from the blue. However, the study can be taken further with advancement of more fMRI images and better decision-making model of attention based deep learning. Accuracy may drop but there could be significantly better chances of proper diagnosis and could also detect outliers. 

## References
-	[ Anxiety onset in adolescents: a machine-learning prediction | Molecular Psychiatry)](https://www.nature.com/articles/s41380-022-01840-z)
