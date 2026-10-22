# Experiment 4: Apriori Association Rule Mining in WEKA

## Aim
To find frequent itemsets and generate association rules using Apriori.

## Files
- `retail_transactions.arff`

## Procedure
1. Open WEKA Explorer → Preprocess and load `retail_transactions.arff`.
2. Select the **Associate** tab.
3. Click **Choose** and select `Apriori`.
4. Open the algorithm options. Set a minimum support and confidence suitable for this small dataset; start with support around 0.2 and confidence around 0.6.
5. Click **Start** and inspect the generated rules.
6. Record the actual rules, support/confidence settings, and result.

## Interpretation
A rule such as `{bread} ==> {milk}` means transactions containing bread also contain milk with the reported confidence. It does not by itself prove causation.

## Result
Apriori is used to discover frequent itemsets and association rules. The exact rules depend on the dataset and options used.
