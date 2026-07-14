# Database for Predicting Oxidation Resistance of Refractory High-Entropy Alloys

## Overview

This repository contains the experimental database used in the study *"Advancing Refractory High-Entropy Alloy Development with AI-Predictive Models for High-Temperature Oxidation Resistance"*. The database was designed to train and validate machine learning models for predicting specific mass gain due to oxidation in Refractory High-Entropy Alloys (RHEAs) and Refractory Complex Concentrated Alloys (RCCAs). It is a valuable resource for researchers in materials science, particularly those focusing on high-temperature alloy applications.

## Contents

* `data/`

  * `alloy_oxidation_886_202406.csv`: Contains the experimental data in CSV format.
  * `alloy_oxidation_886_202406.json`: Contains the experimental data in JSON format.
  * `data_analysis.ipynb`: A Jupyter notebook illustrating basic dataset statistics, distributions, and example data-loading workflows for exploratory analysis.
* `README.md`: Documentation of the dataset.

## Dataset Description

The database comprises **886 observations** from published literature, detailing the following parameters:

1. **Alloy Identification**:

   * A unique numerical alloy identifier assigned within the dataset.
   * A source-specific alloy identifier assigned to distinguish the same nominal alloy composition reported in different literature sources.
   * Original alloy formula or alloy name reported in the source publication.

2. **Alloy Composition**:

   * Elements: Al, Cr, Hf, Mo, Nb, Si, Ta, Ti, V, W, Zr.
   * Corresponding molar concentrations.

3. **Oxidation Conditions**:

   * Temperature (°C).
   * Time (hours).

4. **Target Property**:

   * Specific mass change due to oxidation in air (mg/cm²).

### File Details

#### `alloy_oxidation_886_202406.csv` and `alloy_oxidation_886_202406.json`

| Column Name                     | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Alloy_ID`                      | Unique identifier assigned to each nominal alloy composition within the dataset. The same `Alloy_ID` is used for the same nominal composition, even when the alloy is reported from different literature sources or tested under different oxidation conditions.                                                                                                                                                  |
| `Source_Alloy_ID`               | Source-specific alloy identifier assigned to each nominal alloy composition within a given literature source. The same `Source_Alloy_ID` is used for the same alloy composition reported in the same source, even when tested under different oxidation temperatures or exposure times. A different `Source_Alloy_ID` is assigned when the same nominal composition is reported in a different literature source. |
| `alloy formula`                 | Chemical formula or alloy name reported in the original publication.                                                                                                                                                                                                                                                                                                                                              |
| `element`                       | Molar concentrations of 11 elements, including Al, Cr, Hf, Mo, Nb, Si, Ta, Ti, V, W, and Zr.                                                                                                                                                                                                                                                                                                                      |
| `Temperature (C)`               | Isothermal oxidation test temperature in °C.                                                                                                                                                                                                                                                                                                                                                                      |
| `time (h)`                      | Oxidation duration in hours.                                                                                                                                                                                                                                                                                                                                                                                      |
| `specific mass change (mg/cm2)` | Net specific mass change measured after oxidation exposure.                                                                                                                                                                                                                                                                                                                                                       |
| `source`                        | Reference source for the data.                                                                                                                                                                                                                                                                                                                                                                                    |


## Notes on Data Interpretation

The reported specific mass change values should be interpreted as **net mass changes** after oxidation exposure. For refractory alloys containing volatile oxide-forming elements, such as Mo, V, and to a lesser extent Ta and W, the measured mass change may reflect the combined effects of oxidation-induced mass gain and volatilization-induced mass loss. Therefore, low or even negative mass change values do not necessarily indicate superior oxidation resistance in all cases.

Oxide scale thickness was not included as a standardized variable in this dataset because such information is not consistently reported across the collected literature. In addition, when scale thickness values are available, they may be affected by differences in measurement method, measurement location, oxide morphology, cracking, porosity, or spallation. These inconsistencies make systematic harmonization across different studies difficult.

## Usage

The dataset can be used to:

* Train machine learning models for predicting oxidation behavior in RHEAs and RCCAs.
* Explore correlations between alloy composition, oxidation conditions, and oxidation resistance.
* Support data-driven screening and design of refractory alloys for high-temperature applications.

## Citation

If you use this dataset in your research, please cite the original publication:

> S. Gorsse et al., "Advancing Refractory High Entropy Alloy Development with AI-Predictive Models for High Temperature Oxidation Resistance," *Scripta Materialia*, vol. 255, 2025. DOI: [10.1016/j.scriptamat.2024.116394](https://doi.org/10.1016/j.scriptamat.2024.116394).

## License

This dataset is distributed under the [CC BY 4.0 License](http://creativecommons.org/licenses/by/4.0/).
