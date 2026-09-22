# EEG Analysis

This repository contains exploratory EEG analysis work implemented in Jupyter notebooks. The workflow uses MNE-Python for EEG preprocessing and epoch handling, and scikit-learn for classification experiments.

## Notebook workflow

- `trials/01_epochs_extraction_rev1.ipynb` loads BioSemi BDF recordings, detects event markers, extracts and aligns experimental epochs, assigns condition labels, applies baseline correction and average referencing, visualizes the EEG data, and saves participant epochs as FIF files.
- `trials/02_single_participant_analysis.ipynb` loads one participant's FIF epochs and compares condition pairs (`IC` vs `N`, `IC` vs `C`, and `N` vs `C`) using SVM, logistic regression, and linear discriminant analysis. It reports accuracy, precision, recall, and F1 scores and plots model comparisons.
- `trials/03_group_level_analysis.ipynb` begins the group-level workflow by loading participant epoch files, extracting condition-specific datasets, and preparing data and labels for across-participant classification and statistical analysis.

The remaining notebooks in `trials/` are earlier experiments and alternative versions of the preprocessing and analysis workflow.

## Data

The participant epoch files in `trials/epoch_data/` are intentionally excluded from this public repository. The notebooks expect those files, or equivalent locally available data, when they are run.

## Main tools

- Python
- MNE-Python
- NumPy
- Matplotlib
- scikit-learn
- SciPy
- Jupyter