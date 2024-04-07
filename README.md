# Hackathon - Loan Repayment Assessment in Banking 
Submitted by - Gayathri Keerthivasagam
## Problem Statement

  Build and train a model that identifies a customer will repay or default from
the loan dataset.

  The primary objective is to create a reliable tool that assists the bank in assessing
the creditworthiness of loan applicants, thereby minimizing the risk of default and
optimizing lending decisions.

## Data collection and Exploration

  The dataset was sourced from the provided link  and the data description is mentioned in detail in the ppt attached.
  
  A comprehensive exploration of the dataset was conducted, meticulously examining each feature in detail. 
  
  Different visualization techniques such as histograms, box plots, pair plots, count plots are used to understand relationships between features and target variable.

## Data Cleaning and Preprocessing

  Observed null values in the following features 
      emp_length
      emp_title
      num_actv_bc_tl
      mort_acc
      tot_cur_bal
      pub_rec_bankruptcies
      revol_util and title
  
  Null values were imputed successfully using either the mean or median based on the business requirements.

  No duplicates found in the training dataset.

  ## Feature Engineering and Selection

  The target label is encoded as 0 and 1.
  
  Heatmap is plotted to identify the correlation between the numerical features.
  
  The outliers are visualized and successfully removed wherever it is needed.

  Features like pub_rec, pub_rec_bankruptcies, fico_range are successfully grouped and labelled.

  Dropped the least important features like ‘grade’, ’emp_ title’, ’emp_length’ according to the chi-square statistical methods.

  Performed feature encoding (one hot encoding) for categorical features.

  Performed feature scaling  for numerical features.

## Dealing with Imbalanced Data

  Techniques used for balancing the data:
  
    SMOTE
    Random Undersampling
    Random Oversampling
    
  A detailed comparative analysis was conducted for different resampling techniques and identified the best sampling method for better f1-score.

## Model Selection

  ML models used are
  
     Logistic regression
     K Nearest Neighbors
     Random Forest Classifier
     Gradient Boosting.
     XGBoost
    
Found the ensemble technique of  Logistic regression + XGBoost outperforms in the F1 score.

## Hyperparameter Tuning

  A grid search is conducted to find optimal parameters (penalty,C) for logistic regression.

  A grid search is conducted to find optimal parameters (n_estimators, max_depth, learning_rate) for  XGBoost.
  
  Following the search, the best estimator are identified. 
  
  The soft vote-based ensemble classifier has been implemented using XGBoost and logistic Regression.

## Prediction on Test Dataset

  The preprocessing for test dataset is done in the same manner as the train dataset.
  
  The successfully trained tuned model is fitted on the test dataset.
  
  The prediction for ‘loan_status’ is done and saved as a excel file 'loan_status_test'.

Thanks for reading!!


######################################################################################################

  


















