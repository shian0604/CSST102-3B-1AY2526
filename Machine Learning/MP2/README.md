# 🎓 Test Preparation Course Completion Prediction

## 📌 Project Overview
This project explores whether student **scores** and **demographic factors** can predict if a student **completed a test preparation course**.  
We compare two machine learning models — **Logistic Regression** and **Random Forest Classifier** — to highlight how different algorithms behave on the same dataset.  

The teaching angle is to show that **correlation ≠ causation**: just because a model finds patterns doesn’t mean prep completion is caused by those features.

---

## 📊 Dataset Description
- **Target Variable:**  
  `test preparation course` → `"completed"` vs `"none"`

- **Features:**  
  - **Scores:** math, reading, writing  
  - **Demographics:** gender, race/ethnicity, parental education, lunch type  

- **Preprocessing:**  
  - One‑hot encoding for categorical features  
  - Standardization for numerical features  

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Encoded categorical variables  
- Normalized numerical features  
- Defined target (`test preparation course`)  

### 2. Train–Test Split
- 80% training, 20% testing  
- Stratified to preserve class balance  

### 3. Model Training
- **Logistic Regression** (baseline linear model)  
- **Random Forest Classifier** (non‑linear ensemble model)  

### 4. Evaluation
- Training & testing accuracy  
- **5‑Fold Cross Validation** (mean & std deviation)  
- Confusion Matrix  
- Accuracy, Precision, Recall, F1‑score  
- Learning Curve Visualization  

---

## 📈 Results

### Logistic Regression
- **Mean CV Accuracy:** 0.7300  
- **Std Dev:** 0.0249  
- Stable performance across folds  
- Balanced generalization  

### Random Forest Classifier
- **Training Accuracy:** 1.0000  
- **Testing Accuracy:** ~0.6500  
- **Mean CV Accuracy:** 0.6750  
- **Std Dev:** 0.0239  
- Clear signs of **overfitting**  

### Confusion Matrix Insights
- Both models predicted `"none"` more reliably than `"completed"`  
- Recall for `"completed"` was weaker → many false negatives  

### Learning Curves
- Logistic Regression: well‑fitted, stable generalization  
- Random Forest: training curve near 1.0, validation curve much lower → overfitting  

---

## 💡 Key Takeaways
- **Simpler ≠ weaker**: Logistic Regression outperformed Random Forest in this dataset.  
- **Overfitting matters**: Random Forest memorized training data but failed to generalize.  
- **Evaluation beyond accuracy**: Precision, recall, F1, and confusion matrices reveal deeper insights.  
- **Teaching moment**: This project is ideal for showing students how to interpret model performance, question causality, and reflect on fairness and bias in predictive modeling.  

---

## 🚀 Next Steps
- Visualize **feature importance** for Random Forest  
- Try other models (SVM, Gradient Boosting, XGBoost)  
- Explore **class imbalance handling** (resampling, class weights)  
- Extend lab activities with **student reflection questions** on fairness and causality
