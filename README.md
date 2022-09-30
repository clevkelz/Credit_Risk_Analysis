# Credit Risk Analysis

## Overview of the Analysis

Recent data on loans made by LendingClub, a peer-to-peer lending services company, were reviewed to determine whether a robust model could be developed to help predict the borrowers’ ability to repay based on this information.  These data contained information related to the loan, such as the amount, term, and repayment history, as well as borrower information including income, total amount of debt, and number of open accounts.  The data also housed a field showing the loan status, which was recorded as current, late (16-30 days), late (31-120 days), in default, and in grace period.  Different models, as listed in the Results section of this analysis, were run to determine whether patterns in the historical data could accurately predict future behavior.  All loans not classified as current were deemed to be high risk.  The accuracy of the models’ ability to identify applicants that were low-risk and thus, more likely to pay loans, and conversely high-risk applicants, was reviewed to determine if any of them would be optimal for use.

## Results

The balanced accuracy, precision, and recall scores of the six machine learning modules used are presented below:

## Naive Random Oversampling

### Balanced Accuracy Score

![image](https://user-images.githubusercontent.com/106293233/193350696-1606b085-06f8-4b21-b6b3-63dd5e6b728a.png)
 
•	The balanced accuracy score for the Naive Random Oversampling Model is 0.65.

### Precision and Recall Scores

![image](https://user-images.githubusercontent.com/106293233/193350776-fd49473a-82d7-4cd5-a131-6f5c87ce2a11.png)
 
*	The precision score is 0.01 for high-risk loans and 1.00 for low-risk loans.
*	The recall score is 0.62 for high-risk loans and 0.68 for low-risk loans.



 





