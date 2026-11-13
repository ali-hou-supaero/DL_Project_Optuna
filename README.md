# Optuna — Automated Hyperparameter Optimization

A teaching demonstration by **Ali Houssenaly**, prepared in the SUPAERO SDD context, showing how Optuna selects models and tunes hyperparameters.

## Demonstrations

1. **Classical machine learning on Fashion-MNIST:** classifier selection among SVC, Random Forest and Gradient Boosting, with an accuracy objective.
2. **Neural networks on Fashion-MNIST:** tuning a feedforward network's architecture, dropout, optimizer and learning rate.
3. **Heart-risk hackathon extension:** CatBoost optimization with an F1 objective.

The [notebook](demo_code.ipynb) implements Optuna studies, search spaces and visualization. Its saved numerical results and leaderboard comparisons are historical observations, not independently rerun benchmarks.

## Contents

- [demo_code.ipynb](demo_code.ipynb) — complete demonstration.
- [Presentation](DL_Project_Optuna_Presentation.pdf) — accompanying slides.
- [Optuna paper](optuna_paper.pdf) — reference material; credit belongs to its authors.

## Setup

Use Jupyter with Python, Optuna, scikit-learn, NumPy, pandas, PyTorch, torchvision and CatBoost. The notebook also imports Optuna's CatBoost integration and visualization modules; install compatible integration/visualization dependencies for your chosen Optuna version. Dependencies are not version-pinned in this repository.

Fashion-MNIST requires dataset access/downloads. For the third demonstration, download the original hackathon data from the [shared Google Drive folder](https://drive.google.com/drive/folders/106h8NLhxBq4la_aS8UOWMZ1iu9fthQ5i?usp=drive_link). Access to this external folder has not been verified.

Place the files as follows:

```text
DL_Project_Optuna/
├── demo_code.ipynb
├── DL_Project_Optuna_Presentation.pdf
├── optuna_paper.pdf
└── mini-hackathon-data/
    ├── train.csv
    └── test.csv
```

Launch Jupyter from the repository root and execute cells in order. Review the trial counts before launching a study: runtime depends on the hardware, dataset and search space. The third section depends on the additional hackathon data.

## Reproducibility and scope

This is an educational demonstration rather than a production tuning service. No automated tests or verified locked environment are provided. Keep training, hyperparameter selection and final test evaluation separate when extending the experiments.
