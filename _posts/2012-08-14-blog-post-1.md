---
title: 'Modeling Dependent Random Variables Using Markov Chains'
date: 2024-02-23
permalink: /modeling_dependent_random_variables_using_markov_chains/
tags:
  - cool posts
---

[Modeling Dependent Random Variables Using Markov Chains is Available on Medium](https://towardsdatascience.com/modeling-dependent-random-variables-using-markov-chains-f363a3be1f9a)

*In my previous article discussing [Maximum Likelihood Estimation of Parameters for Random Variables](https://towardsdatascience.com/maximum-likelihood-estimation-4a1a866dfa70), we acted as a hospital risk manager, senior doctor statistician, data science nurse (I still have literally no idea who would be in charge of this) and developed a simple probability model to estimate our risk of not having enough beds to accommodate new patients. To accomplish this we made the following assumptions:*

*Assume all patients checked in to the hospital will check out same day
Assume patients checked in each day are independent of one another
Though impractical, these assumptions enabled us to model the number of patients in a given day as a Poisson random variable (see [Common Random Variables](https://medium.com/quant-guild/common-random-variables-f30c537a01e4)) which has a well-defined distribution function we may use to estimate the probability of being unable to accommodate a new patient.*

*A quick digression — of course, the Poisson random variable is parameterized by lambda which models the expectation and variance of patients on a given day. We spent a majority of the previous article discussing the best statistical way to estimate this parameter given a set of observed data using the method of maximum likelihood estimation. If you are unfamiliar with this method of choosing an estimator for our parameter estimates I encourage you to check out that article as we will also be applying the idea herein.*

*Incorrect assumptions overestimate or underestimate risk or probabilities depending on the violation. For example, assuming everyone checks in and checks out on the same day underestimates risk as it is likely some patients will stay overnight.*

*This article will be broken up into the following sections.*

*- Introduction to Markov Chains and Transition Matrices*

*- Computing Arbitrary Step Transition Probabilities*

*- Redefining and Solving the Original Problem as a Markov Chain*

*- Absorbing States*

*- Maximum Likelihood Estimation of Transition Probabilities*

*- Calibrating a Transition Matrix to Data and Computing Risk*
