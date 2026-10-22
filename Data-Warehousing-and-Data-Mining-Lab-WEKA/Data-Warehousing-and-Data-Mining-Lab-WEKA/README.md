# Data Warehousing and Data Mining Lab — WEKA
**Course:** 23A30501P — Data Warehousing and Data Mining Lab  
**Programme:** B.Tech Artificial Intelligence & Data Science, JNTUA R23  
**Author:** Busagani Reddy Prasad  
**License:** MIT

This repository contains lab instructions and starter files for the 12 experiments in the syllabus. WEKA is used for GUI-based preprocessing, classification, clustering, association mining, and PCA. SQL is used for data warehouse schemas and OLAP operations.

## Tools
- WEKA (Explorer)
- SQL database such as MySQL, PostgreSQL, or SQLite with a compatible client
- CSV/ARFF datasets
- Optional WEKA Package Manager for algorithms not included in your installation

## Folder structure
- `Experiment-01-Star-Snowflake-Schema/` — SQL schema examples
- `Experiment-02-OLAP-Operations/` — SQL examples for roll-up, drill-down, slice, dice, pivot
- `Experiment-03-Preprocessing/` — CSV dataset and WEKA steps
- `Experiment-04-Apriori/` — transaction dataset and WEKA steps
- `Experiment-05-FP-Growth/` — availability notes and workflow
- `Experiment-06-Naive-Bayes/` — ARFF dataset and WEKA steps
- `Experiment-07-Decision-Tree/` — ARFF dataset and WEKA steps
- `Experiment-08-KNN/` — ARFF dataset and WEKA steps
- `Experiment-09-KMeans/` — ARFF dataset and WEKA steps
- `Experiment-10-Hierarchical-Clustering/` — ARFF dataset and WEKA steps
- `Experiment-11-PCA/` — numeric dataset and WEKA steps
- `Experiment-12-Mini-Project/` — mini-project guide

## Opening a dataset in WEKA
1. Start WEKA and select **Explorer**.
2. Open the **Preprocess** tab.
3. Select **Open file** and choose a `.arff` or `.csv` file.
4. Select the required class attribute (for classification).
5. Use the relevant tab: **Classify**, **Cluster**, **Associate**, or **Preprocess**.
6. Save screenshots of the settings and results for your lab record.

## Important compatibility notes
- WEKA versions and installed packages can differ. Check the available algorithms in your installation.
- Standard WEKA commonly includes Apriori, NaiveBayes, J48, IBk, SimpleKMeans, HierarchicalClusterer, and PrincipalComponents.
- FP-Growth is not guaranteed to be available in every standard installation. Check **Tools → Package Manager** and your instructor's recommended package. If unavailable, document the limitation and use the approved implementation.
- SQL syntax varies between database systems. The provided examples use broadly familiar SQL; adjust date functions or pivot syntax for your chosen DBMS.
- Sample datasets are educational examples, not real-world medical or financial data. For the mini-project, record the dataset source and do not claim results until you run the experiment.

## Suggested GitHub upload
Create a repository named `Data-Warehousing-and-Data-Mining-Lab`. Extract this ZIP, then upload the extracted folders and files. Do not upload only the ZIP if you want each experiment to be browsable on GitHub.
