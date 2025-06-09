
---

# Partial Differential Equation Solving with Neural Operator: Application to a classical Economic Growth Model
TO-DO
Fix final version commit issue, remove old versions 

## Overview

This project explored the application of deep learning techniques to solve a classic economic growth model, from Brock and Mirman (1972). The approach adapts methods from [1] Azinovic et al. (2022), utilizing neural networks to approximate the solution to the model.

## Summary

We solve a simple optimal growth model with a single agent who seeks to maximize lifetime utility, subject to a budget constraint on consumption and savings. 
The model is a simplified version of the Cobb-Douglas model, assuming full depreciation for analytical tractability.
We use a Neural Network to approximate the optimal policy, with a loss derived from the constraints, similarly to physics inspired neural network.

- **Challenge adressed:** Stochasticity can lead to infeasible (e.g., negative) consumption or capital. To address this:.
  - I test the authors method of penalizing infeasible prediction 
  - I introduce a custom scaled sigmoid activation that always enforces the constraint and show it's efficiency.
---

## Note

After having done this project I realized this was similarly implemented in DeepHAM [2] 

## References & Use of Other Material

This notebook draws inspiration from [Azinovic et al. (2022)] and their accompanying notebook. Some algebraic explanations and the general structure of the loss function are based on their work.

## Reference

- [1] [Azinovic et al. (2022)] Deep equilibrium nets M Azinovic, L Gaegauf, S Scheidegger - International Economic Review, 2022
- [2] [Han et Al 2024] DeepHAM: A Global Solution Method for Heterogeneous Agent Models with Aggregate Shocks 2024.
