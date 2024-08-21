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
1. **Comparing modeling methods**:  
   - Should you use national-level or DMA-level data?
   - What happens if you group small channels?
2. **Assessing the impact of modeling conditions**
   - Are coefficients as accurate for small channels as for large channels?
   - What is the impact of extra noise on coefficient accuracy?
3. **Idenitfy other metrics that serve as a proxy for coefficient accuracy**
   - Do VIF values correlate with coefficient accuracy?

## Description of MMM Coefficient Retrieval Experiments

1. **Gather real data** for independent variables
2. **Generate synthetic coefficients** using random numbers
3. **Create synthetic dependent variable**.  Multiply synthetic coefficients by independent variables.  Then add up results to get synthetic dependent variable.
4. **Add noise** to dependent variable.
5. **Retrieve synthetic coefficients with regression**.  Assess accuracy of trained coefficients.
6. **Add data for analysis** to be able to analyze relationship between retrieved coefficient accuracy and other factors.
7. **Repeat steps 2-6** numerous times to get a distribution of outcomes.

### Gather Data
1) Gather Real Data

### Define Functions for MMM Coefficient Retrieval Experiments

Steps 2-6 define functions that will be used in the loop in Step 7.  At the end of each cell block in Steps 2-6 I show a sample output of the function to make the code more understandable.

2) Create Synthetic Coefficients
3) Create Synthetic Dependent Variable
4) Add Noise
5) Retrieve Synthetic Coefficients with Regression
6) Add Data for Analysis

### Conduct MMM Coefficient Retrieval Experiments
7) Loop Steps 2-6

### Analyze Results (2 Examples)
8) Analyze the relationship between retrieved coefficient accuracy and other factors. <br>

    Example 1: Examine effect of independent variable contribution on coefficient accuracy. <br>
    Example 2: Examine the relationship between VIF and coefficient accuracy.
