# 🎓 College Admission Predictive Analysis  
### *Predictive Analytics & Machine Learning Term Project (ISOM 835)*

---

<p align="center">
  <img src="https://img.shields.io/badge/Instructor-Hasan%20Arslan-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Type-Individual_Project-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Student-Pham%20Thien%20An%2C%20Nguyen-purple?style=for-the-badge">
  <img src="https://img.shields.io/badge/Student_ID-UID010043123-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Due-Dec_12%2C_11%3A59_PM-red?style=for-the-badge">
</p>

---

## 🚀 Quick Navigation

<p align="center">
  <a href="#project-overview">
    <img src="https://img.shields.io/badge/Project_Overview-0052CC?style=for-the-badge" />
  </a>
  <a href="#dataset">
    <img src="https://img.shields.io/badge/Dataset-00875A?style=for-the-badge" />
  </a>
  <a href="#eda">
    <img src="https://img.shields.io/badge/EDA-7B61FF?style=for-the-badge" />
  </a>
  <a href="#preprocessing">
    <img src="https://img.shields.io/badge/Preprocessing-F9A825?style=for-the-badge" />
  </a>
  <a href="#modeling">
    <img src="https://img.shields.io/badge/Modeling-9C27B0?style=for-the-badge" />
  </a>
  <a href="#results">
    <img src="https://img.shields.io/badge/Results_&_Insights-E91E63?style=for-the-badge" />
  </a>
  <a href="#ethics">
    <img src="https://img.shields.io/badge/Ethics_&_Responsible_AI-4A6572?style=for-the-badge" />
  </a>
  <a href="#report">
    <img src="https://img.shields.io/badge/Final_Report-000000?style=for-the-badge&logo=adobeacrobatreader" />
  </a>
</p>

---

# 📘 Project Overview <a name="project-overview"></a>

This project applies the full predictive analytics pipeline to a real-world college admissions dataset.  
It simulates a real professional analytics workflow, producing a **Colab notebook**, **GitHub repository**, and a **10–12 page final report**.

Deliverables include:
- Dataset selection + rationale  
- EDA with at least 6 visualizations  
- Preprocessing pipeline  
- Regression + classification modeling  
- Performance comparison  
- Business insights & recommendations  
- Ethics and responsible AI reflection  

---

# 📂 Dataset <a name="dataset"></a>

### **Dataset Used**  
📌 **College Admission Predictive Analysis Dataset**  
🔗 **Dataset link:**  
https://sumail-my.sharepoint.com/:x:/g/personal/jpn11395_su_suffolk_edu/Ed-oKhwyPLxDt8VDowXCgfIB_TX792GrBTQ1AGCg0gjqzg?e=XMmMpT  

---

### **Dataset Rationale**  
I selected this dataset because college admissions represent a highly relevant real-world prediction problem. Universities rely on data-driven decision-making to evaluate applicants, and students also seek transparency about the factors affecting their admission chances.  

This dataset offers:
- Rich multi-variable data (scores, demographics, academic history)  
- Both **numeric & categorical** features suitable for modeling  
- A clearly defined prediction target  
- Enough observations for reliable machine learning  

---

### **Problem Statement**  
> **Can we accurately predict a student's probability of being admitted to college and identify the key variables driving that prediction?**

### **Target Variable**  
🎯 **`admission_probability`**

This variable matters because:
- It enables *probabilistic* assessment of admission chances  
- Supports both regression & classification frameworks  
- Helps identify the most influential admission factors  

---

# 🔍 Exploratory Data Analysis (EDA) <a name="eda"></a>

📄 **Google Colab Notebook:**  
https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing  

EDA includes:
- Dataset structure review  
- Summary statistics  
- Missing value analysis  
- Histograms of numeric features  
- Boxplots for outlier detection  
- Correlation heatmap  
- Scatterplot relationships  
- Pairplot matrix  

At least **6+ visualizations**, each interpreted.

---

# 🧹 Data Cleaning & Preprocessing <a name="preprocessing"></a>

Preprocessing steps:
- Handling missing values  
- Outlier review  
- One-hot encoding for categorical variables  
- Scaling numeric features using StandardScaler  
- Train-test split  
- Scikit-learn `ColumnTransformer` pipeline  

Notebook:  
👉 https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing  

---

# 🤖 Modeling <a name="modeling"></a>

### **Regression Models**
- Linear Regression  
- Ridge Regression  
- Random Forest Regressor  
- Gradient Boosting Regressor  

### **Classification Models**
- Logistic Regression  
- Random Forest Classifier  

### **Evaluation Metrics**
Regression:
- RMSE, MAE, R²  

Classification:
- Confusion Matrix  
- Precision, Recall, F1  
- ROC-AUC Score  

All implemented in the Colab notebook.

---

# 📊 Results & Insights <a name="results"></a>

Key Deliverables:
- Comprehensive model comparison table  
- Predicted vs Actual plots  
- ROC-AUC comparison  
- Feature importance visualizations  

Business-Driven Insights:
- Entrance exam score is the strongest predictor  
- Socioeconomic factors have moderate impact  
- Tree models capture non-linear patterns better  
- Recommended modeling strategy:  
  - Regression model → for probability scoring  
  - Classifier → for admission decision thresholding  

---

# ⚖️ Ethics & Responsible AI <a name="ethics"></a>

Reflection topics included:
- Fairness across demographic groups  
- Biases in admissions datasets  
- Privacy and confidentiality concerns  
- Ethical use of predictive tools in education  
- Transparency and explainability requirements  

A full 1–2 page ethics analysis is included in the final report.

---

# 📝 Final Report (10–12 Pages) <a name="report"></a>

📥 **Final Report (PDF)**  
*(Upload your PDF here once completed and paste the link below)*  

👉 *Coming soon*  

Includes:
- Executive summary  
- Dataset rationale  
- EDA  
- Preprocessing  
- Model development  
- Evaluation  
- Business insights  
- Ethical discussion  
- Conclusion  

---

# 👨‍💻 Author  

**Name:** Pham Thien An, Nguyen  
**Student ID:** UID010043123  
**Course:** ISOM 835 – Predictive Analytics & Machine Learning  
**Instructor:** Hasan Arslan  
**Institution:** Suffolk University  

---
