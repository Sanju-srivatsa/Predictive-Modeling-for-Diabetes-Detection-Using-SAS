# Predictive Modeling for Diabetes Detection: A Comprehensive Approach Using SAS

## **Introduction**
Diabetes is a chronic condition affecting millions worldwide. Early detection and management of diabetes are crucial for improving patients' quality of life and reducing healthcare costs. Predictive modeling has emerged as a powerful tool for identifying individuals at risk of diabetes, enabling timely interventions.

This project leverages SAS to develop a predictive model for diabetes detection using clinical and demographic data. The project follows a systematic approach, including data cleaning, feature engineering, modeling, and evaluation.

---

## **Problem Statement**
Diabetes is often underdiagnosed due to limited access to early diagnostic tools and the complexity of associated risk factors. A robust predictive model can help healthcare providers identify high-risk individuals more effectively.

Key challenges include:
- Handling missing and biologically invalid data.
- Addressing the class imbalance in diabetes outcomes.
- Selecting significant predictors for reliable and interpretable models.

---

## **Objective**
The primary objective is to build a logistic regression model capable of predicting the likelihood of diabetes based on clinical and demographic features. The project aims to:
1. Clean and preprocess raw data to ensure high-quality input.
2. Engineer meaningful features to enhance model performance.
3. Develop a predictive model and evaluate its effectiveness using key metrics.
4. Apply the model to a test dataset for real-world validation.

---

## **Purpose**
This project highlights the application of data science in healthcare. By identifying significant predictors of diabetes, it contributes to understanding the factors influencing the disease. The project emphasizes:
- **Improving Diagnostic Accuracy**: Supporting healthcare professionals in making data-driven decisions.
- **Enhancing Patient Outcomes**: Enabling early interventions for high-risk individuals.

---

## **Real-World Applications**
1. **Clinical Decision Support**: Helping clinicians identify high-risk patients during routine checkups.
2. **Public Health Programs**: Guiding resource allocation for diabetes prevention campaigns.
3. **Health Insurance**: Assisting insurers in risk assessment for policy design.

---

## **Project Workflow**

### **1. Data Import and Initial Overview**
- Imported the diabetes dataset containing 768 records and 9 variables.
- Conducted exploratory analysis to understand dataset structure and metadata.
- Sample data:
  - **Glucose**: Mean = 121.69, Std Dev = 30.44
  - **BMI**: Mean = 32.46, Std Dev = 6.88
  - **Age**: Mean = 33.24, Std Dev = 11.76

### **2. Data Cleaning**
- Identified and replaced biologically invalid zeros in key variables (e.g., Glucose, BMI) with missing values.
- Imputed missing values using the mean.

### **3. Descriptive Statistics**
- Summarized key variables, highlighting variability and central tendencies.
- Analyzed the outcome distribution:
  - 34.9% diabetic (Outcome = 1).
  - 65.1% non-diabetic (Outcome = 0).

### **4. Correlation Analysis**
- Identified strong predictors like glucose, BMI, and age.
- Evaluated relationships between variables to guide feature selection.

### **5. Feature Engineering**
- Standardized numerical variables for better model performance.
- Created interaction terms and categorized BMI into classes: Underweight, Normal, Overweight, Obese.

### **6. Logistic Regression Modeling**
- Built and refined a logistic regression model using stepwise selection.
- Key predictors: Glucose, BMI, Age, BMI Category.
- Evaluated model performance:
  - **Accuracy**: 76.6%
  - **Precision**: 70.8%
  - **Recall**: 56.0%
  - **Specificity**: 87.6%
  - **AUC**: 0.834

### **7. Scoring and Predictions**
- Applied the model to a test dataset.
- Standardized test data using training means and standard deviations.
- Predicted probabilities and classes for each test observation.

---

## **Results**
### **Key Findings**
1. **Model Performance**:
   - Achieved a balance between precision and recall, with strong specificity.
   - Glucose and BMI emerged as critical predictors of diabetes risk.

2. **Confusion Matrix**:
   - True Positives: 150
   - True Negatives: 438
   - False Positives: 62
   - False Negatives: 118

3. **AUC**: The model's ability to distinguish between diabetic and non-diabetic cases was high (AUC = 0.834).

### **Test Dataset Results**
- Example prediction: An individual with high glucose and BMI was correctly identified as diabetic with a probability of 93.7%.
- Predicted classes and probabilities were exported for further analysis.

---

## **Conclusions**
This project demonstrates the effective use of logistic regression for predicting diabetes. The model's strong specificity ensures minimal false positives, making it suitable for healthcare applications where over-diagnosis can lead to unnecessary interventions.

---

## **Future Recommendations**
1. **Improve Recall**: Experiment with alternative thresholds or advanced algorithms like random forests or neural networks.
2. **Integrate Additional Features**: Include lifestyle or genetic factors for a more comprehensive model.
3. **Deployment**: Develop a web or mobile application to provide real-time diabetes risk assessment.
