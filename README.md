# Power Transformer Fault Diagnosis and Remaining Useful Life Analysis

Exploratory analysis of dissolved gas measurements for power transformer
fault diagnosis and Remaining Useful Life (RUL) analysis.

## Overview

This project investigates time-series measurements of dissolved gases in
power transformers and their relationship with transformer operating
conditions and Remaining Useful Life (RUL).

The analysis is based on the **Power Transformers FDD and RUL** dataset.

The main objective of the project is to explore the statistical properties
and temporal dynamics of dissolved gas concentrations and investigate
patterns associated with transformer condition.

---

## Dataset

The dataset contains time-series measurements of dissolved gas
concentrations together with Remaining Useful Life (RUL) labels.

The following dissolved gases are analyzed:

- H₂ — Hydrogen
- CO — Carbon monoxide
- C₂H₄ — Ethylene
- C₂H₂ — Acetylene

The dataset contains approximately **1.26 million observations**
covering **3,000 transformers**.

The analysis uses both training and test data together with the provided
RUL labels.

---

## Analysis Pipeline

The notebook follows the following workflow:

1. Load training and test data
2. Merge sensor measurements with RUL labels
3. Prepare transformer identifiers
4. Construct a temporal scale with 12-hour intervals
5. Check missing and invalid values
6. Analyze dissolved gas distributions
7. Investigate temporal gas concentration patterns
8. Analyze the distribution of Remaining Useful Life
9. Group transformers according to their RUL characteristics
10. Compare gas concentration distributions between groups
11. Analyze temporal behavior for randomly selected transformers

---

## Exploratory Data Analysis

### Dissolved Gas Concentrations

The project analyzes the statistical distributions of four dissolved gases:

- H₂
- CO
- C₂H₄
- C₂H₂

Descriptive statistics, density plots, violin plots, and box plots are used
to investigate their distributions and variability.

### Temporal Analysis

Gas concentrations are analyzed as time series for randomly selected
transformers.

A rolling average is used to reduce short-term fluctuations and visualize
long-term concentration trends.

The temporal resolution of the constructed time scale is **12 hours**.

### Remaining Useful Life

The distribution of RUL values is analyzed to understand the variability
of transformer remaining lifetime.

The dataset contains RUL values ranging from several hundred time units
to values close to the upper bound of the dataset.

---

## Transformer Group Analysis

The analysis separates transformers into two groups based on the RUL
characteristics present in the dataset.

The resulting groups contain:

| Group | Number of Transformers |
|---|---:|
| Group 1 | 1,012 |
| Group 2 | 1,988 |
| Total | 3,000 |

Gas concentration distributions are then compared between the two groups.

This analysis is intended to identify differences in dissolved gas behavior
that may be associated with transformer condition.

---

## Data Quality

The analysis includes checks for missing and invalid values.

No missing values were detected in the analyzed variables:

- H₂
- CO
- C₂H₄
- C₂H₂
- transformer ID
- RUL
- temporal variables

---

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Scikit-learn
- Jupyter Notebook
