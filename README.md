# Credit_Risk_Analysis

Using supervised machine learning to assess credit risk

## Overview of Analysis

### Examining Credit Risk

This project was undertaken in order to evaluate the granting of loans, with the goal of predicting credit risk. Credit risk is inherently unbalanced, with good loans outnumbering risky ones. Therefore, within the domain of supervised machine learning, various models were built to evaluate the data using resampling.

### Resources

- Data Source: LoanStats_2019Q1.csv
- Technology: Jupyter Notebook, Python, scikit-learn library, imbalanced-learn library

## Results

### Data

A CSV file of loan information was obtained for analysis. See below for a snapshot of the dataframe. As expected, the number of low-risk loans vastly outnumbered the risky loans by a tally of 68470 to 347.

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/Creditdf.PNG?raw=true)

### Random Oversampling

- Accuracy score: 0.64
- Precision: low-risk: 1.00; high-risk: 0.01
- Recall: low-risk: 0.68; high-risk: 0.60
- F1 score: 0.81

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/RandomOversampling.PNG?raw=true)

### SMOTE

- Accuracy score: 0.64
- Precision: low-risk: 1.00; high-risk: 0.01
- Recall: low-risk: 0.68; high-risk: 0.60
- F1 score: 0.80

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/SMOTE.PNG?raw=true)

### Cluster Centroids Undersampling

- Accuracy score: 0.53
- Precision: low-risk: 1.00; high-risk: 0.01
- Recall: low-risk: 0.45; high-risk: 0.61
- F1 score: 0.62

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/CCUndersampling.PNG?raw=true)

### SMOTEENN

- Accuracy score: 0.53
- Precision: low-risk: 1.00; high-risk: 0.01
- Recall: low-risk: 0.58; high-risk: 0.70
- F1 score: 0.73

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.PNG?raw=true)

### Random Forest Classifier

- Accuracy score: 0.79
- Precision: low-risk: 1.00; high-risk: 0.04
- Recall: low-risk: 0.91; high-risk: 0.67
- F1 score: 0.95

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/Forest.PNG?raw=true)

### Easy Ensemble Classifier

- Accuracy score: 0.93
- Precision: low-risk: 1.00; high-risk: 0.07
- Recall: low-risk: 0.94; high-risk: 0.91
- F1 score: 0.97

![Credit_Data](https://github.com/josephrodini/Credit_Risk_Analysis/blob/main/Images/EasyEnsemble.PNG?raw=true)

## Summary

### Summary of Results

The models had varying degrees of predictive power for credit risk. Overall, the models erred on the side of low precision when evaluating high-risk cases, meaning they generated a number of false positive identifications of risky borrowers. This is not ideal, so the model with the highest precision was identified for recommendation.

### Recommendation

It is recommended that LendingClub use the Easy Ensemble Classifier due to it having the highest precision for identifying high-risk cases. Furthermore, the model generated a 93% accuracy rate in determining low- from high-risk borrowers, which was also tops out of all the models.
