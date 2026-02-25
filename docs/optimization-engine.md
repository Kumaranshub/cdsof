## Search Strategy

The optimization engine performs iterative exploration of workflow space using population-based stochastic search. Each iteration consists of candidate generation, evaluation, ranking, selection, and mutation.

Candidate generation produces diverse pipeline configurations. Evaluation assigns fitness values using the objective function. Selection retains high-performing workflows, and mutation introduces controlled structural changes to explore new regions of the decision space.

## Mutation Operators

Mutation modifies workflow descriptors through localized changes such as replacing transformation operators, adjusting feature dimensionality, switching model classes, or perturbing hyperparameters. These operators balance exploration and exploitation within the search space.

## Convergence Detection

The optimizer monitors improvement of the best workflow score across iterations. If improvement falls below a defined threshold for several consecutive iterations, the search is considered converged. This prevents unnecessary computation once performance stabilizes.
