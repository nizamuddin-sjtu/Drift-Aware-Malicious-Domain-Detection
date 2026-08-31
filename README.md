<h1 align="center">Drift-Aware Malicious Domain Detection</h1>

<p align="center">
  <a href="https://doi.org/10.20944/preprints202509.0573.v1"><img src="https://img.shields.io/badge/Paper-Preprint-2f6f9f.svg" alt="Paper"></a>
  <a href="ieee-explore-paper.ipynb"><img src="https://img.shields.io/badge/Notebook-ieee--explore--paper.ipynb-F37626.svg" alt="Notebook"></a>
  <a href="https://www.kaggle.com/nizamuddinmaitlo"><img src="https://img.shields.io/badge/Datasets-Kaggle-20BEFF.svg" alt="Kaggle datasets"></a>
  <a href="https://scholar.google.com/citations?user=bvyKhaEAAAAJ&hl=en"><img src="https://img.shields.io/badge/Publications-Google_Scholar-4285F4.svg" alt="Google Scholar"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/Code_License-MIT-2ea44f.svg" alt="MIT License"></a>
</p>

<p align="center"><b>Nizamuddin Maitlo</b></p>

<p align="center">Malicious-domain detection with leakage-aware splits, calibration, drift analysis, and low-FPR evaluation.</p>

## 🔥 Overview

This notebook studies malicious-domain detection using both raw domain records and a processed feature table. The evaluation emphasizes duplicate control, leakage-aware splitting, temporal and distribution drift, probability calibration, and ultra-low false-positive operating points.

## ✨ Contributions

- Random, deduplicated, and rounded-hash group splits.
- XGBoost, MLP, and FT-Transformer-style baselines.
- Temperature, Platt, isotonic, and target-time calibration.
- Bootstrap confidence intervals, drift indicators, and runtime analysis.

## 🧪 Experimental protocol

- Raw domain records and the processed feature table are detected independently.
- Thresholds and calibration models are fitted without using final test labels.
- Performance is reported under multiple split and drift conditions.

## 📓 Notebook

The complete experiment is implemented in [ieee-explore-paper.ipynb](ieee-explore-paper.ipynb). Data discovery, preprocessing, training, evaluation, and export steps are kept together so the workflow can be reviewed and rerun from top to bottom.

## 🛠️ Installation

Create a Python environment and install the listed dependencies:

```bash
python -m pip install -r requirements.txt
```

The notebook is configured for Kaggle. A CUDA-capable GPU is recommended where GPU training is enabled.

## 📦 Datasets

Datasets, trained weights, and generated experiment outputs are not stored in this repository.

| Resource | Purpose | Link |
|---|---|---|
| Malicious Domain Detection Dataset | Raw-domain and processed-feature evaluation | [Kaggle dataset](https://www.kaggle.com/datasets/nizamuddinmaitlo/malicious-domain-detection-dataset) |

On Kaggle, attach the dataset through **Add Input** before running the notebook. External datasets remain subject to the licenses and terms on their source pages.

## 🚀 Running the experiment

### Kaggle

1. Upload or import [ieee-explore-paper.ipynb](ieee-explore-paper.ipynb).
2. Attach the dataset listed above through **Add Input**.
3. Enable a GPU accelerator when required by the configured model.
4. Run the notebook from top to bottom.

### Local Jupyter

```bash
python -m pip install -r requirements.txt
jupyter notebook ieee-explore-paper.ipynb
```

Dataset paths may need to be changed when running outside Kaggle.

## ♻️ Reproducibility

- Keep the documented train, validation, and test protocol unchanged when comparing models.
- Fit thresholds, calibration parameters, and feature transformations without using final test labels.
- Record the random seed, package versions, accelerator, and dataset version for each run.
- Treat saved tables and figures under the notebook's output directory as generated artifacts rather than source files.

## 📚 Paper information

The publication below is a related malicious-domain study from the same research line. Its distributed deep-forest architecture is distinct from several baselines evaluated in this notebook.

| Publication | Venue | Year | Link |
|---|---|---:|---|
| Efficient Malicious Domain Detection Using a Distributed Deep Forest Algorithm | Preprints | 2025 | [DOI](https://doi.org/10.20944/preprints202509.0573.v1) |

## ⭐ Citation

For research building on this repository, cite the relevant publication or dataset descriptor:

```bibtex
@article{mangi2025maliciousdomain,
  title   = {Efficient Malicious Domain Detection Using a Distributed Deep Forest Algorithm},
  author  = {Mangi, Samar Abbas and Rajper, Samina and Shaikh, Noor Ahmed and Maitlo, Nizamuddin},
  journal = {Preprints},
  year    = {2025},
  doi     = {10.20944/preprints202509.0573.v1}
}
```

## ⚠️ Scope and limitations

Offline splits approximate drift but do not reproduce every live DNS environment. Operational thresholds must be revalidated for local traffic, class prevalence, analyst capacity, adversarial adaptation, and the cost of false positives.

## 📄 License

Repository code is released under the [MIT License](LICENSE). Datasets and publications retain their own licenses and terms.

## 🤝 Acknowledgements

The experiments use public datasets, open-source Python libraries, and Kaggle compute infrastructure. We thank the dataset contributors and software maintainers who support reproducible research.
