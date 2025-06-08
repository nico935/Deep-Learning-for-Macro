
---

# Deep Learning Project

## Overview

This project explores the application of deep learning techniques to solve a classic economic growth model, from Brock and Mirman (1972). The approach follows and adapts methods from Azinovic et al. (2022), utilizing neural networks to approximate the solution to the model.

## Summary

We solve a simple optimal growth model with a single agent who seeks to maximize lifetime utility (log utility), subject to a budget constraint on consumption and savings. 
The model is a simplified, macroeconomic version of the Cobb-Douglas production function, assuming full depreciation for analytical tractability.
We use a Neural Network to approximate the optimal policy. This method comes from physics inspired neural network.

- **Challenge adressed:** Stochasticity can lead to infeasible (e.g., negative) consumption or capital. To address this:.
  - I test the authors method of penalizing infeasible prediction 
  - I introduce a custom scaled sigmoid activation that always enforces the constraint and show it's efficiency.
  - I find that the Neural network does not generalize outside of the interval it is trained on, potentially overfitting. 
---

## References & Use of Other Material

This notebook draws inspiration from [Azinovic et al. (2022)] and their accompanying notebook. Some algebraic explanations and the general structure of the loss function are based on their work.

## Reference

- [Azinovic et al. (2022)] Deep equilibrium nets M Azinovic, L Gaegauf, S Scheidegger - International Economic Review, 2022
