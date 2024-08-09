# MMM-Coefficient-Retrieval-Experiment

## Background

Marketers use MMM to determine the efficacy of each of their advertising channels.  While the ability to predict sales might be a nice bonus outcome to a good MMM model, no marketer is going to be happy with an MMM model that correctly predicts sales but inaccurately assesses the efficacy of each advertising channel.

In contrast with the primary purpose of MMM (interence, not prediction), most ML validation methods are intended to assess whether a model makes accurate predictions.  The following are methods intended to assess the accuracy of the predictions:

- train/test sets
- MAPE
- MRSE
- residual analysis (heteroscedasticity, autocorrelation, Durbin-Watson statistic, etc.)

Additional measures that do not directly measure the accuracy of coefficients include:

- measures of multicollinearity such as VIF

## Purpose of MMM Coefficient Retrieval Experiments


Unlike many other ML tasks, the purpose of MMM is to make inferences.  In predictive tasks, it doesn't matter if the coefficients are correct as long as the predictions are close to correct.  This is not true for MMM.  Correct coefficients is the name of the game.  
