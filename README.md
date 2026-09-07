# Predicting Kickstarter Campaign Success Using Machine Learning

Machine learning classification project analyzing 331,000+ Kickstarter campaigns to predict funding success and identify the strongest drivers of campaign outcomes.

## Overview

Only a minority of Kickstarter campaigns reach their funding goal. This project applies classification models to predict whether a campaign will be successfully funded and translates the results into actionable recommendations for creators.

**Research Questions**
1. What campaign and creator characteristics most strongly predict funding success?
2. Is there an optimal funding goal for a campaign?
3. What advice can be offered to a creator launching a new campaign?

## Data

The dataset is a publicly available collection of Kickstarter campaigns sourced from Kaggle, containing 331,370 campaigns after filtering.

**Source:** Michalczyk, M. (2018). *Kickstarter Projects*. Kaggle. https://www.kaggle.com/datasets/kemical/kickstarter-projects

## Methods

- **Feature engineering:** campaign duration, launch month/year, and a log-transformed funding goal (`log_goal`) to correct for extreme outliers
- **Models trained:** Logistic Regression, Linear Discriminant Analysis (LDA), Decision Tree, and Random Forest
- **Evaluation:** accuracy, precision, recall, ROC-AUC, and confusion matrices, using a 70/30 train-test split (231,959 / 99,411 campaigns)

## Key Findings

- **Funding goal is the strongest predictor of success.** Campaigns under $1,000 succeed at ~55%, compared to ~8% for campaigns over $100,000.
- **No single "optimal" goal exists**, but campaigns under $10,000 consistently outperform larger ones.
- **Category matters significantly.** Creative/performance categories (Theater, Dance, Comics, Music) have notably higher success rates than Technology, Journalism, Crafts, and Food.
- All four models performed similarly (AUC 0.67–0.69), suggesting the dataset's available features are the main constraint on predictive power rather than model choice.

## Recommendations for Creators

Set a realistic, minimum-viable funding goal rather than an aspirational one, favor shorter-to-medium campaign lengths, and recognize that category and community fit play a meaningful role in likelihood of success.

## Repository Contents

| File | Description |
|---|---|
| `KickStarter_FinalNotebook.ipynb` | Full analysis notebook: data cleaning, feature engineering, EDA, model training, and evaluation |
| `Final Project ABA.docx` | Full written report covering research questions, methodology, results, and business recommendations |

## Limitations

This analysis is based on historical campaign metadata only — it does not capture qualitative factors like creator reputation, social media presence, or pre-launch audience building, all of which likely influence real-world outcomes.

## Author Contributions

- **Cooper Ritz** — Data analysis, feature engineering, model development, and final notebook (code, analysis, interpretations, visualizations)
- **Tommy Devens** — Report writing and research framing
- **Grace Gavlinski** — Report review, writing, and editing

Completed for BIT 3484, Spring 2026.
