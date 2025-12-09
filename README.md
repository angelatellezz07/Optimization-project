# Regularized Regression Optimization

This project implements and compares several optimization algorithms for solving regularized least-squares problems (LASSO, Ridge, Elastic Net, and intermediate \(p\)-norms) using real PHQ-9 depression data. The goal is to study convergence speed, sparsity patterns, stability, and predictive performance across different regularization types.

## Methods Implemented

The notebook includes from-scratch implementations of:

- Gradient Descent (GD)
- Gradient Descent with Backtracking Line Search
- Nesterov Accelerated Gradient (NAG)
- Subgradient Method (for L1)
- ISTA (proximal gradient for LASSO)
- FISTA (accelerated ISTA)

Each method returns:
- Estimated coefficients  
- Objective evolution  
- Runtime per iteration  

## Objective Functions

We solve problems of the form:

$$
F(\beta) = \frac{1}{n}\|y - X\beta\|^2 + \lambda \|\beta\|_p^p,
$$

including the special cases:

- LASSO (\(p = 1\))
- Ridge (\(p = 2\))
- Elastic Net (L1 + L2 combination)
- Intermediate \(p\)-norms (\(1 < p < 2\))

## Analyses Included

- Convergence trajectories across algorithms  
- Sparsity vs. \(\alpha\) for Elastic Net  
- Stability evaluation across folds (correlation and Jaccard overlap)  
- Comparison of LASSO, Ridge, Elastic Net, and intermediate \(p\)-penalties  

