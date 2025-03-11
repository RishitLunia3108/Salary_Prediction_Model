# Salary Prediction Model

## 📄 Overview
This project involves the development of a robust salary prediction model to estimate salaries based on various candidate attributes such as experience, education, technical skills, and engagement metrics. The model leverages advanced feature engineering and machine learning techniques to achieve high accuracy and interpretability.

---

## 🚀 Key Features

### 1. **Data Preprocessing**
- Cleaned and normalized salary data (CTC) to ensure consistency and removed outliers.
- Handled missing values using median imputation for numeric features and encoded categorical variables using `LabelEncoder`.

### 2. **Feature Engineering**
- Created advanced features to enhance model performance:
  - **Experience-based features**: Squared experience, experience flags, and career level bands (Entry, Mid, Senior, Expert).
  - **Education score**: Weighted mapping of qualifications (e.g., B.Tech, M.Tech, MCA) to numerical scores.
  - **Skill scores**: Aggregated technical (coding, DSA) and non-technical scores into overall engagement metrics.
  - **Interaction features**: Combined experience, education, and technical scores to capture complex relationships.
  - **Attendance and submission rates**: Calculated attendance and submission rates for coding, DSA, and non-technical tasks.
  - **Tech stack grouping**: Standardized and grouped tech stacks into top categories (e.g., MERN, JAVA, OTHERS).
- Generated bucketed metrics for attendance, attempts, and submissions to analyze performance across ranges.

### 3. **Model Development**
- Used **XGBoost Regressor** as the primary model due to its efficiency and ability to handle complex relationships in data.
- Designed a robust pipeline for training and evaluation, including feature scaling with `StandardScaler` and 5-fold cross-validation to ensure generalization.

### 4. **Model Evaluation**
- Achieved **80% accuracy** with detailed performance metrics:
  - **R² Score**: Evaluated the proportion of variance explained by the model.
  - **RMSE (Root Mean Squared Error)**: Measured prediction error magnitude.
  - **MAE (Mean Absolute Error)**: Assessed average prediction error.
  - **MAPE (Mean Absolute Percentage Error)**: Evaluated percentage-based prediction accuracy.
- Conducted error analysis and evaluated performance across salary bands (e.g., 0-3L, 3-6L, 6-9L).

### 5. **Feature Importance Analysis**
- Identified the most influential features, such as technical scores, education scores, and experience-based metrics.
- Grouped features into categories (e.g., Experience, Education, Technical, Non-Technical) to analyze their relative contributions to salary predictions.

### 6. **Deployment and Predictions**
- Designed a reusable pipeline for predicting salaries of new candidates by applying the same preprocessing and feature engineering steps.
- Saved the trained model, encoders, and feature list as artifacts for deployment and reproducibility.

---

## 📊 Results
- **Accuracy**: 80%
- **Key Metrics**:
  - **R² Score**
  - **RMSE (Root Mean Squared Error)**
  - **MAE (Mean Absolute Error)**
  - **MAPE (Mean Absolute Percentage Error)**
- **Error Analysis**: Detailed evaluation across salary bands and error distributions.

---

## 🛠️ Technologies Used
- **Programming Language**: Python
- **Libraries**: XGBoost, Pandas, NumPy, Scikit-learn
- **Tools**: LabelEncoder, StandardScaler, KFold Cross-Validation

---

## 💻 How to Use

1. **Preprocess Data**: Use the `prepare_data` function to clean and preprocess the dataset.
2. **Train Model**: Train the model using the provided pipeline and evaluate its performance.
3. **Make Predictions**: Use the `predict_salary` function to predict salaries for new candidates.
4. **Analyze Results**: Evaluate feature importance and performance metrics to interpret the model.

---

## 📈 Conclusion
This project demonstrates an end-to-end machine learning workflow, including data preprocessing, feature engineering, model training, evaluation, and deployment. The salary prediction model achieves reliable and interpretable results, making it a valuable tool for estimating salaries based on candidate attributes.

