# Identification of Important Wavelengths for Fishmeal Protein Estimation

This repository contains the Python implementation used in the article: **“Identification of most important wavelengths in the spectral signature for on-line estimation of protein in anchoveta fishmeal (Engraulis ringens)”**

The objective of this project is to identify the most relevant wavelengths in the visible–near infrared spectral range (400–900 nm) for estimating protein content in fishmeal using Partial Least Squares (PLS) regression combined with variable selection methods.

## Project objective

Estimate fishmeal protein content from hyperspectral reflectance data using:
- Partial Least Squares (PLS)
- Variable Importance in Projection (VIP)
- Backward Variable Elimination (BVE)
- Grid Search Moving Window (GSMW)

These methods allow reducing the number of wavelengths required for prediction while maintaining high accuracy.

## Dataset description

The dataset consists of:
- 122 fishmeal samples
- Spectral signature range: 400–900 nm
- 240 wavelength channels
- Protein reference values obtained using the Kjeldahl method

Spectral signatures were normalized using L2 normalization before model training.

## Repository structure
- Analisis_descriptivo.ipynb
- Analisis_estadistico_comparacion.ipynb
- PLS_BVE/
- PLS_GSMW/
- PLS_VIP/
- PLS_completo/

## Description:

- Analisis_descriptivo.ipynb: Exploratory analysis of spectral signatures, protein distribution and normalization process
- Analisis_estadistico_comparacion.ipynb: Comparison between models Full PLS, VIP-PLS, BVE-PLS and GSMW-PLS

## Performance metrics:
- R²
- RMSE
- Q² cross-validation

## Methodology

The repository implements the following workflow:
- Spectral signature normalization
- Train/test split (75% / 25%)
- Cross-validation for component selection
- PLS regression
- Variable selection using: VIP, BVE and GSMW
- Performance comparison between models

## Main results

The BVE-PLS model achieved: similar accuracy to full-spectrum PLS using less than one quarter of wavelengths

This confirms its suitability for real-time industrial implementation.

## Contact
Gerson La Rosa

gerson.larosa@udep.edu.pe

Universidad de Piura

Peru
