# TikTok Claims Classification Model

## Overview

*Note: This project was developed as part of the <a href="https://coursera.org/share/3f665f8503b65baef6dd0667dd28a52a">Google Advanced Data Analytics Certificate</a> Specialization.*

TikTok is a social media platform for creating, sharing and discovering short videos. The app is used as an outlet for people to express themselves and allows users to create videos and share them across a community. TikTok users have the ability to submit reports that identify videos and comments that contain user claims.

**Problem:** These reports identify content that needs to be reviewed by a limited number of moderators. The process generates a large number of user reports that are challenging to consider in a timely manner.

**Proposed Solution:** To create a predictive machine learning model that classifies videos as either claims or opinions.

These are the steps taken to create the model:
1. <a href="https://github.com/AliaAbdulAziz/TikTokClassification/tree/main/EDA">Exploratory Data Analysis (EDA)</a>
2. <a href="https://github.com/AliaAbdulAziz/TikTokClassification/tree/main/Hypothesis%20Testing">Hypothesis Testing</a>
3. <a href="https://github.com/AliaAbdulAziz/TikTokClassification/tree/main/Regression%20Model">Regression Modelling</a>
4. <a href="https://github.com/AliaAbdulAziz/TikTokClassification/tree/main/ML%20model">Machine Learning Classification</a>

## Files and workflow
- [EDA](EDA/EDA.ipynb): exploratory analysis.
- [Hypothesis testing](Hypothesis%20Testing/HT.ipynb): statistical testing.
- [Regression](Regression%20Model/Regression%20Model.ipynb): regression modelling.
- [Machine learning](ML%20model/ML.ipynb): random forest and XGBoost classification.
- [Dataset](tiktok_dataset.csv): input records.

The ML notebook uses a 60/20/20 train/validation/test split, text features with CountVectorizer, and GridSearchCV with recall as its model-selection metric. Random forest is selected over XGBoost in the notebook's comparison.

## Reproduce
Use Jupyter with pandas, NumPy, Matplotlib, seaborn, scikit-learn, XGBoost, and statsmodels for the relevant notebooks. Set the working directory or CSV paths so each notebook can locate tiktok_dataset.csv in the repository root. Run cells in order; hyperparameter searches can take several minutes. Library versions are not pinned.

## Results and limitations
The notebook describes 10 validation misclassifications for random forest and 26 for XGBoost; displayed classification-report values are rounded, so 1.00 should not be interpreted as zero errors. These observations concern the certificate dataset, not a deployed moderation system. Assess feature availability at triage time, leakage, and generalisation before using such a model operationally. The classifier distinguishes claims from opinions; it does not establish whether a claim is true or violates policy.

[Portfolio](https://aliaaziz.work)
