# 🎓 College Admission Predictive Analysis

### *Predictive Analytics & Machine Learning — Term Project (ISOM 835)*

| | | | |
| :---: | :---: | :---: | :---: |
| **Professor** | Hasan Arslan | **Project Type** | Individual |
| **Student** | Pham Thien An, Nguyen | **Student ID** | UID010043123 |
| **Due Date** | December 12, 11:59 PM | | |

---

## 🚀 Quick Navigation

| Section | Link | Section | Link |
| :---: | :---: | :---: | :---: |
| **Overview** | [Project Overview](#project-overview) | **Preprocessing** | [Preprocessing](#data-cleaning--preprocessing) |
| **Dataset** | [Dataset](#dataset) | **Modeling** | [Modeling](#modeling) |
| **EDA** | [EDA](#exploratory-data-analysis-eda) | **Results** | [Results & Insights](#results--insights) |
| **Ethics** | [Ethics](#ethics--responsible-ai) | **Final Report** | [Final Report](#final-report-1012-pages) |

---

## 📘 Project Overview <a id="project-overview"></a>

This project implements a full end-to-end **predictive analytics and machine learning pipeline** using a real-world **college admission dataset (25,000 records, 13 features)**. The goal is to assist universities in:

- Predicting **admission probability** (regression)
- Classifying students as **admitted vs. not admitted** (classification)
- Understanding the **key drivers** behind admission outcomes
- Ensuring fairness, transparency, and responsible AI principles in deployment

Deliverables include a **Google Colab notebook**, **GitHub repository**, and a **10–12 page final report** summarizing methodology, results, and strategic business insights.

---

## 📂 Dataset <a id="dataset"></a>

### Dataset Details  
📌 **College Admissions Dataset (25,000 rows × 13 features)**  
🔗 *Dataset link:* [SharePoint (login required)](https://sumail-my.sharepoint.com/:x:/g/personal/jpn11395_su_suffolk_edu/Ed-oKhwyPLxDt8VDowXCgfIB_TX792GrBTQ1AGCg0gjqzg?e=XMmMpT)

### Feature Types
**Numeric Features**
- age  
- entrance_score  
- board_percentage  
- extracurricular_score  
- admission_probability  

**Categorical Features**
- gender  
- category  
- state  
- preferred_stream  
- entrance_exam  
- admission_status  
- scholarship_eligibility  

### Target Variables  
- **Regression:** `admission_probability`  
- **Classification:** `admitted` (binary label created using threshold 0.5)  

### Problem Statement  
> **Can we accurately predict admission outcomes and identify the factors that most strongly influence them?**

---

## 🔍 Exploratory Data Analysis (EDA) <a id="exploratory-data-analysis-eda"></a>

📄 **Google Colab Notebook:**  
👉 https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing

### EDA Highlights

- Dataset summary statistics (25,000 observations)
- No missing values detected
- Several visualizations:
  - Histograms (numeric features)
  - Boxplots (outlier detection)
  - Correlation heatmap
  - Scatterplot (Entrance Score vs. Admission Probability)
  - Gender comparison bar plot
  - Pairplot scatter matrix
- Key numerical insights:
  - **Board Percentage (0.73)** → strongest correlation with admission
  - **Entrance Score (0.55)** → second strongest predictor
  - **Extracurricular Score (0.40)** → moderate influence
  - Demographics show minimal predictive correlation

---

## 🧹 Data Cleaning & Preprocessing <a id="data-cleaning--preprocessing"></a>

### Preprocessing Steps (as implemented)

1. **Removed `student_id`** (non-predictive)  
2. **Separated numeric and categorical variables**  
3. **Scaled numeric features** using `StandardScaler`  
4. **Encoded categorical features** using `OneHotEncoder(handle_unknown="ignore")`  
5. **Built a unified preprocessing pipeline** using `ColumnTransformer`  
6. **Integrated preprocessing + model into one Pipeline** to prevent leakage  

### Why Use a Pipeline?

- Ensures consistent transformation  
- Prevents test data leakage  
- Enables modular model swapping  
- Fully compatible with cross-validation and grid search  

---

## 🤖 Modeling <a id="modeling"></a>

### Regression Models
- Linear Regression  
- Ridge Regression  
- Random Forest Regressor  
- Gradient Boosting Regressor  

### Classification Models
- Logistic Regression  
- Random Forest Classifier  

### Evaluation Metrics  
| Task | Metrics |
| :--- | :--- |
| **Regression** | RMSE, MAE, R² |
| **Classification** | Accuracy, F1, Precision, Recall, Confusion Matrix, ROC-AUC |

---

## 📊 Results & Insights <a id="results--insights"></a>

### ⭐ Best Regression Model  
### **Random Forest Regressor**  
- **R² = 0.9317**  
- **RMSE = 0.0825**  
- **MAE = 0.01705**  
- Excellent fit with near-perfect predicted vs actual alignment  
- Captures non-linear relationships effectively  

### ⭐ Best Classification Model  
### **Logistic Regression**  
- **ROC-AUC = 0.9999**  
- **Accuracy = 98%**  
- **F1 = 0.94 (macro)**  
- Most interpretable model → ideal for admissions decision support  

### Key Insights
- Academic metrics (board percentage, entrance score) drive admission outcomes  
- Extracurriculars act as secondary—but meaningful—predictors  
- Demographic variables show minimal influence, supporting fairness  
- Tree-based models outperform linear ones due to non-linear relationships  

### Business Recommendations
- Use **Random Forest** for probability scoring  
- Use **Logistic Regression** for explainable decision-making  
- Provide applicant feedback using model insights  
- Implement fairness audits and yearly model retraining  
- Enhance academic readiness programs for borderline applicants  

---

## ⚖️ Ethics & Responsible AI <a id="ethics--responsible-ai"></a>

A full ethics analysis is included in the final report.

### Topics Addressed
- Potential biases hidden within academic metrics  
- Fairness risks from socioeconomic disparities  
- Privacy & FERPA compliance  
- Transparent decision support, not automated decision-making  
- Recommendations for explainability tools (SHAP/LIME)  

---

## 📝 Final Report (10–12 Pages) <a id="final-report-1012-pages"></a>

📥 *Upload your final PDF and insert the link:*  
👉 **[Insert PDF Link Here]**

### Report Sections
1. Executive Summary  
2. Introduction & Business Context  
3. Exploratory Data Analysis  
4. Methodology: Preprocessing & Modeling  
5. Model Results & Interpretation  
6. Business Insights & Recommendations  
7. Ethics & Responsible AI  
8. Conclusion & Future Work  
9. References & AI Assistance (ChatGPT + Google Gemini)  

---

## 👨‍💻 Author

| Attribute | Detail |
| :--- | :--- |
| **Name** | Pham Thien An, Nguyen |
| **Student ID** | UID010043123 |
| **Course** | ISOM 835 – Predictive Analytics & Machine Learning |
| **Professor** | Hasan Arslan |
| **Institution** | Suffolk University |

---
