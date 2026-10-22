# Experiment 9: K-Means Clustering in WEKA

## Aim
To cluster a dataset using K-Means and inspect cluster separation.

## Dataset
Use `iris_unlabeled.arff` (the class attribute is intentionally omitted).

## Procedure
1. Open the file in WEKA Explorer → Preprocess.
2. Open **Cluster → Choose → SimpleKMeans**.
3. Set `numClusters` (for example, 3 for this demonstration).
4. Choose **Classes to clusters evaluation** only if a known class label is available. This starter file omits the label, so use cluster assignments and centroids.
5. Click **Start**.
6. Inspect cluster sizes, centroids, and assignments. Use WEKA's visualization options to compare attributes.
7. Record the random seed and distance settings for reproducibility.

## Result
SimpleKMeans assigns instances to clusters. Discuss separation based on the actual cluster output; do not assume that cluster IDs correspond to known classes.
