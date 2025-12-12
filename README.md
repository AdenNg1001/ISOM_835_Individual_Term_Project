# 🎓 College Admission Predictive Analysis 
### *Predictive Analytics & Machine Learning - Term Project (ISOM 835)*

| | | | |
| :---: | :---: | :---: | :---: |
| **Professor** | Hasan Arslan | **Project Type** | Individual |
| **Student** | Pham Thien An, Nguyen | **Student ID** | UID010043123 |
| **Due Date** | December 12, 11:59 PM | | |

---

## 🚀 Quick Navigation

| Section | Link | Section | Link |
| :---: | :---: | :---: | :---: |
| **Overview** | [Project Overview](#project-overview) | **Dataset** | [Dataset](#dataset) |
| **EDA** | [EDA](#exploratory-data-analysis-eda) | **Preprocessing** | [Data Cleaning & Preprocessing](#data-cleaning--preprocessing) |
| **Modeling** | [Modeling](#modeling) | **Results** | [Results & Insights](#results--insights) |
| **Ethics** | [Ethics](#ethics--responsible-ai) | **Final Report** | [Final PDF Report](#final-report) |
| **Citations** | [Citations & References](#-citations--references) | | |

---

## 📘 Project Overview <a id="project-overview"></a>

This project implements a full end-to-end **predictive analytics and machine learning pipeline** using a real-world **college admission dataset (25,000 records, 13 features)**. The goal is to assist universities in:

- Predicting **admission probability** (regression)
- Classifying students as **admitted vs. not admitted** (classification)
- Understanding the **key drivers** behind admission outcomes
- Ensuring fairness, transparency, and responsible AI principles in deployment

Deliverables include a **Google Colab Notebook**, **GitHub Repository**, and a **Final PDF Report** summarizing methodology, results, and strategic business insights.

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

📄 **Google Colab Notebook Link:* [ISOM 835_Individual Term Project.ipynb](https://colab.research.google.com/drive/18l3jiyF7uviz2DRrhv8JpW-H63Fw8Qom?usp=sharing)

### Main Steps

- Summary statistics for all numeric and categorical features  
- Histograms for age, entrance_score, board_percentage, extracurricular_score, admission_probability  
- Boxplots to detect outliers, especially in entrance_score  
- Correlation heatmap between numeric variables  
- Scatterplot: **Entrance Score vs. Admission Probability**  
- Grouped bar chart: **Average Admission Probability by Gender**  
- Pairplot / scatter matrix to visualize multivariate patterns  

### Key EDA Insights

- **Board Percentage** is the **strongest predictor** of `admission_probability`  
  - Correlation ≈ **0.73**  
- **Entrance Score** is the **second strongest** predictor  
  - Correlation ≈ **0.55**  
- **Extracurricular Score** has a **moderate but meaningful** impact  
  - Correlation ≈ **0.40**  
- Demographic variables such as **age, gender, and state** show **minimal correlation** with admission probability  
- Several **outliers** exist in `entrance_score` (> 500), but they are handled well by tree-based models  
- **No missing values** were found, simplifying preprocessing  
- Relationships show both **linear and nonlinear** behavior → motivates using **linear + ensemble methods**

---

## 🧹 Data Cleaning & Preprocessing <a id="data-cleaning--preprocessing"></a>

### Missing Value Check

Before beginning preprocessing, the dataset was reloaded and inspected for missing values.  
No missing values were found in any column, confirming the dataset is complete and requires no imputation.

### Preprocessing Steps (as implemented)

1. **Removed `student_id`** (non-predictive)  
2. **Separated numeric and categorical variables**  
3. **Scaled numeric features** using `StandardScaler`  
4. **Encoded categorical features** using `OneHotEncoder(handle_unknown="ignore")`  
5. **Built a unified preprocessing pipeline** using `ColumnTransformer`  
6. **Integrated preprocessing + model into one Pipeline** to prevent leakage  

### Why Use a Pipeline?

- **Prevents data leakage** (fit on train only, transform train + test)  
- Ensures **consistent preprocessing** across all models  
- Makes it easy to **swap models** while reusing the same preprocessing  
- Compatible with **GridSearchCV**, cross-validation, and metric evaluation    

---

## 🤖 Modeling <a id="modeling"></a>

Two predictive tasks were implemented:

1. **Regression** – predict `admission_probability`  
2. **Classification** – predict `admitted` (0/1)

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
The **Random Forest Regressor** clearly outperformed the other regression models.

- **R² ≈ 0.99** (explains ~99% of the variance in admission probability)  
- Very low RMSE and MAE  
- Predicted vs. Actual plot shows points tightly clustered along the 45° line  

**Why it works well**

- Captures **nonlinear interactions** between academic metrics and extracurriculars  
- Robust to **outliers**, especially extreme entrance scores  
- Handles mixed feature types after preprocessing
  

### ⭐ Best Classification Model  
### **Logistic Regression**  
The **Logistic Regression** model achieved **near-perfect** classification performance:

- **ROC–AUC ≈ 0.9999**  
- **Accuracy ≈ 99%**  
- Very high precision and recall for both classes  

From the confusion matrix on the 5,000-row test set:

- Correctly classifies **4435 / 4439** non-admitted students  
- Correctly classifies **550 / 561** admitted students  
- Only a small number of false positives and false negatives  

**Why it’s preferred for deployment**

- High predictive performance  
- **Interpretable coefficients** → easier to explain to admissions officers  
- Works well with the scaled + one-hot encoded feature space
 

### Key Insights
From the modeling and EDA combined:

1. **Academic performance is the primary driver**
   - Board percentage and entrance exam scores are the most important predictors.
2. **Extracurricular activities still matter**
   - Provide a secondary positive contribution and support a **holistic** view.
3. **Demographic bias appears limited in this dataset**
   - Demographic variables have low predictive power relative to academic metrics.
4. **Hybrid modeling approach is ideal**
   - Use **Random Forest** for high-accuracy probability estimation.  
   - Use **Logistic Regression** for **transparent, policy-friendly** decision support.
  

### Business Recommendations
- Rank applicants by **predicted admission probability**.  
- Provide admissions officers with:  
  - Model probability  
  - Key feature drivers (e.g., board % and entrance score)  
- Consider slightly lowering the decision threshold (e.g., 0.50 → 0.45) when the goal is to **reduce false negatives** for borderline applicants.  

---

## ⚖️ Ethics & Responsible AI <a id="ethics--responsible-ai"></a>

Because admissions decisions are **high-stakes**, the project includes a dedicated ethics section.

### Potential Risks

- Academic metrics may encode **socioeconomic advantage** (tutoring access, school quality).  
- Over-reliance on standardized tests can disadvantage under-resourced students.  
- Regional (state-level) differences can reflect structural inequality.

### Recommended Safeguards

- Perform **annual fairness audits** across gender, category, and region.  
- Monitor error rates (false positives/negatives) by subgroup.  
- Use explainability tools (e.g., **SHAP**, **LIME**) to document how features influence predictions.  
- Keep **humans-in-the-loop** — the model should assist, not replace, admissions officers.  
- Ensure strong **data governance**: FERPA compliance, encryption, access control, and audit logs.

---

## 📝 Final PDF Report <a id="final-report"></a>

👉 *PDF File link:* [ISOM835_FinalAssignmentReport_Pham Thien An Nguyen_UID010043123](https://drive.google.com/file/d/16WXZHYXOr7J-NbMJlpoC3W8LTf724OUm/view?usp=sharing)

### Report Sections
1. Executive Summary  
2. Introduction & Business Context  
3. Exploratory Data Analysis (EDA)  
4. Methodology: Preprocessing & Modeling  
5. Regression Modeling  
6. Classification Modeling  
7. Business Insights & Recommendations  
8. Ethics & Responsible AI Reflection  
9. Conclusion & Future Work
10. References & AI Assistance (ChatGPT + Google Gemini)  

---
## 📚 Citations & References

This project used external datasets, open-source tools, research resources, and community knowledge. All key sources are cited below.

---

### Dataset Source & Documentation

- **College Admission Prediction Dataset** (2024).  
  Provided through Kaggle.  
- Dataset documentation and data dictionary accompanying the shared Excel file.

---

### Code References & Adapted Tutorials

Some preprocessing, visualization, and modeling patterns were adapted from standard examples in the following sources:

- **Scikit-learn Documentation**  
  Pipelines, `ColumnTransformer`, `OneHotEncoder`, `StandardScaler`, regression and classification models, and evaluation utilities.  
  https://scikit-learn.org/stable/documentation.html

- **Matplotlib Documentation & Gallery**  
  Used for figure setup, styling, and exporting plots.  
  https://matplotlib.org/stable/gallery/index.html

- **Seaborn Tutorials**  
  Used for statistical visualizations such as histograms, boxplots, pairplots, and correlation heatmaps.  
  https://seaborn.pydata.org/tutorial.html

- **Stack Overflow**  
  Selected snippets were referenced to debug issues related to:
  - Pipeline integration  
  - Confusion matrix plotting  
  - ROC curve implementation  
  (Exact posts available upon request.)

---

### Research Papers & Articles

The following academic and technical references informed the modeling choices, evaluation, and ethical discussion:

- Breiman, L. (2001). **Random Forests**. *Machine Learning*.  
- Hosmer, D. W., Lemeshow, S., & Sturdivant, R. X. (2013). *Applied Logistic Regression*.  
- Ribeiro, M. T., Singh, S., & Guestrin, C. (2016). “**Why Should I Trust You?**: Explaining the Predictions of Any Classifier.”  
- High-level Responsible AI and fairness guidelines from:
  - OECD AI Principles  
  - Google Responsible AI documentation  

These works shaped the interpretation of results, the choice of ensemble methods, and the focus on explainability and fairness.

---

### Python Libraries & Tools Used

The project was implemented using the following tools and open-source libraries:

- **Python 3.x**
- **Pandas** – data loading, cleaning, and transformation  
- **NumPy** – numerical operations and array handling  
- **Scikit-learn** – preprocessing, pipelines, regression and classification models, evaluation metrics  
- **Matplotlib** – core plotting and figure customization  
- **Seaborn** – higher-level statistical visualizations  
- **SHAP** (optional) – model explainability and feature contribution analysis  
- **Google Colab / Jupyter Notebook** – interactive development and experimentation  

All libraries are open-source and used under their respective licenses for academic purposes.

---

### AI Assistance Acknowledgment

Portions of the project documentation and report text (including wording refinement, structure, and explanation clarity) were assisted by **OpenAI ChatGPT** and **Google Gemini**.  
All code implementation, experimental design, model selection, and final interpretations were performed and validated by the student.

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
