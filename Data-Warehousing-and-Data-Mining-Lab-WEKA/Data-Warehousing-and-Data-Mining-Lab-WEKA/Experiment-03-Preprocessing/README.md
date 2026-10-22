# Experiment 3: Data Cleaning, Missing Values, and Normalization in WEKA

## Aim
To import a CSV dataset, inspect missing values, apply cleaning filters, and normalize numeric attributes using WEKA.

## Files
- `sample_missing_values.csv`

## Procedure
1. Open WEKA → **Explorer** → **Preprocess**.
2. Click **Open file** and select `sample_missing_values.csv`.
3. Review attribute types, missing values, and the instance count.
4. Under **Filter**, choose `unsupervised → attribute → ReplaceMissingValues`, click **Apply**.
5. To normalize numeric attributes, choose `unsupervised → attribute → Normalize`, then **Apply**.
6. To save the processed data, click **Save** and use ARFF or CSV if supported by your WEKA version.

## Discussion
`ReplaceMissingValues` replaces missing numeric values with means and nominal values with modes. `Normalize` scales numeric values to a defined range. Apply filters only after deciding whether the transformation is appropriate for your dataset.

## Result
The workflow shows how to load and preprocess a CSV in WEKA. Record the before/after attribute statistics from your actual run.
