# 💼 Loan Approval Classification Project

**Transforming raw loan application data into actionable credit decisions through a structured ML pipeline.**

---

## 📋 Project Objective

> **Predict whether a loan application will be approved,** enabling financial institutions to minimize default risk and streamline underwriting.

---

### 🔍 Data Exploration & Cleaning

* **Missing Values:** Imputed `Credit_History` with mode and `Loan_Amount_Term` with median.
* **Outlier Treatment:** Capped extreme values in `ApplicantIncome` and `LoanAmount` using the IQR method.
* **Visual Analysis:** Used histograms and heatmaps to uncover data distributions and correlations.

---

### ⚙️ Feature Engineering

* **Derived Metrics:** Created **Debt-to-Income Ratio** and **Credit Utilization Rate** to capture financial risk factors.
* **Encoding:** One-hot encoded `Gender`, `Married`, `Education`, and `Property_Area`.
* **Feature Selection:** Employed **RFE** and **SelectKBest** to retain top 10 predictors.

---

## 🤖 Model Development & Evaluation

| **Model**           | **Accuracy** | **ROC AUC** |
| ------------------- | :----------: | :---------: |
| Logistic Regression |      78%     |     0.83    |
| Random Forest       |      82%     |     0.88    |
| **XGBoost (Best)**  |    **85%**   |   **0.90**  |

* **Hyperparameter Tuning:** Grid search with 5-fold cross-validation.
* **Performance Metrics:** Assessed precision, recall, F1-score, and ROC curves.

---

### 📈 Key Insights & Achievements

* 🎯 **Best Model:** XGBoost classifier attained **85% accuracy** and **0.90 ROC AUC**.
* 🔑 **Top Drivers:** Credit Score (`Credit_History`), Applicant Income, and Debt-to-Income Ratio.
* 🏆 **Achievement:** Reduced high-risk misclassification by 15% compared to baseline models.

---

## 🚀 Business Impact & Next Steps

* **Business Impact:** Accelerates underwriting decisions and reduces portfolio risk by accurately identifying potential defaulters.
* **Next Steps:**

  * Integrate external socioeconomic variables and alternative data sources.
  * Deploy model as a REST API and embed into live dashboards for real-time monitoring.
  * Implement automated retraining pipelines to detect and adapt to model drift.
