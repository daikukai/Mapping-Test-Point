---
title: 'Advantages and Limitation of using least square method to select ideal function'
tags:
  - Python
  - Ordinary Least Squares
  - Regression Analysis
  - Data Visualization
authors:
  - name: Daikukai Honey Bindah
orcid: 0000-0000-0000-0000     affiliation: International University of Applied Sciences
date: 25 March 2026
bibliography: paper.bib
---
# Summary
The least square method is a commonly used technique to fit the regression line on a dataset, providing an appropriate approach for finding ideal functions. This software implements both theoretical and experimental methodologies to analyze the performance of the least square method in selecting and mapping ideal functions from a provided dataset. While the outcomes indicate that the least square method is a convenient tool, the implementation also highlights its sensitivity to flaws like outliers, dimensionality problems, overfitting, and multicollinearity.

# Statement of Need
In various fields like healthcare, finance, engineering, and education, researchers must select ideal functions to display complex relationships between variables. While Ordinary Least Square (OLS) regression is widely adopted, its performance varies significantly depending on the characteristics of the data. 

This software provides a Python-based implementation using `SQLAlchemy`, `pandas`, and `scikit-learn` to automate the process of:
1. Identifying the best-fitting "ideal functions" from a large set (50 functions) for a given training dataset.
2. Mapping test data points to these functions based on maximum deviation criteria.
3. Evaluating model performance using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2) metrics.

This tool is specifically useful for students and researchers who need a transparent, scriptable way to visualize how OLS handles large datasets and to identify when residuals indicate a violation of model assumptions.

# Mathematical Background
The goal of this method is to reduce the difference between the observed response and the response predicted by the regression line. The software calculates the sum of squared residuals ($SS_{res}$) to measure the level of variance in the residuals:

$$SS\_res=\Sigma(y-\hat{y})^{2}$$

For parameter estimation, the software utilizes matrix algebra to determine the vector of coefficients ($\beta$):

$$\beta=(X^{\prime}X)^{-1}X^{\prime}y$$

# Mentions and Acknowledgements
The research establishes that while the least squares method is a valued approach, it is vital to be aware of its limitations. I would like to acknowledge the resources provided by the International University of Applied Sciences during the development of this research.

# References
- Montgomery, D. C., Peck, E. A., & Vining, G. G. *Introduction to Linear Regression Analysis*.
- James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). *Introduction to statistical learning* (2nd ed.). New York, NY: Springer.
- Hardin, J. W. (2018). *Statistics by Jim*..
- "Least Square Method", *byjus.com*.
- "Least Square", *Cuemath.com*.
