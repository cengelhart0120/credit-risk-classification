# <p align="center">Module 20 Challenge: Supervised Machine Learning with Python
## Data Analytics assignment to train and evaluate a model of creditworthiness of borrowers based on fictitious lending data
### Overview
#### Purpose
The purpose of this (and any) analysis of creditworthiness is to assess the risk associated with extending credit to an individual or entity, to help answer the question "Does this potential borrower have the capability and reliability to repay their debt obligation(s) in a timely manner?"
#### Explanation of Data
The (fictional) dataset of historical lending activity from a peer-to-peer lending services company included the following information:
- Loan amount
- Interest rate of loan
- Borrower's income
- Borrower's debt-to-income ratio
- Borrower's number of credit accounts
- Number of derogatory marks on borrower's credit history
- Borrower's total debt
- **Loan status** (healthy vs. at high risk of defaulting)
    - **This** is the variable the model was created to predict; Would the outcome of lending to an individual with certain metrics be favorable or unfavorable?
    - Provided as a Boolean value in the dataset: `0` for "healthy" and `1` for "at-risk"
#### Methods
1. Data was split into training and testing sets using `train_test_split` from `scikit-learn`
2. The training data was fit using `LogisticRegression` from `scikit-learn` with the `lbfgs` solver
3. Predictions were made on the test set using the trained model
4. The model's performance was evaluated using a `confusion_matrix` and `classification_report` from `scikit-learn`
### Results
The logistic regression model used here yielded the following scores:
- 99% for **accuracy**, which measures the overall correctness of the model by dividing the number of correct predictions by the total number of predictions.
- Nearly total (99.7%) **precision** for predicting healthy loans, and 85% for predicting high-risk loans. **Precision** measures the model's ability to avoid false positives, and is calculated by dividing the number of true positives by the sum of true and false positives.
- 99% **recall** (also known as sensitivity) for predicting healthy loans, and 91% for prediciting high-risk loans. **Recall** measures the model's ability to avoid false negatives, and is calculated by dividing the number of true positives by the sum of true positives and false negatives.
### Summary
My personal experiences working with models to "fit" data have been pretty narrow and related mostly to my education and career in biological and physical sciences and engineering. Based on this background, my rule of thumb has generally been to stick with models that have upper nineties percentage values (>95% at the very minimum) wherever possible, otherwise the data are too broad or too many variables contribute to the composition of each data point. That being said, this is a real-world application of fitting data to a model, and besides the creditworthiness model's 85% precision for predicting high-risk loans, all other scores are 91% or higher. Generalized/simplified, this suggests that the model would be correct about every 9 out of 10 predictions. Whether this is sufficient for a financial institution is up to that particular institution, but my gut says that this is likely a reasonably good model for predicting creditworthiness.
### Further Information
#### Prerequisites
- Familiarity with and use of the Python programming language, and software to interact with .ipynb files, such as [Jupyter Notebook](https://jupyter.org/)
#### Usage
- Download the contents of the repo (as they are) to the same directory
- Launch Jupyter Notebook, navigate to the appropriate directory, and open `credit_risk_classification.ipynb`
- If desired, clear outputs and inspect/run the code cell by cell, paying attention to prompts and comments throughout
- Have fun exploring/playing around with the data/code! What are some ways the code could be made more clear or efficient? Are there other models/methods that could be used to improve the accuracy, precision, and recall scores achieved by this model/method?
### License
[MIT License](https://opensource.org/licenses/MIT)
### Contact
[Email](mailto:cengelhart@gmail.com)\
[GitHub](https://github.com/cengelhart0120)