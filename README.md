# ILPD Analysis & Classification

This project performs a complete analysis and classification on the Indian Liver Patient Dataset (ILPD) using Python, with improved visualizations and a standard machine learning workflow.

## 1. Features and Labels

- **Features** → All columns except `Selector` (Age, Gender, TB, DB, Alkphos, Sgpt, Sgot, TP, ALB, AG_Ratio). These serve as input data for the ML models.  
- **Labels** → `Selector` → The target we are trying to predict (`0 = no liver disease`, `1 = liver disease`).  

This follows the typical machine learning setup: features (`X`) → label (`y`).

## 2. Preprocessing

- **Handling missing values (NaN)** → Required because most ML algorithms cannot handle missing data.  
- **Encoding categorical variables (Gender)** → Converts "Male/Female" into numbers so ML algorithms can use it.  
- **Standard scaling** → Normalizes numeric features so models like Logistic Regression, KNN, and MLP perform better.  

All of these are standard preprocessing steps in machine learning workflows.

## 3. Model Training & Evaluation

Multiple classifiers were used to train and evaluate the data:

- Logistic Regression  
- K-Nearest Neighbors (KNN)  
- Naive Bayes  
- Decision Tree  
- Random Forest  
- Multilayer Perceptron (MLP)  

Each classifier is a machine learning model.  

- **Cross-validation (`cross_val_score`)** → Evaluates model performance using cross-validation, which helps prevent overfitting and provides a reliable estimate of accuracy.

## 4. Classifier Accuracy Results

| Classifier             | Accuracy |
|------------------------|----------|
| Logistic Regression    | 0.7039   |
| K-Nearest Neighbors    | 0.6395   |
| Naive Bayes            | 0.5470   |
| Decision Tree          | 0.6352   |
| Random Forest          | 0.7016   |
| Multilayer Perceptron  | 0.6847   |

- **Best performing classifier** → Logistic Regression with accuracy `0.7039`.

## 5. Output & Visualizations

- **Accuracy scores** → Each model's performance is listed in the table above.  
- **Visualizations** → Plots for Age distribution, Gender distribution, Selector distribution, and Correlation heatmap are saved in the `ILPD_Visuals` folder within this project.

### Summary

Every step after loading and cleaning the data — scaling, encoding, training classifiers, evaluating accuracy — follows a classic machine learning workflow for classification tasks.
