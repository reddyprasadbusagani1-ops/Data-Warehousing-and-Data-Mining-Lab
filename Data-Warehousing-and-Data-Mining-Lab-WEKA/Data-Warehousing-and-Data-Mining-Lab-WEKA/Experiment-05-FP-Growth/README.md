# Experiment 5: FP-Growth Frequent Pattern Mining

## Aim
To mine frequent patterns from retail transactions using the FP-Growth algorithm.

## WEKA compatibility note
FP-Growth is not present in every standard WEKA installation. Do not assume that the algorithm is available by default.

## Procedure
1. Open WEKA and select **Tools → Package Manager**.
2. Search for a package providing FP-Growth or consult your lab instructor for the approved WEKA package/version.
3. Install the approved package and restart WEKA if required.
4. Load `../Experiment-04-Apriori/retail_transactions.arff` or your instructor-provided transaction dataset.
5. Select the installed FP-Growth implementation in the appropriate tab, configure minimum support, run it, and record the actual frequent patterns.
6. If no approved FP-Growth implementation is available, document that fact and ask your instructor whether an approved alternate tool is acceptable. Do not label Apriori output as FP-Growth output.

## Theory
FP-Growth compresses transactions into an FP-tree and mines frequent patterns without generating candidate itemsets in the same way as Apriori.

## Result
Complete the experiment with the instructor-approved FP-Growth implementation and attach verified output.
