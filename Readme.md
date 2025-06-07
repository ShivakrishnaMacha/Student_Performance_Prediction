# 🎯 Student Performance Prediction

A comprehensive machine learning project to analyze and predict student performance based on socio-demographic and academic preparation factors. Built with EDA, preprocessing, model training, evaluation, and web deployment.

---

## 📌 Problem Statement

Educational institutions strive to understand what factors influence student performance. This project explores how variables like gender, ethnicity, parental education, lunch type, and test preparation affect student scores in math, reading, and writing.

---

## 🎯 Objective

- Perform in-depth exploratory data analysis (EDA).
- Identify key patterns and insights related to student performance.
- Build and evaluate a predictive model to estimate student scores.
- Deploy the model in a web application for real-time inference.

---

## 📊 Dataset Overview

- **Source**: [Kaggle - Students Performance Dataset](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
- **Size**: 1000 rows × 8 columns
- **Features**:
  - `gender`
  - `race/ethnicity`
  - `parental level of education`
  - `lunch`
  - `test preparation course`
  - `math score`
  - `reading score`
  - `writing score`
- **Target Variables**: Scores in Math, Reading, Writing

---

## 🔎 Exploratory Data Analysis (EDA)

Key Insights:
- Female students outperformed male students in reading and writing.
- Students who had **standard lunch** consistently scored higher.
- Test preparation course had a significant positive impact on performance.
- Parental education had mixed impact, with **master's** and **associate’s degrees** contributing the most to better performance.
- Added derived columns: **Total Score** and **Average Score**.

Visualizations:
- Histograms, KDE plots
- Gender vs. Scores distribution
- Impact of lunch and test preparation on average scores
- Influence of parental education on performance

---

## 🧹 Data Cleaning & Feature Engineering

- ✅ No missing values
- ✅ No duplicates
- ✔️ Added new features: `total_score`, `average_score`
- ✔️ Encoded categorical variables for modeling
- ✔️ Normalized numerical data where necessary

---

## 🤖 Modeling

- **Model Used**: CatBoost Regressor
  - Chosen for its superior handling of categorical variables and robustness on tabular data
- **Training**:
  - Train-test split
  - Cross-validation
- **Evaluation Metrics**:
  - R² Score
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)

---

## 📈 Results

| Metric       | Value    |
|--------------|----------|
| R² Score     | ~0.90+   |
| MAE          | Low      |
| RMSE         | Low      |

- **Feature Importance**: Gender, test preparation, and parental education were among top predictors.
- **Artifacts**: Stored in `/artifacts` directory (includes `model.pkl`, `preprocessor.pkl`, `train.csv`, `test.csv`)

---

## ✅ Conclusion & Takeaways

- Strong correlations were observed between standard lunch, test prep, and high scores.
- Gender and parental education level play a role in student performance, but not uniformly.
- CatBoost provided high accuracy with minimal preprocessing.
- Insights could help education planners focus on support areas like meal plans and preparation courses.

---

## 🔮 Next Steps or Future Work

- Explore multi-target regression for all scores combined.
- Introduce more features like school type, hours studied, extracurriculars.
- Deploy with user login and score history tracking.
- Use SHAP for better interpretability of feature impacts.

---

## 🛠️ Tools & Technologies

- **Languages**: Python
- **Libraries**:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `catboost`, `scikit-learn`
- **Platform**: Jupyter Notebook, Flask
- **Deployment**: AWS Elastic Beanstalk (via `.ebextensions`)

---

## 👤 Author

**Shivakrishna Macha**  
Data Science & AI Enthusiast
[LinkedIn](https://www.linkedin.com/in/shivakrishnamacha/) 

---

