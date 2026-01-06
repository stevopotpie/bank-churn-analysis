# Bank Customer Churn Analysis (Leakage-Aware)

## Objective
Analyze drivers of customer churn and build an interpretable baseline model. During modeling, I identified and corrected data leakage to ensure realistic, decision-ready results.

## Dataset
Customer churn dataset (synthetic / educational).

## Workflow
- Data cleaning and preparation
- Exploratory data analysis (EDA) and hypothesis testing
- Feature engineering (behavioral + experience signals)
- Leakage detection (single-feature test) and removal of leaky variables
- Logistic regression baseline + threshold tuning
- Coefficient interpretation and business-friendly takeaways

## Key Findings
- Engagement/activity signals were more informative than raw financial balance.
- After removing leaky post-outcome variables, model performance became realistic.
- Lowering the classification threshold improved churn recall for retention use cases.

## Files
- `01_eda.ipynb` — end-to-end analysis and modeling notebook

## Notes on data leakage
Some behavioral fields in the dataset perfectly predicted churn, indicating they were recorded post-outcome or generated using churn logic. These variables were excluded from predictive modeling to avoid inflated performance.

## Next steps (optional)
- Add a tree-based model for comparison (with careful leakage checks)
- Add ROC-AUC and confusion matrix visuals
- Package key results into a short slide or one-page summary
