# Breast Cancer Diagnosis: Bootstrap Validation of Logistic Regression

## Overview

This project evaluates the stability and reliability of logistic regression for classifying malignant and benign breast tumors using the Wisconsin Diagnostic Breast Cancer (WDBC) dataset. Multiple bootstrap resampling techniques were used to assess coefficient stability, quantify uncertainty, and compare bootstrap-based inference with traditional analytical methods.

## Objective

Evaluate the reliability of logistic regression estimates for breast cancer classification and determine which tumor characteristics provide stable, reproducible predictive signals across different resampling methods.

## Dataset

**Wisconsin Diagnostic Breast Cancer Dataset**

The analysis uses nine mean tumor characteristics derived from digitized images of fine-needle aspirate (FNA) biopsies:

- Radius
- Texture
- Perimeter
- Smoothness
- Compactness
- Concavity
- Concave Points
- Symmetry
- Fractal Dimension

**Outcome:**
- Malignant
- Benign

## Tools & Methods

- R
- Logistic Regression
- Nonparametric Bootstrap
- Parametric Bootstrap
- Residual-Based Bootstrap
- Statistical Inference
- Confidence Interval Estimation
- Model Validation
- ggplot2
- dplyr
- tidyr

## Analysis

A logistic regression model was fit using nine tumor characteristics to predict malignancy. To evaluate the stability of the model's coefficient estimates, three bootstrap procedures were implemented with **2,000 replications each (6,000 total resamples)**:

1. **Nonparametric Bootstrap** – Resampled observations from the original dataset with replacement.
2. **Parametric Bootstrap** – Simulated new binary outcomes using probabilities estimated by the fitted logistic regression model.
3. **Residual-Based Bootstrap** – Resampled model residuals to generate new probabilities and simulated outcomes.

Bootstrap standard errors, bias estimates, and 95% percentile confidence intervals were compared with traditional Wald-based inference.

## Key Findings

- **Mean texture, mean smoothness, and mean concave points** were consistently significant across all three bootstrap methods, with 95% confidence intervals remaining above zero.
- **Mean concavity** showed a positive association under the nonparametric bootstrap, but its confidence intervals included zero under the parametric and residual-based methods, suggesting a less robust effect.
- Radius, perimeter, compactness, symmetry, and fractal dimension showed greater uncertainty, with confidence intervals overlapping zero across all three bootstrap methods.
- Parametric and residual bootstrap standard errors generally aligned closely with analytical Wald estimates.
- The nonparametric bootstrap produced somewhat larger uncertainty estimates for several coefficients.
- Overall, the different inferential approaches largely agreed on which predictors demonstrated the most stable associations with malignancy.

## Bootstrap Coefficient Distributions

![Bootstrap Distributions](images/bootstrap_distributions.png)

The distributions of coefficient estimates across the three bootstrap methods provide a visual assessment of model stability. Mean texture, mean smoothness, and mean concave points demonstrated consistently positive distributions, while several other predictors showed substantially greater variability.

## Analytical vs. Bootstrap Inference

![Wald vs Bootstrap Comparison](images/bootstrap_comparison.png)

Comparison of analytical Wald estimates with bootstrap-based standard errors and confidence intervals demonstrates broad agreement across methods while highlighting differences in uncertainty for less stable predictors.

## Skills Demonstrated

- Statistical Modeling
- Logistic Regression
- Bootstrap Resampling
- Model Validation
- Statistical Inference
- Uncertainty Quantification
- Data Visualization
- Reproducible Analysis
- Biomedical Data Analysis
- R Programming

## Repository Contents

- 📄 [Final Analysis Paper](Breast_Cancer_Boostrap_Analysis.pdf)
- 💻 [R Analysis](YOUR_CODE_FILE.R)
