## Breast Cancer Diagnosis: Bootstrap Validation of Logistic Regression
**Overview**
This project evaluates the reliability of logistic regression for classifying malignant and benign breast tumors using the Wisconsin Diagnostic Breast Cancer dataset. Rather than focusing solely on predictive performance, the analysis investigates the stability of model coefficients using multiple bootstrap resampling techniques to validate statistical inference.

**Project Highlights**
- Built a logistic regression model for breast cancer classification
- Conducted 6,000 total bootstrap resamples across three methods
- Compared bootstrap and analytical confidence intervals
- Evaluated coefficient stability, bias, and uncertainty
- Visualized sampling distributions to assess model robustness

**Objective**
Assess whether traditional logistic regression adequately estimates uncertainty by comparing classical Wald inference with bootstrap-based uncertainty estimation.

**Dataset**
Wisconsin Diagnostic Breast Cancer Dataset
Predictors included nine mean tumor characteristics derived from digitized fine-needle aspirate images, including:
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

**Tools**
  - R
  - Logistic Regression
  - Bootstrap Resampling
  - ggplot2
  - dplyr
  - tidyr
  - Statistical Inference

**Methods**
  - Logistic Regression
  - Nonparametric Bootstrap (2,000 iterations)
  - Parametric Bootstrap (2,000 iterations)
  - Residual Bootstrap (2,000 iterations)
  - Bootstrap Confidence Intervals
  - Bias Estimation
  - Standard Error Comparison
  - Density Visualization of Coefficient Distributions

**Key Findings**
- Mean texture, mean smoothness, and mean concave points were consistently strong predictors of malignancy.
- Bootstrap confidence intervals closely matched traditional Wald confidence intervals.
- The three bootstrap approaches produced similar estimates, supporting the robustness of the logistic regression model.
- Bootstrap validation confirmed that classical inference performed well for this dataset.

**Skills Demonstrated**
  - Statistical Modeling
  - Logistic Regression
  - Bootstrap Resampling
  - Model Validation
  - Confidence Interval Estimation
  - Data Visualization
  - Predictive Analytics
  - Medical Data Analysis
