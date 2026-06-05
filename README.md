# Supplementary Code for Network-Extended TPB Digital Collaboration Study

This repository contains the supplementary Python/Jupyter Notebook code for the manuscript:

**A Network-Extended Theory of Planned Behavior for Digital Collaboration in Construction Project Management**

The notebook reproduces the main quantitative outputs reported in the manuscript, including respondent profile summaries, measurement reliability and validity checks, hierarchical regression models, mediation SEM results, bootstrap mediation effects, and manuscript figures.

## Repository contents

|File|Description|
|-|-|
|`network\_extended\_tpb\_v01.ipynb`|Main Jupyter Notebook for reproducing the manuscript analysis.|
|`requirements.txt`|Python package requirements for running the notebook locally.|
|`.gitignore`|Excludes generated outputs, caches, and local environment files.|
|`CITATION.cff`|Citation metadata for the supplementary code repository.|
|`REPOSITORY\_SETUP.md`|Step-by-step instructions for uploading the repository and opening it in Google Colab.|
|`COMMIT\_MESSAGE.txt`|Suggested initial Git commit message.|

## Data Usage and Citation

The data presented in this notebook are the property of their respective owners and are used with prior permission. Any use of this dataset in future work requires prior approval from the corresponding author (Dr. Long D. Nguyen at lnguyen@fgcu.edu). Users must ensure appropriate attribution and citation in all resulting publications or materials.How to run in Google Colab

In Colab, choose **Runtime > Run all** to reproduce the tables and figures.

## How to run locally

1. Clone the repository.
2. Install Python 3.10 or later.
3. Install the package requirements:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook network\_extended\_tpb\_supplementary\_code\_google\_drive\_translated\_values.ipynb
```

5. Run all cells.

## Outputs produced by the notebook

The notebook creates an output folder named:

```text
outputs\_network\_extended\_tpb/
```

The folder contains:

|Output|Description|
|-|-|
|`network\_extended\_tpb\_manuscript\_tables.xlsx`|Excel workbook containing Tables 1-8 and diagnostic sheets.|
|`Figure2\_regression\_model\_comparison.png`|Figure comparing R-squared values across hierarchical regression models.|
|`Figure3\_final\_empirical\_mediation\_model.png`|Final empirical mediation model figure.|

The Excel workbook includes the following sheets:

* Table 1 respondent profile
* Full respondent profile
* Role coding audit
* Training coding audit
* Table 2 descriptive statistics
* Table 3 reliability and convergent validity
* Table 4 correlations and discriminant validity
* Table 5 hierarchical regression
* Regression model summary
* Regression details
* VIF diagnostics
* SEM df diagnostic
* Table 6 SEM fit
* Table 7 SEM structural paths
* Table 8 bootstrap mediation effects
* SEM estimates
* Bootstrap raw results

## Important SEM specification note

The mediation SEM model used in the manuscript frees the covariance between the two exogenous predictors:

```text
SNS \~\~ years\_pm\_experience
```

This covariance is important because it matches the manuscript model that yields **df = 17** in Table 6. If this covariance is omitted, the model imposes an additional restriction that Social Network Support and years of PM experience are uncorrelated, which increases the SEM degrees of freedom to **df = 18** and can change the mediation SEM estimates.

## Main analyses reproduced

The notebook reproduces the following manuscript outputs:

1. Respondent profile table
2. Measurement item descriptive statistics
3. Cronbach's alpha, Composite Reliability, and Average Variance Extracted
4. Correlation matrix and discriminant validity assessment
5. Hierarchical regression models:

   * Model 1: traditional TPB predictors only
   * Model 2: TPB predictors plus Social Network Support
   * Model 3: TPB predictors, Social Network Support, and years of PM experience
6. Mediation SEM:

   * Social Network Support to Perceived Behavioral Control
   * Perceived Behavioral Control to Digital Collaboration Behavior
   * Social Network Support to Digital Collaboration Behavior
   * PM experience control paths
7. Bootstrap mediation effects
8. Manuscript figures

## Reproducibility notes

* The notebook uses a fixed random seed for bootstrap reproducibility.
* The dataset is downloaded directly from Google Drive/Sheets at runtime.
* Generated output files are excluded from Git tracking by default through `.gitignore`.
* If the Google Drive dataset is edited after publication or review submission, regenerated results may differ from the submitted manuscript outputs. For archival reproducibility, consider preserving a dated, read-only copy of the dataset used for the manuscript submission.

## Suggested repository citation

Nguyen, T. D., and Nguyen, L. D. (2026). *Supplementary code for A Network-Extended Theory of Planned Behavior for Digital Collaboration in Construction Project Management*. GitHub repository.

## Contact

For questions about the supplementary analysis, contact the corresponding author listed in the manuscript.

