# Ridge Logistic Regression Analysis

## Overview
This project explores the effects of Ridge (L2) regularization in a multiclass logistic regression model. The analysis investigates how regularization impacts coefficients, cross-validation performance, and predictions. This project applies these techniques to classify ancestry groups based on human genetic data.

## Context
The dataset consists of **𝑁 = 183 training observations (individuals)** sampled from populations across the world. Each individual's genetic data has been projected along the **𝑝 = 10 top principal components**, which together explain **24.16% of the variance**. These principal components are used as features instead of raw genetic data to significantly reduce computational complexity while retaining meaningful information for classification.

The goal is to fit a model that predicts (classifies) an individual's ancestry from these 10 principal components.

## Purpose
The notebook demonstrates:
1. The impact of varying the regularization parameter (λ) on model coefficients.
2. The relationship between λ and cross-validation performance (log-loss).
3. Predictions for test samples using the optimal λ, including probabilities for each ancestry class.

## Key Features
- Visualizes the effect of λ on the coefficients of logistic regression for better interpretability.
- Identifies the optimal λ using cross-validation to minimize log-loss.
- Produces class probabilities for test samples and highlights ancestry patterns.

---

## Packages Used
The analysis relies on the following Python libraries:
- **`numpy`**: Numerical operations and array manipulations.
- **`pandas`**: Data handling and preprocessing.
- **`matplotlib`**: Visualization of results and trends.
- **`scikit-learn`**: Logistic regression modeling, cross-validation, and metrics.
- **`seaborn`**: Heatmaps for predicted probabilities.

---

## Results Summary

### Key Findings
- **Mixed Ancestry Patterns**: Mexican and African American samples exhibit mixed ancestry, reflecting historical events like colonization and the transatlantic slave trade.
- **Clear Assignments for Unknown Samples**: Unknown samples were clearly matched to a single ancestry group.
- **Historical Insights**: The results align with historical records, including indigenous populations' mixing with colonizers and the slave trade's genetic impacts.
- **Speculative Observations**: Possible ancient seafaring connections (e.g., Polynesians reaching the Americas or Indian Ocean trade influencing genetics) are hinted at by shared traits.

---

### Example Table of Results

Below is a sample of predicted probabilities and classifications:

| African    | European   | EastAsian  | Oceanian   | NativeAmerican | Predicted Class | Actual Class |
|------------|------------|------------|------------|----------------|-----------------|--------------|
| 0.131156   | 0.093878   | 0.099505   | 0.081108   | 0.594353       | NativeAmerican  | Unknown      |
| 0.102278   | 0.064486   | 0.109084   | 0.651919   | 0.072233       | Oceanian        | Unknown      |
| 0.099014   | 0.167203   | 0.520602   | 0.097951   | 0.115230       | EastAsian       | Unknown      |
| 0.181682   | 0.216551   | 0.126798   | 0.216200   | 0.258769       | NativeAmerican  | Unknown      |
| 0.132245   | 0.620827   | 0.065980   | 0.098260   | 0.082688       | European        | Unknown      |
| 0.135332   | 0.062889   | 0.191956   | 0.537468   | 0.072355       | Oceanian        | Mexican      |
| 0.153923   | 0.084007   | 0.253703   | 0.387418   | 0.120948       | Oceanian        | Mexican      |
| 0.143852   | 0.103410   | 0.157563   | 0.509435   | 0.085740       | Oceanian        | Mexican      |
| 0.166508   | 0.117424   | 0.261901   | 0.347607   | 0.106560       | Oceanian        | Mexican      |
| 0.186156   | 0.121892   | 0.256650   | 0.337394   | 0.097908       | Oceanian        | Mexican      |
| 0.186488   | 0.096595   | 0.335412   | 0.272778   | 0.108727       | EastAsian       | Mexican      |

---

## Repository Structure
- **`data/`**: Training and test datasets.
- **`images/`**: Visualizations of results.
- **`notebooks/`**: Jupyter Notebook containing the analysis.
- **`requirements.txt`**: List of required Python packages.

---

## Usage Instructions
1. Clone this repository:
   ```bash
   git clone https://github.com/DevDizzle/ridge-logistic-regression.git
