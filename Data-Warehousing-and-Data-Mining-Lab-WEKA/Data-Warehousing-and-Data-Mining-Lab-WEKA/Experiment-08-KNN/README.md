# Experiment 8: K-Nearest Neighbors (KNN) Using WEKA

## Aim
To classify instances using KNN and analyze the evaluation results.

## Dataset
Use `iris.arff` in this folder.

## Procedure
1. Load `iris.arff` in WEKA Explorer → Preprocess.
2. Set `class` as the class attribute.
3. Open **Classify → Choose → lazy → IBk**.
4. Open options and set `KNN` neighbour count (for example, K=3) if required.
5. Optionally add a `Normalize` filter through the FilteredClassifier for a fairer distance comparison when feature scales differ.
6. Select cross-validation and click **Start**.
7. Record accuracy, confusion matrix, and class-wise precision/recall.

## Result
IBk performs instance-based KNN classification. Use the values reported by your actual run.
