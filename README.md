# mean-variance-portfolio-optimization
# Mean–Variance Portfolio Optimization

This project implements and compares multiple optimization algorithms for solving the classical mean–variance portfolio optimization problem under simplex constraints.

## Problem

We solve:

min (1/2) w^T Σ w − λ μ^T w  
subject to:  
w ≥ 0,  1^T w = 1  

where:
- w: portfolio weights
- Σ: covariance matrix
- μ: expected returns
- λ: risk aversion parameter


## Methods Implemented

### 1. Projected Gradient Descent (PGD)
- Projection onto simplex
- Guaranteed feasibility at each iteration

### 2. Penalty Gradient Descent
- Converts constraint into penalty term
- Studies trade-off between feasibility and conditioning

### 3. Augmented Lagrangian Method (ALM)
- Combines Lagrangian + penalty
- Achieves fast convergence and exact constraint satisfaction


## Key Results

- PGD and ALM converge to identical solutions (up to numerical precision)
- Penalty method requires large λ_p but suffers from slow convergence
- ALM achieves:
  - Near-zero constraint violation
  - Fast convergence
  - High numerical stability


## Experiments

- Objective convergence vs iterations
- Constraint violation analysis
- Weight comparison across methods
- Approximation error vs penalty parameter


## KKT Equivalence

We verify equivalence between:
- Scalarized formulation
- Target-return formulation
- Risk-budget formulation

All produce identical optimal solutions (up to tolerance), confirming KKT conditions.


