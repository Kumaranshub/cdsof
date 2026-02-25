## Dataflow Overview

The CDSOF system processes information through a staged pipeline beginning with workflow generation and ending with optimized workflow selection. Each stage consumes structured inputs and produces outputs that feed subsequent stages. The dataflow model ensures traceability of decisions and reproducibility of results.

## Workflow Generation Stage

The optimizer generates workflow descriptors representing candidate pipelines. Each descriptor contains transformation definitions, feature operators, model configuration, and validation strategy. These descriptors are submitted to the execution layer for evaluation.

## Execution Stage

The executor receives workflow descriptors and dataset references. It applies transformations, constructs features, trains models, and computes validation metrics. Execution outputs include performance scores, variance estimates, runtime measurements, and resource usage data.

## Objective Evaluation Stage

Execution outputs are passed to the objective layer. This layer computes scalar or vector scores that quantify workflow fitness. These scores allow workflows to be ranked and compared across iterations.

## Aggregation Stage

Evaluation results are collected and stored in a central results store. This store maintains workflow configurations, metrics, and timestamps. Aggregated data supports convergence analysis, reproducibility, and experiment auditing.

## Feedback Loop

The optimizer consumes aggregated results and updates the search population. High-performing workflows are retained, mutated, or recombined to generate new candidates. This feedback loop continues until convergence criteria are met.

## Traceability

Each workflow evaluation is assigned a unique identifier linking the descriptor, execution metrics, objective score, and runtime metadata. This enables complete reconstruction of optimization history and ensures experiment transparency.
