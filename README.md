# Correcting Heteroskedasticity in Regression Models: Data Transformations and FGLS Methods

## Introduction

Heteroskedasticity, where the variance of residuals varies across observations, is a common issue in regression analysis that can lead to inefficient estimates and unreliable statistical inferences. This project demonstrates how to diagnose and correct heteroskedasticity in a dataset, focusing on both squared and exponential patterns. By leveraging Feasible Generalized Least Squares (FGLS), the goal is to stabilize the variance of the residuals and produce more reliable regression estimates.

This repository contains:
- A Jupyter Notebook that walks through the entire process with Python code.
- An attached dataset (`FGLSData.xlsx`) that can be used to follow along.

## Steps Taken

### 1. Initial OLS Regression
The process begins with fitting an Ordinary Least Squares (OLS) regression model and examining the residuals. Although it is good practice to visualize the residuals at this stage, the focus here is on handling both squared and exponential heteroskedasticity to demonstrate how different patterns of non-constant variance can be addressed.

### 2. Diagnosing Heteroskedasticity
To formally diagnose heteroskedasticity, the Breusch-Pagan test is performed. This test provides statistical evidence for whether the variance of the residuals is constant. A low p-value indicates that heteroskedasticity is present.

### 3. Correcting Squared Heteroskedasticity
For heteroskedasticity that follows a more gradual, polynomial pattern, the variance is estimated using the squared residuals. The dataset is then transformed accordingly, and a new regression model is fit with weighted data to stabilize the variance.

### 4. Correcting Exponential Heteroskedasticity
In cases where the heteroskedasticity appears exponential (where the variance grows or shrinks rapidly), the log of the squared residuals is regressed against the independent variables. The fitted values from this regression are exponentiated and used as weights to transform the original data. The final regression is run without a constant term to account for the adjusted variance structure.

### 5. Visualizing the Corrected Residuals
To confirm the corrections, the residuals are plotted after applying the transformations. The plots show that the variance is now more stable, indicating that the approach effectively handled the heteroskedasticity. Although visualizing the residuals is typically done at the start of the analysis, this presentation highlights the different methods of handling both squared and exponential heteroskedasticity.

## Conclusion and Relevance

Correcting heteroskedasticity is essential in regression analysis because it ensures that the coefficient estimates are efficient and that statistical tests are valid. This project highlights the flexibility of Feasible Generalized Least Squares (FGLS) in addressing various patterns of heteroskedasticity. The Jupyter Notebook included in this repository demonstrates each step of the process with detailed explanations and Python code, allowing these techniques to be applied to other projects.

Understanding how to identify and correct heteroskedasticity is crucial for anyone working with econometrics or data science, as it directly impacts the reliability of regression models.

