# Experiment 11: Principal Component Analysis (PCA) in WEKA

## Aim
To reduce the dimensionality of a numeric dataset using PCA.

## Dataset
Use `numeric_data.arff`.

## Procedure
1. Load `numeric_data.arff` in WEKA Explorer → Preprocess.
2. Open **Filter → Choose → unsupervised → attribute → PrincipalComponents**.
3. Open filter options and review variance coverage settings if available.
4. Click **Apply**. Inspect the transformed attributes (principal components).
5. Compare the number of original numeric attributes with the transformed attributes and note the explained variance information shown by your WEKA version.
6. Save the transformed dataset if required.

## Result
PCA transforms correlated numeric features into principal components. Report the dimensions and variance information shown by the actual run.
