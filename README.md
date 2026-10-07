# Credit Card Default Prediction Using Orange

An educational machine learning project by **Vaibhav Mishra**, using Orange Data Mining to explore credit card client data and compare default classification models.

## Objective

Predict the binary target `default payment next month`:

- **0:** No default.
- **1:** Default.

## Dataset

The supplied CSV contains **30,000 records and 25 columns**. There are 23,364 non-default records and 6,636 default records (22.12% defaults).

Features include credit limit, demographic variables, repayment status, bill amounts and payment amounts. The workflow's Select Columns widget assigns the default column as the target and excludes ID from predictive features.

The supplied Excel file contains the same columns and values as the CSV, so only the CSV is needed for this repository.

## Repository files

| File | Purpose |
| --- | --- |
| `Credit_Card_Default.ows` | Orange workflow |
| `F215020_default of credit card clients.csv` | Input dataset |
| `README.md` | Project overview and instructions |

## Workflow contents

The saved workflow contains widgets for:

- Selecting columns, imputation, outlier handling, continuization and preprocessing.
- Constructing features and ranking variables.
- Exploring distributions, box plots, scatter plots, heat maps and correlations.
- Comparing Logistic Regression, Random Forest, Decision Tree, kNN and a stacking learner.
- Evaluating models with Test and Score, ROC Analysis, Confusion Matrix, Calibration Plot and Performance Curve.
- Additional exploration using PCA, t-SNE and k-Means.
- Inspecting predictions and a Logistic Regression nomogram.

The presence of these widgets does not establish model performance; rerun the workflow to inspect results.

## How to run

1. Install Orange Data Mining.
2. Download this repository and extract all files into one folder.
3. Open Orange and use **File → Open** to open `Credit_Card_Default.ows`.
4. Open the workflow's **File widget** and browse to `F215020_default of credit card clients.csv`.
5. Confirm that `default payment next month` is categorical with values 0 and 1.
6. In **Select Columns**, confirm that this column is the target and ID is excluded from features.
7. Apply any pending changes and allow the connected widgets to run.
8. Review Test and Score and the evaluation plots.

**Dataset path:** The original workflow stores a local Windows path to `Updated_default of credit card clients.csv`. Users must select the supplied CSV in the File widget if that path cannot be resolved. Save the workflow after selecting the dataset.

## Interpretation and limitations

- Default is the minority class, so accuracy should be considered alongside recall, precision, F1 and AUC.
- Verify the Test and Score settings before reporting evaluation results.
- Data transformations and feature selection should be fitted within training folds for rigorous validation; preprocessing the entire dataset before evaluation can bias performance estimates.
- Predictions and feature associations do not establish causal relationships.
- This workflow is an educational project, not a deployed lending decision system.

## Data attribution

Before public redistribution, add the original dataset source, citation and licence. The supplied files alone do not establish redistribution permission.

## Author

**Vaibhav Mishra**  
MSc Digital Finance & AI, Loughborough University London
