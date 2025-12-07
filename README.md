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

This project delivers a complete **end-to-end predictive analytics workflow** applied to a real-world college admissions dataset. It follows professional machine learning standards and includes a full **Google Colab notebook**, **GitHub repository**, and a structured **10–12 page report**.

### 🔑 Key Deliverables
- Dataset acquisition & justification  
- **EDA** with 6+ visualizations  
- Full preprocessing pipeline  
- Regression & classification model development  
- Performance evaluation & comparison  
- Business insights & actionable recommendations  
- Ethics & Responsible AI considerations  

---

## 📂 Dataset <a id="dataset"></a>

### Dataset Used  
📌 **College Admission Predictive Analysis Dataset**  
🔗 *Dataset link:*  
[SharePoint (Login Required)](https://sumail-my.sharepoint.com/:x:/g/personal/jpn11395_su_suffolk_edu/Ed-oKhwyPLxDt8VDowXCgfIB_TX792GrBTQ1AGCg0gjqzg?e=XMmMpT)

| Requirement | Description |
| :--- | :--- |
| **Type** | Real-world, multivariable dataset |
| **Observations** | *[Insert]* |
| **Features** | *[Insert]* |
| **Target Variable** | `admission_probability` |

### Why This Dataset?
College admissions involve complex decision-making influenced by academic, demographic, and extracurricular factors. This dataset is ideal because it offers:
- A rich blend of **numeric and categorical variables**  
- A defined prediction target suitable for regression and classification  
- High relevance for educational institutions and applicants  
- Sufficient data size for robust modeling  

### 🎯 Problem Statement
> **Can we accurately predict a student’s likelihood of admission and identify the variables that most strongly influence admissions decisions?**

---

## 🔍 Exploratory Data Analysis (EDA) <a id="exploratory-data-analysis-eda"></a>

📄 **Google Colab Notebook:**  
👉 https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing

### EDA Highlights
- Dataset structure, datatypes, and descriptive statistics  
- Missing value exploration and treatment strategy  
- Outlier examination using boxplots  
- **6+ visualizations**, including:  
  - Histograms  
  - Pairplots  
  - Scatterplots  
  - Correlation heatmap  
- Insights guided preprocessing and modeling choices  

---

## 🧹 Data Cleaning & Preprocessing <a id="data-cleaning--preprocessing"></a>

Notebook:  
👉 https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing

### 🔧 Preprocessing Workflow
- Systematic handling of missing values  
- Outlier detection and mitigation  
- **One-hot encoding** for categorical variables  
- **StandardScaler** for numeric variables  
- Train-test split with justification  
- End-to-end **ColumnTransformer + Pipeline** ensuring:
  - No data leakage  
  - Reproducible transformations  
  - Compatibility with all regression/classification models  

---

## 🤖 Modeling <a id="modeling"></a>

Both predictive (regression) and decision-based (classification) models were developed.

### 📈 Regression Models (Predicting Probability)
- Linear Regression  
- Ridge Regression  
- Random Forest Regressor  
- Gradient Boosting Regressor  

### 🧮 Classification Models (Admit vs. Reject)
- Logistic Regression  
- Random Forest Classifier  

### 📏 Evaluation Metrics
| Task | Metrics |
| :--- | :--- |
| **Regression** | RMSE, MAE, R² |
| **Classification** | Confusion Matrix, Precision, Recall, F1, ROC-AUC |

---

## 📊 Results & Insights <a id="results--insights"></a>

### 📌 Key Results
- Comprehensive comparison table for all models  
- Predicted vs. Actual regression performance plots  
- ROC-AUC comparison for classification models  
- Feature importance visualization  

### 🔍 Analytical Insights
- **Entrance exam score** is the strongest predictor of admission probability  
- Socioeconomic and extracurricular features show **moderate predictive impact**  
- Non-linear models (Random Forest, Gradient Boosting) outperform linear models → indicating complex relationships within the data  

### 🧭 Recommended Modeling Strategy
1. **Gradient Boosting Regression** → Best for accurate probability scoring  
2. **Random Forest Classification** → Best for threshold-based admission decisions  

---

## ⚖️ Ethics & Responsible AI <a id="ethics--responsible-ai"></a>

A full ethics section (1–2 pages) is included in the final report.

### Topics Covered
- Bias & fairness concerns related to demographic features  
- Accountability and transparency of automated admissions tools  
- Privacy considerations (student data, institutional policy)  
- Responsible deployment & ongoing monitoring  

---

## 📝 Final Report (10–12 Pages) <a id="final-report-1012-pages"></a>

📥 *Upload your final PDF and include the link here:*  
👉 **[Insert Final Report PDF]**

### Report Structure
1. Executive Summary  
2. Introduction & Business Context  
3. Exploratory Data Analysis  
4. **Methodology: Preprocessing & Modeling**  
5. Model Comparison & Interpretation  
6. Business Insights & Recommendations  
7. Ethics & Responsible AI Analysis  
8. Conclusion & Future Work  
9. **References & Acknowledgments**  
   - Includes citation of tools: *Google Gemini*, *ChatGPT*, etc.

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

