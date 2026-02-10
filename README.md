
# Database for Predicting Oxidation Resistance of Refractory High-Entropy Alloys

## Overview

This repository contains the experimental database used in the study *"Advancing Refractory High-Entropy Alloy Development with AI-Predictive Models for High-Temperature Oxidation Resistance"*. The database was designed to train and validate machine learning models for predicting specific mass gain due to oxidation in Refractory High-Entropy Alloys (RHEAs) and Refractory Complex Concentrated Alloys (RCCAs). It is a valuable resource for researchers in materials science, particularly those focusing on high-temperature alloy applications.

## Contents

- `data/`
  - `alloy_oxidation_886_202406.csv`: Contains the experimental data in CSV format.
  - `alloy_oxidation_886_202406.json`: Contains the experimental data in JSON format.
  - `alloy_oxidation_886_202406.pkl`: Trained XGBoost model to infer specific mass gain of an alloy based on its composition during isothermal oxidation as a function of temperature and time.
- `README.md`: Documentation of the dataset.

## Dataset Description

The database comprises **886 observations** from published literature, detailing the following parameters:

1. **Alloy Composition**:
   - Elements: Al, Cr, Hf, Mo, Nb, Si, Ta, Ti, V, W, Zr.
   - Corresponding molar concentrations.
2. **Oxidation Conditions**:
   - Temperature (°C).
   - Time (hours).
3. **Target Property**:
   - Specific mass gain due to oxidation (mg/cm²).

### File Details

#### `alloy_oxidation_886_202406.csv` and `alloy_oxidation_886_202406.json`

| Column Name           | Description                                                |
|-----------------------|------------------------------------------------------------|
| `alloy formula`       | Chemical formula of the alloy.                             |
| `element`             | Molar concentrations of 11 elements (e.g., `Al`).          |
| `Temperature (C)`     | Oxidation test temperature in °C.                          |
| `time (h)`            | Oxidation duration in hours.                               |
| `specific mass gain (mg/cm2)` | Specific mass gain during oxidation.                |
| `source`              | Reference source for the data.                             |

## Usage

The dataset can be used to:
- Train machine learning models for predicting oxidation resistance in RHEAs and RCCAs.
- Explore correlations between alloy composition, oxidation conditions, and oxidation resistance.

## Citation

If you use this dataset in your research, please cite the original publication:

> S. Gorsse et al., "Advancing Refractory High Entropy Alloy Development with AI-Predictive Models for High Temperature Oxidation Resistance," Scripta Materialia, vol. 255, 2025. DOI: [10.1016/j.scriptamat.2024.116394](https://doi.org/10.1016/j.scriptamat.2024.116394).

## License

This dataset is distributed under the [CC BY 4.0 License](http://creativecommons.org/licenses/by/4.0/).
