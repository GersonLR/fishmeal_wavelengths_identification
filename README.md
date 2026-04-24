
# Identification of Important Wavelengths for Fishmeal Protein Estimation

Python implementation of the methodology presented in:

**Identification of most important wavelengths in the spectral signature for on-line estimation of protein in anchoveta fishmeal (Engraulis ringens)**

This repository contains the implementation of wavelength selection methods applied to hyperspectral reflectance data for protein estimation using Partial Least Squares (PLS).

---

## Project overview

The objective of this project is to identify the most relevant wavelengths within the spectral range:

**400–900 nm**

to estimate fishmeal protein content using:

- Partial Least Squares (PLS)
- Variable Importance in Projection (VIP)
- Backward Variable Elimination (BVE)
- Grid Search Moving Window (GSMW)

The methodology enables reducing the number of wavelengths while maintaining predictive performance.

---

## Repository structure

```
fishmeal_wavelengths_identification/
│
├── Analisis_descriptivo.ipynb
├── Analisis_estadistico_comparacion.ipynb
│
├── PLS_completo/
├── PLS_VIP/
├── PLS_BVE/
├── PLS_GSMW/
```

### Description

**Analisis_descriptivo.ipynb**
Exploratory data analysis:

- spectral signatures
- normalization
- protein distribution

**Analisis_estadistico_comparacion.ipynb**
Model comparison:

- Full PLS
- VIP-PLS
- BVE-PLS
- GSMW-PLS

Evaluation metrics:

- R²
- RMSE
- Q² cross-validation

**PLS_completo**
Baseline model using all wavelengths

**PLS_VIP**
Feature selection based on VIP ≥ 1

**PLS_BVE**
Iterative elimination using regression coefficient magnitude

**PLS_GSMW**
Optimal spectral window detection using moving window grid search

---

## Dataset characteristics

Samples: 122 fishmeal samples  
Spectral range: 400–900 nm  
Channels: 240 wavelengths  

Reference protein values obtained using:

Kjeldahl method

Preprocessing:

L2 normalization applied to spectral signatures

Dataset split:

75% training  
25% testing

---

## Workflow

```
Normalization
↓
Train/test split
↓
Cross-validation (Q²)
↓
PLS regression
↓
Variable selection (VIP, BVE, GSMW)
↓
Performance comparison
```

---

## Results summary

Feature selection methods reduce dimensionality while maintaining prediction accuracy.

Best trade-off:

**BVE-PLS**

Uses fewer wavelengths with performance comparable to full-spectrum PLS.

Suitable for:

real-time industrial implementation

---

## Requirements

Install dependencies:

```
pip install numpy pandas matplotlib scipy scikit-learn
```

---

## Citation

If you use this repository, please cite:

La Rosa G., Valdiviezo J., Soto J.

Identification of most important wavelengths in the spectral signature for on-line estimation of protein in anchoveta fishmeal

---

## Author

Gerson La Rosa  
Universidad de Piura  
Peru

---

## Contact

gerson.larosa@udep.edu.pe
