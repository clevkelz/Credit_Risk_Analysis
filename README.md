# Credit Risk Analysis

## Overview of the Analysis

Recent data on loans made by LendingClub, a peer-to-peer lending services company, were reviewed to determine whether a robust model could be developed to help predict the borrowers’ ability to repay based on this information.  These data contained information related to the loan, such as the amount, term, and repayment history, as well as borrower information including income, total amount of debt, and number of open accounts.  The data also housed a field showing the loan status, which was recorded as current, late (16-30 days), late (31-120 days), in default, and in grace period.  Different models, as listed in the Results section of this analysis, were run to determine whether patterns in the historical data could accurately predict future behavior.  All loans not classified as current were deemed to be high risk.  The accuracy of the models’ ability to identify applicants that were low-risk and thus, more likely to pay loans, and conversely high-risk applicants, was reviewed to determine if any of them would be optimal for use.

## Results

The balanced accuracy, precision, and recall scores of the six machine learning modules used are presented below:

### Naive Random Oversampling

#### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193350696-1606b085-06f8-4b21-b6b3-63dd5e6b728a.png)
 
•	The balanced accuracy score for the Naive Random Oversampling Model is 0.65.

#### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193350776-fd49473a-82d7-4cd5-a131-6f5c87ce2a11.png)
 
*	The precision score is 0.01 for high-risk loans and 1.00 for low-risk loans.
*	The recall score is 0.62 for high-risk loans and 0.68 for low-risk loans.

### SMOTE Oversampling

#### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193351420-8dabe5b8-b024-48f1-8820-f8aafff186be.png)

* The balanced accuracy score for the SMOTE Oversampling Model is 0.64.

#### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193351640-29d5bbb3-6c22-4187-add6-b652c21d6bcf.png)

* The precision score is 0.01 for high-risk loans and 1.00 for low-risk loans.
* The recall score is 0.63 for high-risk loans and 0.66 for low-risk loans.

### Undersampling

#### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193351961-e7170d66-2796-4aa6-aa91-cee0c83e474e.png)

* The balanced accuracy score for the Undersampling Model is 0.64.

#### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193352149-0a4217e9-0bfb-455a-80c7-df47e719a066.png)

* The precision score is 0.01 for high-risk loans and 1.00 for low-risk loans.
* The recall score is 0.60 for high-risk loans and 0.43 for low-risk loans.

### Combination (Over and Under) Sampling

#### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193352382-68308c69-f2a8-4c3e-9ea0-bd5a22d478d8.png)

*	The balanced accuracy score for the Combination (Over and Under) Sampling Model is 0.64.

#### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193352514-c7ec5f9d-fee4-47d0-b1b7-c7964d770145.png)

* The precision score is 0.01 for high-risk loans and 1.00 for low-risk loans.
* The recall score is 0.70 for high-risk loans and 0.57 for low-risk loans.

### Balanced Random Forest Classifier

#### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193352779-263e0b16-d967-4d34-90d0-957ad9930a15.png)

* The balanced accuracy score for the Balanced Random Forest Classifier Model is 0.79.

#### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193352936-04028a47-5697-47c1-839d-9a13bf23bd37.png)

* The precision score is 0.04 for high-risk loans and 1.00 for low-risk loans.
* The recall score is 0.67 for high-risk loans and 0.91 for low-risk loans.

### Easy Ensemble AdaBoost Classifier

#### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193353122-9f18d62b-143c-4377-ad09-eea1a6a41208.png)

* The balanced accuracy score for the Easy Ensemble AdaBoost Classifier Model is 0.93.

#### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193353310-2e5ce32a-b0a5-4236-9541-f76ee18aaeae.png)

* The precision score is 0.07 for high-risk loans and 1.00 for low-risk loans.
* The recall score is 0.91 for high-risk loans and 0.94 for low-risk loans.

## Summary

### Overview of Results

Most of the models had accuracy scores around 65%.  The accuracy improved sharply for the Balanced Random Forest Classifier Model and was highest for Easy Ensemble AdaBoost Classifier Model.  The latter two models are ensemble methods, which use multiple learning algorithms to enhance models’ ability to predict patterns.  The other models use resampling methods which involve repeatedly taking samples from a subset of data called the training data, drawing conclusions from the data, predicting how that would extrapolate to the remaining data (the test data), and then comparing the projected results on the test data to the actual test data.

The precision scores were very low for high-risk loans and high for low-risk loans.  The recall, or sensitivity scores, were around 60% for high-risk and low-risk loans for the non-ensemble methods.  The recall scores were generally much higher for the ensemble methods.

The F1 score takes into account both the precision and recall scores.  Using this score can help balance precision and sensitivity when selecting a model.  The F1 scores are very low for all methods in attempting to identify which borrowers will likely default on their loans but there is a substantial increase in the score with the AdaBoost Classifier Model.

### Recommended Method to Use

Models to predict credit risk can be very helpful in quickly screening borrowers during the credit decision process.  These automated decisions can often allow financial institutions to offer credit at lower costs because of reduced overhead and can also result in more consistent credit decisions.  Although none of the models were very precise in predicting high-risk loans, the accuracy and sensitivity scores of the Easy Ensemble AdaBoost Classifier Model were high.  Therefore, this model is recommended for use. 
