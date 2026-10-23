# Bank Customer Churn Prediction

## Overview

This project uses a simple artificial neural network built with
TensorFlow to estimate the probability that a bank customer leaves,
based on historical customer data.

It is an educational project focused on developing a reproducible
deep learning workflow with software engineering practices and
automated testing.

## Goal

Build a workflow that preprocesses customer data, trains and evaluates
a neural network, and returns a churn probability for an individual
customer.

The target variable is `Exited`:
- `0`: The customer did not leave the bank.
- `1`: The customer left the bank.

## Dataset

Each record describes a bank customer using these fields:

| Field | Description |
|---|---|
| customer_id | Customer identifier |
| surname | Customer surname |
| CreditScore | Customer credit score |
| Geography | Customer geographic category |
| Gender | Customer gender |
| Age | Customer age |
| Tenure | Number of years the customer has been with the bank |
| Balance | Customer account balance |
| NumofProducts | Number of bank products held by the customer |
| HasaCard | Indicator of whether the customer has a credit card |
| isActiveMember | Indicator of whether the customer is an active member |
| EstimatedSalary | Estimated customer salary |
| Exited | Target indicating whether the customer left the bank |

Column names and definitions will be checked against the dataset
during inspection.

## Planned Workflow

1. Inspect the dataset and verify column meanings and data types.
2. Check for missing, duplicate, invalid, or inconsistent information.
3. Select input features and define categorical encoding.
4. Split the dataset into training and validation sets.
5. Fit preprocessing on training data and apply it consistently
   to validation data, including feature scaling.
6. Build a simple neural network using TensorFlow.
7. Train and evaluate the model.
8. Predict the churn probability for one customer observation.

Evaluation metrics and model configuration will be defined during
their respective development stages.

## Engineering Requirements

- Keep preprocessing consistent between training and prediction.
- Fit data-dependent preprocessing only on training data.
- Record dependencies and configuration for reproducibility.
- Add automated tests for preprocessing and prediction behavior.
- Save the trained model and the preprocessing artifacts needed
  for inference.
- Document how to run the implemented workflow.

## Expected Deliverables

- Data preprocessing code.
- TensorFlow model training and evaluation code.
- A prediction workflow for an individual customer.
- Automated tests.
- Dependency and execution instructions.
- Documented evaluation results and limitations.

## Limitations

The dataset's collection date and outcome observation period are
not established. Predictions therefore estimate the supplied
`Exited` outcome without a specific future time horizon.

This project is an educational prototype, not a validated banking
decision system.

## Project Status

Project definition. Implementation has not started.