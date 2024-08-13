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

MMM Coefficient Retrieval Experiments are intended as a new validation method, focused specifically on assessing the accuracy of coefficients.  It can be used for several purposes:
1. **Comparing modeling methods**:  Here are some example scenarios:
   - Should you use national-level or DMA-level data?
   - What happens if you group small channels?
2. **Assessing the impact of modeling conditions**
   - Are coefficients as accurate for small channels as for large channels?
   - What is the impact of extra noise on coefficient accuracy?
3. **Idenitfy other metrics that serve as a proxy for coefficient accuracy**
   - Do VIF values correlate with coefficient accuracy?

## Description of MMM Coefficient Retrieval Experiments

1. Gather real independent variable data
2. Generate synthetic coefficients using random numbers
3. Multiply synthetic coefficients by independent variables.  Then add up results to get synthetic dependent variable.
4. Add random noise to dependent variable.
5. Train regression model in an attempt to retrieve synthetic coefficients.  Assess accuracy of trained coefficients.
6. Repeat steps 2-5 numerous times to get a distribution of outcomes.
