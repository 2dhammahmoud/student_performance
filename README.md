

# 🎓 Student Performance Prediction

## 📌 Project Overview

This project analyzes the **Student Performance dataset (UCI Repository)** to understand factors affecting academic success.
We applied **data cleaning, EDA, clustering (K-Means), and supervised learning (Logistic Regression, Decision Tree, Random Forest)** to predict whether a student will **pass or fail**.

The goal is to:

* Identify key risk factors for student failure.
* Compare model performance with and without data leakage (G1 & G2).
* Provide actionable recommendations for early interventions.

---

## 📊 Dataset

* **Source**: [UCI Machine Learning Repository – Student Performance](https://archive.ics.uci.edu/ml/datasets/Student+Performance)
* **Size**: \~650 rows, 33 features
* **Target**:

  * `passs` (binary: pass/fail)
  * `risk` (3-class: low/medium/high risk, optional)
* **Limitations**: Small dataset, imbalanced classes, sensitive attributes (e.g., family background).

---

## 🛠️ Setup

### Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

### Key Libraries Used

* **pandas, numpy** → Data manipulation
* **matplotlib, seaborn** → Visualization
* **scikit-learn** → ML models, preprocessing, evaluation
* **scipy** → Statistical tests

---

## ▶️ How to Run

All steps are in a **single notebook**:

1. Open the notebook:

   ```bash
   jupyter notebook student_performance.ipynb
   ```

   *(or run in VS Code / Colab)*

2. Run cells sequentially:

   * Data loading & cleaning
   * Exploratory Data Analysis (EDA)
   * K-Means clustering
   * Classification (Logistic Regression, Decision Tree, Random Forest)
   * Evaluation (hold-out, 5-fold CV, tuning)
   * Interpretation & recommendations

---

## 📈 Results Summary

* **With Leakage (G1, G2 included)** → Models achieved very high performance (Random Forest F1 ≈ 0.96), but unrealistic.
* **Without Leakage** → Performance dropped (Random Forest F1 ≈ 0.90), which is a fairer representation.
* **Key Features**: Failures, absences, study time, parental support strongly influence passing.

---

## ⚖️ Ethics

* **Privacy**: No personally identifiable info is used.
* **Fairness**: Avoid relying too heavily on socio-economic variables.
* **Mitigation**: Focus on interpretable features like study habits and absences.

---

## ✅ Recommendations

1. Early support for students with **≥2 failures** or **high absences**.
2. Promote **study habits** (more study time → higher pass rate).
3. Encourage **family/teacher support programs**.
4. Monitor **students with low parental education** for extra tutoring.
5. Deploy predictive model in schools with care to avoid unfair bias.

---

## 📌 Limitations

* Dataset is small and may not generalize to all schools.
* Target is simplified (binary pass/fail).
* Future work: larger dataset, more robust ML models, fairness audits.

---

