
---

# Deep Learning Project

**Author:** Nicolas Lapautre

## Overview

This project explores the application of deep learning techniques to solve a classic economic growth model, from Brock and Mirman (1972). The approach follows and adapts methods from Azinovic et al. (2022), utilizing neural networks to approximate the solution to the model.

## References & Use of Other Material

This notebook draws inspiration from [Azinovic et al. (2022)] and their accompanying notebook. Some algebraic explanations and the general structure of the loss function are based on their work.


## Summary

We solve a simple optimal growth model with a single agent who seeks to maximize lifetime utility (log utility), subject to a budget constraint on consumption and savings. 
The model is a simplified, macroeconomic version of the Cobb-Douglas production function, assuming full depreciation for analytical tractability.
We use a Neural Network to approximate the optimal policy. This method comes from physics inspired neural network.

- **Challenge with Deep Learning Mehtod:** Stochasticity can lead to infeasible (e.g., negative) consumption or capital. To address this:.
  - I test the authors method of penalizing infeasible prediction 
  - I introduce a custom scaled sigmoid activation that always enforces the constraint and show it's efficiency.
  - I find that the Neural network does not generalize outside of the interval it is trained on, potentially overfitting. 
---

## Acknowledgements

- [Azinovic et al. (2022)] for foundational ideas and code structure.
- [Kahou et al. (2021), Han et al. (2022), Azinovic and Žemlička (2023)] for insights into encoding economic priors and symmetries into network architectures.
