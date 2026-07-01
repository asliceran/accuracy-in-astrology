# Accuracy in Astrology

A statistical analysis investigating whether years of astrological experience predict performance in a blinded natal chart matching challenge using Python, correlation analysis, and linear regression.

---

## Project Overview

This project was completed as part of a statistics course at Minerva University.

The objective was to evaluate a common claim within astrology: whether individuals with more years of experience perform better on an objective astrology challenge. To investigate this, I analyzed participant data from the Clearer Thinking Astrology Challenge using statistical modeling and hypothesis testing.

---

## Motivation

Many people believe that astrology becomes more accurate with experience. I wanted to test this claim empirically by examining whether years of experience are associated with better performance while controlling for belief in astrology. To isolate the effect of experience, the analysis was restricted to participants who reported positive beliefs in astrology.

---

## Research Question

Among astrology believers participating in the Clearer Thinking Astrology Challenge, can years of astrological experience predict performance on a natal chart matching task?

---

## Dataset

The dataset used in this analysis can be found [Clearer Thinking Astrology Challenge Dataset] (https://docs.google.com/spreadsheets/d/1pYd5_I0V12tvB-ogjcHIfk-1K0_Es1VqiFuqkLSd5o8/edit?usp=sharing) The dataset contains responses from participants who voluntarily completed an online astrology matching challenge. For this analysis, only participants with positive belief scores (> 0) were included.

**Variables used:**

* Years of astrological experience
* Belief in astrology
* Number of correct natal chart matches

This restriction was applied to focus specifically on practitioners who actively believe in astrology while reducing the influence of belief as a confounding variable.

---

## Methods

The analysis was performed in Python using:

* Data preprocessing and filtering
* Exploratory data analysis
* Pearson correlation analysis
* Simple linear regression
* Hypothesis testing
* Confidence interval estimation
* Residual and Q-Q plot diagnostics

**Libraries**

* pandas
* numpy
* scipy
* matplotlib
* seaborn
* statsmodels

---

## Key Findings

### Correlation Analysis

Pearson's correlation coefficient was **r = -0.0088**, indicating essentially no linear relationship between years of experience and matching accuracy. The scatterplot similarly showed no meaningful trend between the variables.

<img width="678" height="547" alt="correlation plot" src="https://github.com/user-attachments/assets/d7518026-251c-4b3a-b587-aa4f20331ca8" />

---

### Regression Analysis

A simple linear regression model was used to estimate whether years of experience could predict matching accuracy.

The model explained only **0.01% of the variance** in performance (**R² = 0.0001**), indicating that experience alone provides virtually no predictive value.

Model diagnostics, including residual plots and a Q-Q plot, suggested that the regression assumptions were reasonably satisfied, despite the model having almost no explanatory power.

<img width="729" height="470" alt="regression plot" src="https://github.com/user-attachments/assets/9376df11-f7eb-4d7a-a815-1bc8591d4645" />

---

### Hypothesis Test

To evaluate whether experience significantly predicts performance, a two-tailed hypothesis test was conducted.

**Null Hypothesis (H₀):**
The slope of the regression line equals zero (β₁ = 0), meaning years of experience do not predict matching accuracy.

**Alternative Hypothesis (H₁):**
The slope differs from zero (β₁ ≠ 0).

**Results**

* Standard Error: 0.1115
* t-statistic: -0.091
* p-value: 0.927
* Significance level (α): 0.05

Because the p-value is substantially greater than 0.05, the null hypothesis cannot be rejected. The analysis provides no statistical evidence that years of experience improve performance on this task.

---

### Confidence Interval

The 95% confidence interval for the regression slope was:

**[-0.2313, 0.2109]**

Because this interval includes zero, it supports the conclusion that the true relationship between experience and matching accuracy may be nonexistent. The relatively wide interval also reflects substantial uncertainty in estimating the effect size.

---

## Conclusion

Within this sample of astrology believers, years of experience were not associated with improved performance on a standardized natal chart matching task. Both the regression analysis and correlation analysis indicate that experience alone is not a meaningful predictor of success.

This project also highlights the importance of interpreting statistical models beyond p-values by considering effect sizes, confidence intervals, model assumptions, and practical significance.

---

## Limitations

* The sample size was relatively small.
* Experience was measured only by duration rather than quality or intensity of practice.
* Results are limited to participants in the Clearer Thinking Astrology Challenge and may not generalize to all practitioners.

---

## Skills Demonstrated

* Python programming
* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Correlation analysis
* Linear regression
* Statistical hypothesis testing
* Confidence interval estimation
* Data visualization
* Interpretation of statistical models
