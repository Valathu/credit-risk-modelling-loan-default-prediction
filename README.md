# Credit Risk Modelling and Loan Default Prediction

## Project Overview

This project develops a machine learning model to predict the probability of credit card default using customer demographic information, credit limits, repayment history, bill amounts, and previous payment amounts.

The objective is to understand how classification models can support credit risk assessment and identify customers who may be at a higher risk of default.

## Objectives

- Explore and prepare credit card customer data.
- Build Logistic Regression and Random Forest classification models.
- Compare model performance using classification and probability-based metrics.
- Select a classification threshold using validation data.
- Evaluate the selected model on an untouched test dataset.

## Dataset

The project uses a historical credit card default dataset containing 30,000 observations and 25 columns, including the target variable `dpnm`.

The target variable indicates whether a customer defaulted on payment:

- `0` — No default
- `1` — Default

The dataset relates to credit card clients in Taiwan and should not be interpreted as representative of all borrowers or the Indian lending market.

## Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Methodology

1. Loaded and inspected the dataset.
2. Checked missing values, duplicate records, and target class distribution.
3. Excluded the customer ID and separated the target variable.
4. Split the data into training, validation, and final test sets using stratified sampling.
5. Built preprocessing pipelines for numerical and categorical variables.
6. Trained Logistic Regression and Random Forest models.
7. Selected a classification threshold using validation data.
8. Evaluated the final Random Forest model on the untouched test set.

## Final Model Results

The selected Random Forest model was evaluated at a classification threshold of 0.30.

| Metric | Result |
|---|---:|
| Accuracy | 79.08% |
| Precision | 52.54% |
| Recall | 56.14% |
| F1-score | 54.28% |
| ROC-AUC | 0.7836 |
| Brier score | 0.1344 |

The model achieved a ROC-AUC of 0.7836, indicating useful discrimination between default and non-default cases. At the selected threshold, it identified 745 actual defaulters in the final test set, while missing 582 actual defaulters.

## Key Learnings

- Preparing numerical and categorical variables using preprocessing pipelines.
- Comparing Logistic Regression and Random Forest.
- Understanding the impact of class imbalance on classification metrics.
- Selecting a classification threshold based on validation performance.
- Evaluating model discrimination, classification errors, and probability predictions.

## Limitations

- The dataset represents historical credit card clients in Taiwan.
- The model has not been validated on current or Indian lending data.
- Predicted probabilities require further calibration assessment before interpretation as reliable individual default probabilities.
- The model has not undergone fairness, regulatory, or production validation.

This project is intended for academic learning and demonstration. It is not a production-ready credit decision system.

## Author

VAlathappan G | MSc Statistics Student | Interests: Credit Risk Analytics, Market Risk, and Quantitative Analytics

