# TP 01 — Leakage-safe intrusion detection with UNSW-NB15

Coursework project for **AI for Cybersecurity**. The notebook builds and evaluates
leakage-safe machine-learning pipelines for intrusion detection using the supplied
UNSW-NB15 train and test splits.

## Contents

- `UNSW_NB15_Lab01_Solution.ipynb` — complete analysis and experiments.
- `Detailed_Report_Ahmed_Mohamed_Houssam.pdf` — project report.
- `TP N°01 3SC.pdf` — assignment brief.

## Experiments

1. Multi-class attack-category classification.
2. Binary normal-versus-attack detection.
3. An imbalance experiment comparing unweighted and class-balanced models for
   the rare `Worms` category.

The notebook evaluates Logistic Regression and Random Forest models, selects
settings with a stratified validation split using macro F1, and reserves the
supplied test split for final scoring. Preprocessing is fitted inside each
training pipeline to avoid data leakage.

## Run locally

Use Python 3.10+ and install the dependencies:

```bash
python -m pip install -r requirements.txt
jupyter notebook UNSW_NB15_Lab01_Solution.ipynb
```

Download or obtain the two course-supplied datasets and place them beside the
notebook (they are intentionally not versioned):

- `UNSW_NB15_training-set.csv`
- `UNSW_NB15_testing-set.csv`

The notebook also runs in Google Colab; when the files are absent it prompts for
an upload.

## Data

This repository does not redistribute UNSW-NB15 data. Please obtain and use the
dataset according to its licence and your course instructions.

## Reproducibility

All random operations use `RANDOM_STATE = 42`. Run the notebook cells in order.
