# credit_risk-classification

## Overview of the Analysis
The purpose the the analysis was the create a classification model to sort through credit score data. There was either a healthy loan (0) or a risky loan (1). The data invloved a number of factors that could influence if someone was considered a healthy or risky loan. There was information about the size of the loan, the amount of debt, the borrower income and other things. These factors, or features, influenced the loan score of 0 or 1, which was the target variable. There was more data for the 0 data than the 1 data when the value_counts function was used. 

To create the model, I split the data into a training set and a testing set. I used the LogisticRegression to classify the data and used the training data (X_train and y_train) to fit the model. I calculated the predicted values and compared those to the test data. Since there was more 0 data than 1 data, I oversampled and did the process again. 

## Results
Using the oversampled data led to better or the same recall, precision, and accuracy scores. 

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Accuracy was 94%
  * Recall and Precision for 0 were both 1.0
  * Recall and Precision for 1 were .89 and .87.
  * There were more false negatives and false positives in the 1 category

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Accuracy was 99%
  * Recall and Precision for 0 were both 1.0 again
  * Recall and Precision for 1 were 1.0 and .87
  * Recall, Precision, and Accuracy improved with fewer or the same false negatives and false positives

## Summary
Overall, there were more false negatives and false positives in the first model. This means that people who aren't risky are being identified as risky and people who are risky aren't gettting identified. This will cost money. The second model has fewer false negatives and a few more false positives even if the classification report said it was the same. The second model had fewer people who weren't risky being identified as risky. There were the same or more people who were risky, but not identified. The second model is better because accuracy and recall improved, but it wasn't enough improvement in the right category. 

I don't think I would recommend either model. The data will influence if you want to limit false positives or false negatives. In this case, people who are risky are being identified for healthy loans and this will probably cost more money. Those people are the false positive people and neither model limited the number of false positives. The false negatives could appeal the decision, but the false positive people are already on their way to a loan. Both people had the same .87 in the classification report and there were 11 more in the confusion matrix of the second model. I wouldn't want either model because between the two model about 85 people are being identified for healthy loans and shouldn't. As the client, I wouldn't want that many false positives. 
