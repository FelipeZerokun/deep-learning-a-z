# Deep Learning A–Z: Software Engineering Practice

Seven deep learning projects based on the Udemy course
[Deep Learning A–Z](https://www.udemy.com/course/deeplearning/),
updated with reproducible environments, automated checks,
and a shared GitHub development workflow.

## Purpose

I have previously completed these projects. This collection revisits
them to practice two skills:

1. Developing small deep learning projects with professional
   software engineering practices.
2. Coordinating and maintaining multiple independent projects
   within one GitHub repository.

The intended timeframe is a few days to one week. Implementation
and tooling will remain proportional to the size of the projects.

## Scope

Each project will include:

- A documented objective and expected inputs and outputs.
- An independent Python environment managed with uv.
- Reusable code for its main workflow.
- Appropriate data preprocessing and model evaluation.
- Ruff for linting and formatting.
- mypy for type checking project code.
- pytest for meaningful automated tests.
- Instructions for running the project.
- Documented results and limitations.

The collection will use GitHub Issues, short-lived branches,
pull requests, and GitHub Actions to practice coordinated development.

## Projects

| Project | Focus | Documentation |
|---|---|---|
| 01 — ANN | Bank customer churn probability | [README](01_ANN/README.md) |
| 02 — CNN | Image classification | [README](02_CNN/README.md) |
| 03 — LSTM | Stock-price time-series prediction | [README](03_LSTM/README.md) |
| 04 — SOM | Anomaly detection in credit application data | [README](04_SOM/README.md) |
| 05 — Hybrid Model | Combining a SOM with a neural network | [README](05_Hybrid_Model/README.md) |
| 06 — Boltzmann Machine | Binary movie-preference recommendations | [README](06_Boltzmann_Machine/README.md) |
| 07 — Autoencoder | Movie-rating prediction | [README](07_Autoencoder/README.md) |

Each project's README defines its specific scope, execution
instructions, evaluation, and limitations.

## Repository Strategy

This is a monorepo: one Git repository containing seven
independent Python projects.

- `main` contains accepted work from all projects.
- Each project manages its own dependencies through
  `pyproject.toml` and `uv.lock`.
- Virtual environments, caches, and generated artifacts
  are excluded from Git.
- Shared development conventions apply across the collection.
- Projects are developed one at a time.

Dataset sources and access instructions will be documented.
Course materials and datasets will only be redistributed
where permitted.

## Development and Coordination

This is a solo project that practices team responsibilities:
planning, implementation, review, and release.

The workflow is:

1. Create a GitHub issue with a clear outcome and acceptance criteria.
2. Create a short-lived branch for the task.
3. Implement the change and relevant tests.
4. Run local quality checks.
5. Open a pull request and perform a documented self-review.
6. Merge after the applicable automated checks pass.
7. Update documentation and close the issue.

One GitHub Projects board tracks work across the collection:

Backlog → Ready → In progress → In review → Done

Project labels identify which project a task belongs to.
Slack is used for brief coordination exercises and milestone
announcements, with links to the relevant GitHub records.

## Tools

| Tool | Responsibility |
|---|---|
| Git and GitHub | Version control and change review |
| GitHub Issues and Projects | Task planning and progress tracking |
| GitHub Actions | Continuous integration |
| uv | Python environments and dependency management |
| Ruff | Linting and formatting |
| mypy | Static type checking |
| pytest | Automated testing |
| TensorFlow / PyTorch | Deep learning implementation |
| Slack | Coordination and milestone communication |

Additional tools will only be introduced when necessary
to complete the defined scope.

## Testing and Continuous Integration

Automated checks will cover formatting, linting, type checking,
and meaningful software behavior.

Tests will focus on relevant risks, such as invalid inputs,
preprocessing behavior, and prediction interfaces.

Model quality will be evaluated separately using suitable
held-out data and project-specific metrics.

Full model training will not be required on every pull request.
CI will be expanded as each project is implemented.

## Definition of Done

An individual project is complete when:

- Its documented workflow runs successfully.
- Dependencies and execution instructions are recorded.
- Relevant automated checks pass.
- Model evaluation results and limitations are documented.
- Its implementation has been reviewed through a pull request.
- Setup and execution have been verified in a clean environment
  with the required data available.

The collection is complete when all seven projects meet these
criteria and the root documentation accurately describes them.

## Out of Scope

For this iteration:

- Production deployment or cloud infrastructure.
- Permanent branches for simulated teams.
- Comprehensive experiment-tracking infrastructure.
- Extensive hyperparameter optimization.
- Building shared abstractions without a demonstrated need.

## Acknowledgments

Project topics originate from Deep Learning A–Z on Udemy.

This repository focuses on my updated implementations and
software development practice. Individual project documentation
identifies relevant datasets and reference materials.