## Objective Definition

Workflows are evaluated using a composite objective that integrates predictive performance, stability, computational cost, and structural complexity.

Let A(W) denote mean validation performance, Var(W) denote variance across folds, C(W) denote computational cost, and Comp(W) denote structural complexity. The scalar objective is defined as

J(W) = A(W) − λ₁ Var(W) − λ₂ C(W) − λ₃ Comp(W)

where λ₁, λ₂, and λ₃ are weighting parameters controlling trade-offs between accuracy, reliability, and efficiency.

## Metric Rationale

Cross-validation performance approximates expected generalization accuracy. Variance penalization discourages unstable pipelines sensitive to sampling fluctuations. Computational cost is estimated from runtime and parameter counts to discourage inefficient models. Complexity penalization implements structural risk minimization, favoring simpler pipelines when performance is comparable.

## Multi-Objective Extension

The scalar objective may be replaced by a vector objective to enable Pareto frontier analysis. This allows workflows to be compared across multiple dimensions and supports resource-aware deployment policies.
