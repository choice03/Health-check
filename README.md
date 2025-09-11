# Health-check
Project Overview

This project analyzes the Postpartum Depression (PPD) dataset (THP_clean.csv) to explore demographic, medical, and social factors linked to PPD and to build a machine learning model that predicts risk. Dataschema was alemployed as some column names were encrypted.

The dataset includes:

Demographics: age, marital status, education, employment, parity (number of children)

Medical history: previous depression, HAMD baseline score, birth complications

Social support: MSPSS baseline score

Target: Postpartum depression (yes/no)

Methodology

1. Data Loading Loaded the dataset (THP_clean.csv) into a Pandas DataFrame. Checked shape, column names, and data types.

2. Data Cleaning Removed duplicate rows. Standardized column names (lowercase, underscores). Filled missing values: Numeric columns → filled with median. Categorical columns → filled with mode (most frequent value).

3. Exploratory Data Analysis (EDA) & Visualizations

20 key research questions were asked and answered: Visualizations used: bar plots, boxplots, pie chart, histogram, and heatmap.

1. Does age group influence PPD?
2. Does marital status affect PPD?
3. Does social support reduce PPD risk?
4. what is depression rate based on parent educational level?
5. What percentage of mothers experienced PPD?
6. Does birth complications increase PPD risk?
7. Does the number of children (parity) affect PPD?
8. How does social relationship influence PPD?
9. Does employment status affect PPD?
10. What is the effect of hamd severity score of the mother on wppsi variables?
11. how does ppd affect the social behaviour of children using scas & sdq
12. What is the ratio of depressed and not depressed among mother's with no health issue?
13. Effect the influcence of external family members being on PPD?
14. Does the number of child being born influence PPD?
15. Does the living condaition influence PPD?
16. Finacial inflence on PPD?
17. How does BMI inflenece Mother's physical and mental health?
18. What is the effect of the Home on PPD?
19. Is PPD influenced by practicing birth spacing?
20. What is the mortality rate of children?


4. Predictive Modeling Preprocessed categorical variables using Label Encoding. Defined features (X) and target (y = depressed). Split dataset into training and testing sets (80/20). Trained a Random Forest Classifier. Evaluated with: Accuracy, Precision, Recall, F1-score (classification report). Confusion matrix.


5. Feature Importance Extracted feature importances from the Random Forest model. Identified the Top 10 predictors of PPD (e.g., social support score, HAMD score, marital status, birth complications). Results & Insights Mothers with lower social support had a higher risk of PPD. History of depression and higher HAMD scores were strong predictors. Marital status and birth complications were also linked to increased risk. Random Forest achieved good predictive performance, showing potential for risk screening.

How to Run
1. Open the Jupyter Notebook PPD_Analysis.ipynb.
2. Run all cells step by step.
3. Upload THP_clean.csv when prompted.
4. Visualizations and model results will display inline.

Libraries Used
1. pandas(data handling)
2. numpy(numerical processing)
3. matplotlib& seaborn (visualization)
4. scikit-learn(machine learning)
