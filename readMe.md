# Employee Hiring and Retention Challenges

Hiring and retaining employees are extremely complex tasks that require **capital, time, and skills**. Small business owners spend **40% of their working hours** on tasks that do not generate any income, such as hiring. Additionally, companies spend **15% - 20% of an employee's salary** to recruit a new candidate.

An average company loses anywhere between **1% and 2.5% of their total revenue** due to the time it takes to bring a new hire up to speed. The cost of hiring a new employee varies, but for companies with **0 - 500 employees**, the average cost is **$7,645**. Furthermore, it takes **52 days on average** to fill a position.

**Source:** [The True Cost of Hiring an Employee in 2024](https://toggl.com/blog/cost-of-hiring-an-employee)

---

## Employee Attrition Prediction

As a **data scientist** at a multinational corporation, you have been approached by the **HR team** to develop a **predictive model** that can determine which employees are more likely to quit. The HR team has collected **extensive employee data**, and a sample of the dataset includes the following features:

- **JobInvolvement**
- **Education**
- **JobSatisfaction**
- **PerformanceRating**
- **RelationshipSatisfaction**
- **WorkLifeBalance**

**Data Source:** [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset)

---

## Project Overview

This project aims to develop a **predictive machine learning model** to determine whether an employee is likely to leave the company. The goal is to help HR teams **reduce attrition rates**, retain valuable employees, and make **data-driven hiring and retention decisions**.

To achieve this, three machine learning models were trained and evaluated:

1. **Logistic Regression** – a baseline model for interpretability.
2. **Random Forest Classifier** – a tree-based ensemble learning model.
3. **Neural Network** – a deep learning-based approach for complex patterns.

---

## Dataset Description

The dataset used for this project comes from IBM HR Analytics and contains various features related to employees' professional and personal experiences. Some key attributes include:

- **Employee Demographics:** Age, Gender, Education
- **Job-Related Factors:** Job Role, Department, Business Travel, Training Time
- **Performance & Satisfaction:** JobInvolvement, JobSatisfaction, PerformanceRating
- **Work-Life Balance:** WorkLifeBalance, OverTime, MonthlyIncome

The dataset was preprocessed by handling missing values, normalizing numerical features, encoding categorical variables, and splitting into training and testing sets.

---

## Modeling Approach

### **1. Data Preprocessing**
- **Encoding categorical variables** (One-Hot Encoding for categorical data like Department, Job Role, etc.).
- **Feature scaling** (MinMax Scaling for numerical variables).
- **Splitting the dataset** (75% training, 25% testing).

### **2. Model Training**
Three machine learning models were trained:

- **Logistic Regression:** A simple, interpretable model to serve as a baseline.
- **Random Forest Classifier:** A robust ensemble model that improves prediction accuracy.
- **Neural Network:** A deep learning model capable of capturing complex relationships in the data.

### **3. Model Evaluation**
Each model was evaluated based on:

- **Accuracy** – Overall performance of the model.
- **Precision** – Correctly predicted positives vs. total predicted positives.
- **Recall** – True positives captured vs. actual positives.
- **F1-Score** – Harmonic mean of precision and recall.
- **Confusion Matrix** – Breakdown of correct and incorrect classifications.

---

## Results and Model Comparison

| Model              | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |
|-------------------|---------|------------------|------------------|------------------|
| Logistic Regression | 88%     | 0.79             | 0.37             | 0.51             |
| Random Forest      | 85%     | 0.60             | 0.15             | 0.24             |
| Neural Network     | 86%     | 0.60             | 0.42             | 0.50             |

**Key Takeaways:**
- **Logistic Regression** performs best in terms of accuracy (**88%**) and is highly interpretable.
- **Random Forest** achieves **85% accuracy** but has very low recall for predicting employees likely to leave.
- **Neural Network** provides a better recall (**0.42**) for quitting employees while maintaining an overall accuracy of **86%**.

---

## Conclusion

### Model Comparison and Selection

In this study, we evaluated three different models—**Logistic Regression, Random Forest, and a Neural Network**—to predict employee attrition. The classification reports for each model indicate the following key insights:

1. **Logistic Regression**:
   - Achieved an accuracy of **88%**.
   - **High precision (0.89) and recall (0.98) for non-quitting employees (Class 0)**.
   - **Moderate precision (0.79) but low recall (0.37) for quitting employees (Class 1)**.
   - Performs well overall but struggles with recall for predicting employees who are likely to quit.

2. **Random Forest**:
   - Achieved an accuracy of **85%**.
   - **Precision for Class 1 (0.60) is lower, and recall (0.15) is significantly poor**, making it ineffective at predicting employees likely to leave.
   - This model is more biased toward predicting employees who stay, reducing its usefulness in attrition prediction.

3. **Neural Network**:
   - Achieved an accuracy of **86%**.
   - **Balanced performance between precision (0.60) and recall (0.42) for quitting employees (Class 1)**.
   - This model captures more quitting employees than Random Forest but still has room for improvement.

### Final Recommendation

Based on the results, **Logistic Regression provides the best overall accuracy (88%)** and performs well for predicting employees who stay. However, its recall for quitting employees is still low (**0.37**), meaning it misses many actual attrition cases.

If the goal is to **maximize recall for quitting employees**, the **Neural Network is the best option** as it provides a more balanced prediction between staying and leaving employees. However, it still requires further optimization.

To improve predictions, **cost-sensitive learning, resampling techniques (SMOTE), or feature engineering** could be applied to enhance recall for quitting employees while maintaining overall performance.

---

## Future Improvements

To enhance model performance, the following approaches could be explored:

- **Feature Engineering:** Incorporate additional features such as work history trends, promotions, and employee surveys.
- **Handling Class Imbalance:** Use **oversampling (SMOTE)** or adjusting class weights to improve recall for attrition cases.
- **Advanced Models:** Try **XGBoost or ensemble stacking** to combine the strengths of multiple models.
- **Explainability Techniques:** Use **SHAP or LIME** to help HR professionals interpret model predictions.

This project highlights the power of **machine learning in workforce analytics** and provides HR teams with **data-driven insights to reduce employee turnover** effectively.

