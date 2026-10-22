# Experiment 7: Decision Tree Classification (J48 / ID3)

## Aim
To build and visualize a decision tree using WEKA.

## Dataset
Use `weather.nominal.arff` in this folder.

## Procedure
1. Load the dataset in WEKA Explorer → Preprocess.
2. Set `play` as the class attribute.
3. Open **Classify → Choose → trees → J48**. J48 is WEKA's implementation of the C4.5-style decision tree algorithm.
4. Choose 10-fold cross-validation (or the setting required by your instructor) and click **Start**.
5. In the result list, right-click the completed result and select **Visualize tree** if available.
6. Record the tree, accuracy, confusion matrix, and evaluation options.
7. If your lab specifically requires ID3, check whether `trees → Id3` is present and use it where suitable; ID3 has attribute-type limitations.

## Result
A decision tree is trained and visualized in WEKA. Include the tree image and actual evaluation results.
