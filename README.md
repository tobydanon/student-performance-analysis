# Student Academic Performance Analysis

## Overview
Analysis of the UCI Student Performance dataset (395 Portuguese secondary school students) exploring demographic, behavioural, and academic predictors of final mathematics grades.

**Tools:** Python, pandas, matplotlib, scikit-learn  
**Models:** Linear Regression, Random Forest Regressor  
**Dataset:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/320/student+performance)

---

## Key Findings

- **Prior grades dominate:** G2 (second term grade) alone accounts for 93% of the Random Forest model's predictive power, achieving R² = 0.925
- **Behavioural factors are weak direct predictors:** Removing G1 and G2 drops R² to -2.67, indicating demographic and behavioural variables cannot reliably predict final grades on their own
- **Indirect effects likely:** EDA revealed that higher parental education and lower absences correlate with better grades, suggesting these factors influence performance indirectly through prior grades
- **Support mechanisms are reactive:** Students with no external support scored highest on average, consistent with support being a response to poor performance rather than a cause of good performance

---

## Structure

- `analysis.ipynb` — Full analysis notebook with EDA, feature engineering, and modelling
- `student-mat.csv` — Mathematics course dataset (used in analysis)
- `student-por.csv` — Portuguese language dataset (not analysed, available for future work)
- `student.txt` — Variable descriptions

---

## Limitations & Future Work

- Dataset is small (395 observations) which limits model reliability for behavioural features
- Several key variables are self-reported ordinal scales which compress nuance
- Future work: extend analysis to Portuguese dataset and compare predictive factors across subjects; conduct formal mediation analysis to test whether behavioural factors operate through prior grades
