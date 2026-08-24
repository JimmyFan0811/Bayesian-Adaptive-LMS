# Bayesian Adaptive LMS

This repository contains MATLAB simulations and analysis of the paper:

**“A Bayesian Step Least Mean Squares Algorithm for Gaussian Signals”**  
by Paulo Alexandre Crisóstomo Lopes, published in *IET Signal Processing* (2020).

The project was completed as part of a graduate-level **Adaptive Signal Processing** course.

## Project Overview

The Least Mean Squares (LMS) algorithm requires an appropriate step size to balance:

- Convergence speed
- Stability
- Steady-state estimation error

The studied Bayesian Step Least Mean Squares (BSLMS) algorithm uses a
**time-varying step size** derived from estimates of:

- Coefficient estimation error variance \(q_w\)
- Measurement noise variance \(q_v\)

These unknown quantities are estimated online using a Bayesian framework.

## Key Concepts

- Least Mean Squares (LMS)
- Adaptive Filtering
- Bayesian Inference
- Kalman Filtering
- Time-Varying Step Size
- Online Variance Estimation
- Monte Carlo Simulation

## My Work

### MATLAB Simulation

Reproduced and evaluated the BSLMS algorithm using **MATLAB**.

The simulations investigate:

- Online estimation of \(q_w\) and \(q_v\)
- Adaptive LMS step-size behavior
- Convergence of coefficient estimation
- Performance under different noise conditions
- Sensitivity to different initial values

### Algorithm Comparison

Compared BSLMS with other adaptive filtering algorithms under both
optimized and non-optimized parameter settings.

The evaluation focuses on:

- Convergence speed
- Mean coefficient estimation error
- Steady-state performance

## LMS and Bayesian Step-Size Selection

The standard LMS update is

\[
\mathbf{w}(n)
=
\mathbf{w}(n-1)
+
\mu(n)e(n)\mathbf{u}(n),
\]

where the step size \(\mu(n)\) controls the convergence behavior.

In BSLMS, the step size is related to the estimated variances \(q_w(n)\)
and \(q_v(n)\), allowing the algorithm to adapt the step size online rather
than using a fixed value.

## Simulation Analysis

The project includes experiments involving:

### Variance Estimation

Analysis of the convergence behavior of the estimated:

- Coefficient-error variance \(q_w\)
- Measurement-noise variance \(q_v\)

### Different Noise Conditions

Simulation of the algorithm under different combinations of
\(q_w\) and \(q_v\) to study their influence on convergence and
coefficient estimation accuracy.

### Initial-Value Sensitivity

Additional experiments were conducted using different initial values
and compared with the results reported in the original paper.

### Comparison with Other Algorithms

BSLMS was compared with several adaptive filtering methods to evaluate
its convergence and steady-state behavior.

## Repository Structure

- `src/`
  - `bayesian_step_lms.mlx` — main MATLAB simulation
  - `bslms_filter_length_experiment.mlx` — additional experiment

- `figures/`
  - simulation and comparison figures

- `docs/`
  - project report

## Tools

- MATLAB
- Adaptive Signal Processing
- Bayesian Estimation
- Numerical Simulation

## Reference

P. A. C. Lopes,  
**“A Bayesian Step Least Mean Squares Algorithm for Gaussian Signals,”**  
*IET Signal Processing*, 2020.
