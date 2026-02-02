# 📂 Dataset Directory

This directory contains the **final, cleaned, and harmonized dataset** used for the Vehicle Damage Severity Assessment project.

Unlike the raw source datasets, the images stored here have undergone a 5-stage data engineering pipeline (Deduplication, Resolution Filtering, Label Correction) and are ready for model training.

## 🗂️ Directory Structure

The dataset follows a standard ImageNet-style directory structure, compatible with PyTorch `ImageFolder` and most Computer Vision frameworks.

```text
data/
├── train/                  # Training Set (~73%)
│   ├── minor/
│   ├── moderate/
│   └── severe/
├── val/                    # Validation Set (~18%)
│   ├── minor/
│   ├── moderate/
│   └── severe/
└── test/                   # Golden Test Set (~9%)
    ├── minor/
    ├── moderate/
    └── severe/

```

## 🏷️ Naming Convention

To ensure a clean structure and remove gaps caused by filtering, all files have been re-indexed using a strict 3-digit schema:

`{split}_{class}_{id}.jpg`

**Examples:**
* `train_minor_001.jpg`
* `val_moderate_021.jpg`
* `test_severe_055.jpg`

> **Note:** Original source prefixes were removed during the final unification step to ensure a cleaner namespace.
