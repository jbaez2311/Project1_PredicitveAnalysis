# Offline Orders Prediction

## Executive Summary
The goal of this project is to analyze consumer online behavioral data and accurately predict their likelihood of making offline purchases. This README provides an overview of the project, data, methods, and results.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Data Profiling](#data-profiling)
4. [Machine Learning Workflow](#machine-learning-workflow)
   - [Step 1: Train-Test Split](#step-1-train-test-split)
   - [Step 2: Baseline Model with Logistic Regression](#step-2-baseline-model-with-logistic-regression)
   - [Step 3: Confusion Matrix Calculation](#step-3-confusion-matrix-calculation)
   - [Step 4: Evaluation Metrics](#step-4-evaluation-metrics)
   - [Step 5: Handling Imbalanced Data with SMOTE](#step-5-handling-imbalanced-data-with-smote)
   - [Step 6: Random Forest Classifier with Hyper-Parameter Tuning](#step-6-random-forest-classifier-with-hyper-parameter-tuning)
5. [Results and Interpretation](#results-and-interpretation)
6. [Future Work](#future-work)
7. [How to Run](#how-to-run)
8. [References](#references)

## Project Overview
This project utilizes consumer online behavioral data to predict offline purchase behavior. The analysis includes data profiling, machine learning model building, evaluation of models, and interpretation of the results. The primary goal is to achieve an accurate prediction model that can be used to optimize marketing efforts.

## Data Description
The dataset used in this project includes 1,171 records, each representing a unique user's online behavior. The key variables in the dataset include:
- **Pageviews**: Number of pages viewed by the user.
- **Time_On_Site**: Time spent on the site by the user.
- **Bounces**: Number of times the user bounced from the site.
- **Sessions**: Number of sessions initiated by the user.
- **Form_Submitted**: Whether the user submitted a form.
- **Primary_CTA_clicks**: Clicks on the primary Call-To-Action (CTA).
- **Secondary_CTA_clicks**: Clicks on the secondary CTA.
- **Tertiary_CTA_clicks**: Clicks on the tertiary CTA.
- **Product_Nav_clicks**: Clicks on product navigation links.
- **Product_Comparison_clicks**: Clicks on product comparison links.
- **Offline_Sale**: Whether the user made an offline purchase (target variable).

## Data Profiling
A thorough data profiling was conducted using YData Profiling to understand the dataset better. Key findings include:
- No missing data points.
- No duplicate rows.
- High correlation between `Form_Submitted` and `Pageviews`.

## Machine Learning Workflow

### Step 1: Train-Test Split
The dataset was split into training and testing sets to evaluate model performance. The target variable is `Offline_Sale`, and the features include various numerical variables related to user behavior.

### Step 2: Baseline Model with Logistic Regression
A logistic regression model was initially trained to establish a baseline for hyper-parameter tuning.

### Step 3: Confusion Matrix Calculation
A confusion matrix was calculated to evaluate the baseline model’s performance in predicting offline purchases.

### Step 4: Evaluation Metrics
Standard evaluation metrics, including precision, recall, F1 score, and accuracy, were calculated to assess the model's effectiveness.

### Step 5: Handling Imbalanced Data with SMOTE
The Synthetic Minority Over-sampling Technique (SMOTE) was applied to address the imbalanced nature of the dataset, ensuring that the model could learn effectively from both positive and negative cases.

### Step 6: Random Forest Classifier with Hyper-Parameter Tuning
A Random Forest Classifier was trained with hyper-parameter tuning to improve the model's predictive performance, focusing on optimizing the F1 score.

## Results and Interpretation
The best-performing model achieved significant improvements in precision, recall, and F1 score, indicating a more balanced and meaningful ability to predict offline purchases.

## Future Work
Further improvements can be made by:
- Fine-tuning the decision threshold to balance precision and recall.
- Exploring more advanced models, such as ensemble methods or deep learning approaches.
- Regularly updating the model with new data and incorporating additional behavioral metrics.

## How to Run
To run this project, follow these steps:
1. **Clone the Repository**: Ensure you have the project files, including the dataset and necessary scripts.
2. **Set Up the Environment**: Install the required Python packages using the provided `requirements.txt` file.
3. **Execute the Notebook**: Run the Jupyter Notebook or Python scripts in your environment. The analysis will load the dataset, perform data profiling, and execute the machine learning workflow to predict offline purchases.
4. **Review the Results**: After execution, review the output metrics and model performance for insights.

## References
- Scikit-learn documentation: [Logistic Regression](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression)
- YData Profiling: [YData](https://ydata.ai/)
- SMOTE: [Imbalanced-learn documentation](https://imbalanced-learn.org/stable/over_sampling.html#smote)
