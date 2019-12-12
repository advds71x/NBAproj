---
layout: post
title: Statistical Models
description: Statistical Models
image: assets/images/model.png
nav-menu: true
permalink: /model
---
## Why Not Machine Learning Models
- Better Interpretation: infernce and prediction
- Prediction Accuracy: achieve similar performance compared to tree-based ML models
- Time Saving
  - save training time
  - no need for parameter tuning, cross-validation

## Model Formulation

$$ logit[Pr(i \succ j \ \text{in game} \ k)] = \lambda_i - \lambda_j + \delta \cdot I(i \in adv)+ \gamma^{\top} z_{ij}
$$

## Evaluation Metric

Cross-Entropy Loss

$$ \mathcal{L} = - \sum_{i=1}^N y_i log(\hat{p_i})+(1-y_i) log(1-\hat{p_i}) $$

## Prediction Results
<div class="row">
	<div class="6u 12u$(small)">
		<h3>Model Summary</h3>
		<span class="image fit"><img src="assets/images/model_summary.png" alt="" height ="600" /></span>
	</div>
	<div class="6u$ 12u$(small)">
		<h3>Player-Level: Prediction Accuracy</h3>
		<span class="image fit"><img src="assets/images/confusion_mat.png" alt="" height ="600" /></span>
	</div>
</div>



## Model Checking

- Overdispersion: quasi-likelihood approach
