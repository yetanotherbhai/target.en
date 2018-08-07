---
description: Ensemble methods use multiple learning algorithms to obtain better predictive performance than could be obtained from any of the constituent learning algorithms. The Random Forest algorithm in the automated personalization system is a classification or regression method that operates by constructing a multitude of decision trees at training time.
keywords: Targeting
seo-description: Ensemble methods use multiple learning algorithms to obtain better predictive performance than could be obtained from any of the constituent learning algorithms. The Random Forest algorithm in the automated personalization system is a classification or regression method that operates by constructing a multitude of decision trees at training time.
seo-title: Random Forest Algorithm
solution: Target
title: Random Forest Algorithm
uuid: dd8ab459-a651-410a-beb0-f2bf5bc68ca9
index: y
internal: n
snippet: y
translate: y
---

# Random Forest Algorithm

Their output is a class or regression value that is the mode of the outputs by individual trees. The method combines bagging and the random selection of features in order to construct a collection of decision trees with controlled variance. Algorithm 1 (referred to as EDT) outlines how ensemble decision trees are constructed and make predictions.
**Feature Transformation** 
Before the data goes through the algorithm, it undergoes a feature transformation.
The feature transformations depend on the type of feature being used. Mainly, there are two types of features:

* Categorical Categorical features cannot be counted but can be sorted into different groups. They could be features like country, gender, zip code.

* Numeric Numeric features can be measured or counted, such as age, income, and so on. For categorical features, a set of all possible features is maintained and the likelihood transformation is used to reduce the data size. For numeric features, re-scaling ensures that the features are comparable across the board.


**Generalized Score** 
Generalized score is computed per modeling group to compute the general conversion rate of the offer without taking into account the personalized model.
**Combiner** 
Combiner adds the personalized score computed by the random forest algorithm to the generalized score. The random forest score is used when the model is available. However, when the model is not available, Target uses the general score. The general score serves as a backup for the personalized score.
** **Multi-Armed Bandit** ** 
The multi-armed bandit (MAB) problem is a classic example of the exploration vs. exploitation dilemma in which a collection of one-armed bandits, each with unknown reward probability, is given. The key idea is to develop a strategy, which results in the arm with the highest success probability to be played so the total reward obtained is maximized. Multi-armed bandit is used in the system when for online scoring after the online models are built. This helps with online learning during exploration.
The current multi-armed algorithm is epsilon (ε) greedy algorithm. In this algorithm, with probability 1- ε, the best arm is chosen. And, with probability ε, any other arm is randomly chosen.

