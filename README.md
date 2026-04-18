# Digital Marketing Campaign Conversion Prediction

A binary classification project that predicts whether a customer will convert after interacting with a digital marketing campaign. Built as an end-to-end applied ML capstone covering problem framing, data analysis, model development, and impact reporting.

## Problem Statement

> Predict whether a **customer** will **convert** after interacting with a digital marketing campaign, using demographic, behavioral, and campaign data recorded during the campaign, so that marketing managers can optimise ad spend, reduce wasted impressions, and focus resources on high-intent users.

**Classification Type:** Binary (Convert = 1, No Conversion = 0)  
**SDG Alignment:** SDG 12 — Responsible Consumption and Production

## Dataset

| Attribute | Detail |
|-----------|--------|
| Source | [Kaggle — Predict Conversion in Digital Marketing Dataset](https://www.kaggle.com/datasets/rabieelkharoua/predict-conversion-in-digital-marketing-dataset) |
| Records | 8,000 customers |
| Features | 19 input features + 1 target variable |
| Missing Values | None |
| Class Balance | Imbalanced — 87.7% positive, 12.3% negative |

### Key Features

- **Demographics:** Age, Gender, Income
- **Campaign:** CampaignChannel, CampaignType, AdSpend, AdvertisingPlatform
- **Engagement:** ClickThroughRate, WebsiteVisits, PagesPerVisit, TimeOnSite
- **Email Metrics:** EmailOpens, EmailClicks
- **Social:** SocialShares
- **Customer History:** PreviousPurchases, LoyaltyPoints

## Project Structure

```
classification-capstone/
├── notebooks/
│   └── classification_capstone.ipynb
├── data/
│   └── digital_marketing_campaign_dataset.csv
├── impact_statement.md
└── README.md
```

## Notebook Sections

The capstone notebook follows the full ML pipeline:

1. **Problem Statement and Motivation** — Business context, five-part ML framing, stakeholder analysis
2. **Hypothesis** — Testable hypotheses on engagement, channel effectiveness, and feature importance
3. **Dataset Selection and Ethical/Licensing Considerations** — Source, licensing, sensitive attributes, leakage risks
4. **Data Understanding, Cleaning, and Preprocessing** — EDA, visualisations, class imbalance analysis, feature engineering, encoding and scaling
5. **Model Development and Comparison** — Logistic Regression, Random Forest, Gradient Boosting with full evaluation
6. **Evaluation, Optimization, and Diagnostics** — Hyperparameter tuning, threshold optimisation, cross-validation, fairness analysis
7. **Impact Reporting** — Technical summary, stakeholder-facing summary, key visuals, limitations and ethics reflection

## Models Trained

| Model | Role |
|-------|------|
| Logistic Regression | Baseline — interpretable, fast |
| Random Forest | Ensemble — balanced performance |
| Gradient Boosting | Stretch — highest predictive power |

## Evaluation Approach

- **Metrics:** Precision, Recall, F1-Score, ROC-AUC (accuracy alone is insufficient due to class imbalance)
- **Imbalance Handling:** Class weights, SMOTE oversampling
- **Validation:** Stratified K-Fold cross-validation
- **Fairness:** Performance comparison across gender subgroups
- **Threshold Tuning:** Precision-recall curve analysis for optimal decision threshold

## Impact Summary

**Target KPI:** Reduce cost per conversion by 15% while maintaining or improving total conversions.

**Direct Beneficiaries:** Marketing managers, CRM teams, media planners  
**Indirect Beneficiaries:** Customers (fewer irrelevant ads, better experience)

## Tech Stack

- Python 3.x
- pandas, NumPy
- scikit-learn
- imbalanced-learn (SMOTE)
- matplotlib, seaborn
- Jupyter Notebook (Kaggle)

## Ethical Considerations

- `Gender` identified as a sensitive attribute — fairness metrics reported by subgroup
- `ConversionRate` flagged as a potential leakage feature and investigated
- `AdvertisingPlatform` and `AdvertisingTool` anonymised by data provider
- EU AI Act risk tier: **Limited** (marketing optimisation)

## License

This project is for educational purposes as part of an Applied ML Classification Capstone. The dataset is publicly available on Kaggle under standard Kaggle terms of use.

## Author

[Your Name]
