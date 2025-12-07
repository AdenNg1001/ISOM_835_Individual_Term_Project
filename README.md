# 🎓 College Admission Predictive Analysis

### *Predictive Analytics & Machine Learning Term Project (ISOM 835)*

| | | | |
| :---: | :---: | :---: | :---: |
| **Instructor** | Hasan Arslan | **Type** | Individual Project |
| **Student** | Pham Thien An, Nguyen | **Student ID** | UID010043123 |
| **Due Date** | December 12th, 11:59 PM | | |

---

## 🚀 Quick Navigation

| Section | Link | Section | Link |
| :---: | :---: | :---: | :---: |
| **Project Overview** | [Overview](#project-overview) | **Preprocessing** | [Preprocessing](#data-cleaning--preprocessing) |
| **Dataset** | [Dataset](#dataset) | **Modeling** | [Modeling](#modeling) |
| **EDA** | [EDA](#exploratory-data-analysis-eda) | **Results & Insights** | [Results](#results--insights) |
| **Ethics** | [Ethics](#ethics--responsible-ai) | **Final Report** | [Report](#final-report-1012-pages) |

---

## 📘 Project Overview <a id="project-overview"></a>

This project applies the full **predictive analytics pipeline** to a real-world college admissions dataset. It simulates a professional analytics workflow, producing a **Google Colab notebook**, a **GitHub repository**, and a **10–12 page final report**.

### Key Deliverables:
* Dataset selection and rationale
* **EDA** with a minimum of **6 visualizations**
* Full preprocessing pipeline
* Comparison of **Regression** and **Classification** models
* Performance comparison and evaluation
* Business insights & recommendations
* Ethics and Responsible AI reflection

---

## 📂 Dataset <a id="dataset"></a>

### **Dataset Used**
📌 **College Admission Predictive Analysis Dataset**
🔗 **Dataset link:** [SharePoint Link - Access may require login](https://sumail-my.sharepoint.com/:x:/g/personal/jpn11395_su_suffolk_edu/Ed-oKhwyPLxDt8VDowXCgfIB_TX792GrBTQ1AGCg0gjqzg?e=XMmMpT)

| Requirement | Detail |
| :--- | :--- |
| **Type** | Real-world, multi-variable data |
| **Observations** | [Insert Number] |
| **Features** | [Insert Number] |
| **Target** | `admission_probability` (Numeric) |

### **Dataset Rationale**
I selected this dataset because college admissions represent a highly relevant real-world prediction problem. Universities rely on data-driven decision-making to evaluate applicants, and students also seek transparency about the factors affecting their admission chances.

This dataset offers:
* Rich multi-variable data (scores, demographics, academic history).
* Both **numeric** and **categorical** features suitable for modeling.
* A clearly defined prediction target (`admission_probability`).
* Enough observations for reliable machine learning analysis.

### **Problem Statement**
> **Can we accurately predict a student's probability of being admitted to college and identify the key variables driving that prediction?**

### **Target Variable**
🎯 **`admission_probability`**

This variable is crucial because:
* It enables a *probabilistic* assessment of admission chances.
* Supports both regression (predicting the probability) and classification (predicting admission success based on a threshold) frameworks.
* Helps identify the most influential admission factors for interpretation.

---

## 🔍 Exploratory Data Analysis (EDA) <a id="exploratory-data-analysis-eda"></a>

📄 **Google Colab Notebook:**
👉 [https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing](https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing)

### EDA Highlights:
* Dataset structure review and summary statistics.
* Missing value analysis and handling.
* Visualizations (minimum 6 plots): Histograms, Boxplots for outlier detection, Correlation heatmap, Scatterplot relationships, and Pairplot matrix.
* All visualizations are interpreted to guide subsequent modeling decisions.

---

## 🧹 Data Cleaning & Preprocessing <a id="data-cleaning--preprocessing"></a>

Notebook:
👉 [https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing](https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing)

### Preprocessing Steps:
* Handling missing values (documentation of strategy).
* Outlier review and treatment.
* **One-hot encoding** for categorical variables.
* **Scaling** numeric features using `StandardScaler`.
* Creation of a robust **train-test split**.
* Implementation of the Scikit-learn **`ColumnTransformer`** pipeline for streamlined application of transformations.

---

## 🤖 Modeling <a id="modeling"></a>

The project implemented and compared multiple model types as required, focusing on both prediction (Regression) and decision-making (Classification).

### **Regression Models (Predicting Probability)**
* Linear Regression
* Ridge Regression (Regularization)
* Random Forest Regressor
* Gradient Boosting Regressor

### **Classification Models (Predicting Admission Decision)**
* Logistic Regression
* Random Forest Classifier

### **Evaluation Metrics**
| Problem Type | Key Metrics |
| :--- | :--- |
| **Regression** | RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), $R^2$ (Coefficient of Determination) |
| **Classification** | Confusion Matrix, Precision, Recall, F1-Score, ROC-AUC Score |

All models and evaluations are fully documented in the linked Colab notebook.

---

## 📊 Results & Insights <a id="results--insights"></a>

### Key Deliverables:
* Comprehensive **Model Comparison Table** with performance metrics.
* Predicted vs. Actual plots for regression models.
* ROC-AUC comparison plot for classification models.
* **Feature Importance** visualizations and analysis.

### Business-Driven Insights:
* **Entrance exam score** is the strongest, most consistent predictor of admission probability.
* Socioeconomic factors and extracurricular activities have a **moderate, measurable impact** on the final prediction.
* **Tree-based models** (Random Forest, Gradient Boosting) consistently outperformed linear models, suggesting **non-linear patterns** in the admissions data.

### Recommended Modeling Strategy:
1.  **Regression Model** (e.g., Gradient Boosting) for **probability scoring** (providing the most granular risk assessment).
2.  **Classifier Model** (e.g., Random Forest) for **admission decision thresholding** (determining a simple 'Admit/Reject' based on the best F1/Recall score).

---

## ⚖️ Ethics & Responsible AI <a id="ethics--responsible-ai"></a>

A dedicated 1–2 page reflection on responsible AI is included in the final report.

### Reflection Topics:
* **Fairness** and potential biases across demographic groups in admissions.
* **Privacy** and confidentiality concerns related to using student records.
* **Transparency and Explainability** requirements for stakeholders (students, administrators).
* Ethical deployment and monitoring of predictive tools in the education sector.

---

## 📝 Final Report (10–12 Pages) <a id="final-report-1012-pages"></a>

📥 **Final Report (PDF)**
*(Upload your PDF here once completed and paste the link below)*

👉 *[Insert PDF Link Here]*

### Report Sections Include:
1.  Executive Summary
2.  Introduction & Business Context
3.  Exploratory Data Analysis (min 6 plots)
4.  Methodology (Preprocessing & Modeling)
5.  Results & Model Comparison
6.  Business Insights & Recommendations
7.  Ethics & Responsible AI Reflection
8.  Conclusion & Future Work

---

## 👨‍💻 Author

| Attribute | Detail |
| :--- | :--- |
| **Name** | Pham Thien An, Nguyen |
| **Student ID** | UID010043123 |
| **Course** | ISOM 835 – Predictive Analytics & Machine Learning |
| **Instructor** | Hasan Arslan |
| **Institution** | Suffolk University |

---
