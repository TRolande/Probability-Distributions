# Probability Distributions, Bayesian Probability & Gradient Descent

## Group 12 Data Science Assignment

This repository contains our implementation for the Data Science Formative Assignment covering:

- Probability Distributions
- Expectation-Maximization (EM) Algorithm
- Bayesian Probability
- Gradient Descent (Manual & Python Implementation)

The project demonstrates both the mathematical foundations and practical implementation of these machine learning concepts using Python.

# Team Members

| Name | Contribution |
|-------|--------------|
| Milena  | README documentation, EM Algorithm implementation, repository management |
| Saam | Bayesian Probability |
| Rolande | Gradient Descent Manual Calculations |
| Colombe| Gradient Descent Python Implementation |

# Assignment Objectives

This project aims to:

- Understand Gaussian Probability Distributions
- Implement the Expectation-Maximization algorithm from scratch
- Apply Bayesian Probability using the IMDb dataset
- Perform manual Gradient Descent calculations
- Convert Gradient Descent into Python code
- Demonstrate understanding through presentation and live prediction

# Repository Structure
Galton-Data-Science-Assignment/

│── Probability_Distributions_&_Gradient_Descent_in_Code.ipynb
│── GaltonFamilies.csv
│── README.md
│── Manual_Calculations.pdf
│── Contribution_Report.pdf

# Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

# Part 1 — Expectation-Maximization (EM)

## Dataset

Galton Families Dataset

Records: **934**

The dataset contains human height measurements which are treated as a mixture of two Gaussian distributions.

## Objective

Instead of manually separating the observations, we use the Expectation-Maximization algorithm to estimate the hidden distributions.

Our implementation includes:

- Gaussian Probability Density Function
- Log-Likelihood computation
- Expectation Step
- Maximization Step
- Parameter Updates
- Convergence Tracking

## Why NOT split at the global mean?

One of the assignment questions asks:

> Should we simply draw a line at the global mean?

Our answer is **No.**

Reasons:

- Real-world data overlap.
- Many observations close to the mean belong to different populations.
- A hard split causes misclassification.
- EM performs **soft assignments**, giving every observation a probability of belonging to each Gaussian.
- This results in much more accurate parameter estimation.

## EM Algorithm Flow

Initialization

↓

Expectation Step

↓

Compute Responsibilities

↓

Maximization Step

↓

Update

- Means (μ)
- Variances (σ²)
- Mixing Coefficients (π)

↓

Compute Log-Likelihood

↓

Repeat until convergence

---

## Optimization Tracking

The notebook prints the optimization table showing:

- Iteration
- Mean 1
- Mean 2
- Variance 1
- Variance 2
- Mixing Coefficients
- Log-Likelihood

This satisfies the assignment presentation requirement.

## Live Prediction Engine

Our prediction engine accepts a random height supplied during presentation.

It automatically:

- Converts units
- Computes posterior probabilities
- Predicts the most likely population
- Displays probability for each class

Example:

Input:
1.51 m

Output:

Probability Group 1:
96.30%

Probability Group 2:
3.70%

Prediction:
Group 1

# Part 2 — Bayesian Probability

This section implements Bayes' Theorem using the IMDb Movie Reviews dataset.

The implementation computes:

- Prior Probability
- Likelihood
- Marginal Probability
- Posterior Probability

using only basic Python operations.

Keywords are selected based on their ability to indicate sentiment.

# Part 3 — Manual Gradient Descent

This section contains handwritten calculations demonstrating:

- Matrix multiplication
- Prediction
- Error computation
- Chain Rule
- Gradient calculation
- Parameter updates

Each group member completed at least one full iteration.

# Part 4 — Gradient Descent in Python

The notebook converts the manual calculations into Python.

Features include:

- Matrix operations
- Gradient computation
- Parameter updates
- MSE calculation
- Gradient verification
- Final prediction

# Visualizations

The completed project includes:

- Parameter change over iterations
- Error reduction plot

These plots demonstrate convergence of the optimization process.

# Learning Outcomes

Through this project we gained practical experience in:

- Gaussian Distributions
- Expectation-Maximization
- Bayesian Inference
- Gradient Descent
- Numerical Optimization
- Python for Data Science

# Contribution Evidence

Each contributor made commits to this repository.

Git history provides evidence of:

- Individual commits
- Feature development
- Documentation
- Code implementation

# Future Improvements

Possible future enhancements include:

- Interactive web interface
- More Gaussian components
- Additional datasets
- Performance benchmarking
- Automatic convergence visualization
