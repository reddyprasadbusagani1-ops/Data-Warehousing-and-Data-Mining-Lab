# Experiment 6: Naïve Bayes Classification in WEKA

## Aim
To train a Naïve Bayes classifier and evaluate accuracy, precision, and recall.

## Dataset
`weather.nominal.arff` is a small educational dataset.

## Procedure
1. WEKA Explorer → Preprocess → Open file → load `weather.nominal.arff`.
2. Set the class attribute to `play`.
3. Open **Classify** → **Choose** → `bayes → NaiveBayes`.
4. Under **Test options**, select **Cross-validation** and use 10 folds if the dataset size and instructor requirements permit.
5. Click **Start**.
6. Record correctly/incorrectly classified instances, accuracy, and per-class precision/recall from the output.

## Result
The experiment trains and evaluates a Naïve Bayes model. Report only the metrics shown by your run.
