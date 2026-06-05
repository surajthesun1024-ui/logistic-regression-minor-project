# 🔬 Ad Click Prediction — Logistic Regression Classification

## 📌 Overview
A supervised machine learning project that predicts whether a user will 
click on an advertisement based on their browsing behavior and demographics. 
Built using Python with a complete EDA, outlier treatment, and model 
evaluation pipeline.

**Result: 95.98% accuracy on test set**

---

## 📊 Dataset
- **Source:** Kaggle — Advertising Dataset
- **Records:** 1,000 rows (after outlier removal: ~990)
- **Total Features:** 10 columns
- **Features Used:** 4 (Daily Time Spent on Site, Age, Area Income, 
  Daily Internet Usage)
- **Target Variable:** `Clicked on Ad` (Binary — 0: Not Clicked, 1: Clicked)
- **Class Balance:** Perfectly balanced (50% / 50%)
- **Null Values:** 0
- **Duplicates:** 0

---

## 🛠️ Tools & Libraries
| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data loading and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Static visualizations |
| Seaborn | Statistical plots |
| Plotly | Interactive boxplots for outlier analysis |
| Scikit-learn | Model building and evaluation |

---

## 🔄 Project Workflow
1. **Data Loading & Exploration** — Shape, dtypes, null check, describe, 
   duplicate check
2. **Feature Selection** — Selected 4 most relevant numeric predictors 
   from 10 features
3. **Outlier Analysis** — Interactive Plotly boxplots across all 4 features; 
   identified outliers in Area Income
4. **Outlier Treatment** — Removed outliers using IQR method 
   (Lower Fence = Q1 − 1.5×IQR, Upper Fence = Q3 + 1.5×IQR)
5. **Train-Test Split** — 80/20 split (792 train / 199 test), random_state=5
6. **Model Training** — Logistic Regression (max_iter=1000) via Scikit-learn
7. **Model Evaluation** — Confusion matrix, accuracy score, ROC-AUC curve

---

## 📈 Results
| Metric | Score |
|--------|-------|
| **Accuracy** | **95.98%** |
| True Positives | 89 |
| True Negatives | 102 |
| False Positives | 3 |
| False Negatives | 5 |
| Total Misclassifications | 8 out of 199 |

---

## 🔑 Key Findings
- Users who spent **more time on site** and had **higher internet usage** 
  were less likely to click ads
- **Older users** with **lower area income** showed higher ad click rates
- The model achieved near-perfect separation between the two classes 
  on this balanced dataset

---

## 🚀 How to Run
```bash
git clone https://github.com/surajthesun1024-ui/logistic-regression-minor-project
cd logistic-regression-minor-project
pip install -r requirements.txt
jupyter notebook logistic_regression_classification.ipynb
```

## 👤 Author
**Suraj Singh** — M.Sc. Data Science & Analytics, Sharda University  
[LinkedIn](https://linkedin.com/in/suraj-singh-ds) | 
[GitHub](https://github.com/surajthesun1024-ui)
