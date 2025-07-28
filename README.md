# Placement_analysis
#  College Student Placement Analysis & Prediction

This project involves a complete exploratory data analysis (EDA) and predictive modeling pipeline for analyzing **college student placement** data and identifying the most influential factors determining a student's placement status.

---

##  Objective

The goal of this project is to:
- Explore the relationships between various academic and behavioral features.
- Visualize how different factors affect placement outcomes.
- Build machine learning models to **predict student placement**.
- Interpret and evaluate model performance using various metrics.

---

##  Dataset

The dataset includes information about college students such as:

- IQ
- CGPA
- Academic Performance
- Communication Skills
- Extra Curricular Scores
- Internship Experience
- Number of Projects
- Placement Status (Target Variable)

---

##  Libraries Used

- `pandas`, `numpy` – Data manipulation
- `seaborn`, `matplotlib`, `plotly` – Visualization
- `sklearn` – Machine learning and evaluation

---

##  Exploratory Data Analysis (EDA)

Key steps in EDA included:

- **Missing Values & Duplicates**: Verified that there were no null or duplicate entries.
- **Encoding**: Converted categorical columns like `Internship_Experience` and `Placement` into numerical format.
- **Distributions**: Used Plotly histograms and pie charts to visualize feature distributions with respect to placement.
- **Correlations**: Used heatmaps to assess the relationship between numeric features.

###  Key Insights:

- **CGPA** and **Communication Skills** are the strongest indicators of placement.
- **IQ** has moderate importance.
- **Internship Experience** and **Extra Curricular Score** have minimal influence.
- Students with fewer than 2 projects are less likely to be placed.

---

##  Machine Learning Models

### 1. Random Forest Classifier
- Achieved **~100% accuracy**.
- Feature Importance:
  - Most important: `CGPA`, `Communication Skills`, `IQ`.
  - Least important: `Extra Curricular Score`, `Internship`.

### 2. Logistic Regression
- Simple and interpretable.
- Coefficients show:
  - `CGPA`, `Communication Skills`, and `IQ` have strong positive contributions.
  - Minimal contribution from internship and extracurriculars.

### 3. Gradient Boosting Classifier
- Tuned with:
  - `n_estimators=150`, `max_depth=3`, `learning_rate=0.1`
- Excellent performance (nearly perfect accuracy).

---

##  Evaluation Metrics

For each model, we used:
- **Classification Report**: Precision, recall, F1-score.
- **Confusion Matrix**: To examine true/false positives and negatives.
- **5-Fold Cross-Validation**: To ensure generalization.


##  Conclusion

- **CGPA**, **Communication Skills**, and **IQ** are the most important factors for predicting placement.
- **Projects Completed** have a moderate effect—especially having *less than 2* reduces chances.
- **Internship Experience** and **Extra Curricular Score** showed weak correlation with placement.
- All models performed exceptionally well, with **Random Forest** giving near-perfect results.

---

