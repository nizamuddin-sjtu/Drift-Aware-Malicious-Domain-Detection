# Drift-Aware Malicious Domain Detection

Malicious-domain detection with leakage-aware splits, calibration, drift analysis, and low-FPR evaluation.

## Overview

This notebook studies malicious-domain detection using both raw domain records and a processed 23-feature dataset. It emphasizes leakage-aware evaluation, distribution drift, calibration, ultra-low false-positive operating points, and reviewer-oriented statistical analysis.

## Highlights

- Random, deduplicated, and rounded-hash group splits
- XGBoost, MLP, and FT-Transformer-style baselines
- Temperature, Platt, isotonic, and target-time calibration
- Bootstrap confidence intervals and runtime analysis

## Notebook

The full experiment is provided in [ieee-explore-paper.ipynb](ieee-explore-paper.ipynb). It is configured for Kaggle and expects the datasets described in the notebook to be attached through the **Add Input** panel.

## Running the experiment

1. Create a Kaggle notebook or open the included notebook in Jupyter.
2. Attach the required dataset and enable a GPU accelerator where noted.
3. Install the listed dependencies.
4. Run the notebook from top to bottom.

```bash
pip install -r requirements.txt
```

Datasets, trained weights, and generated experiment outputs are not stored in this repository.

## License

This project is available under the MIT License.
