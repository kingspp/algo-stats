# Confusion Matrix

A matrix table used to describe the performance of a classification model (or "classifier") on a set of 
test data for which the true values are known. 

There are four classes in Confusion Matrix:
1. **True Positives** - Class used to describe a state when True value and Predicted values are **high** [1 == 1]
2. **False Positives** - Class used to describe a state when True value is **low** and Predicted value is **high** [0 != 1]
3. **True Negatives** - Class used to describe a state when True value is **high** and Predicted value is **low** [1 != 0]
4. **False Negatives** - Class used to describe a state when True value and Predicted values are **low** [0 == 0]

#### Ex: 
**True Values**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = [1, 1, 0, 1, 1, 1, 0, 0, 1, 0] <br>
**Predicted Values** = [1, 0, 0, 1, 0, 1, 1, 1, 1, 0] <br>

#### Confusion Matrix:

| True/Pred     | 0 | 1  |
| ------------- |:-:| --:|
| 0             | 2 | 2 |
| 1             | 2 | 4 |


From the above matrix we can derive the following statistics:
#### 1. Accuracy: 
Accuracy of the Model:<br>
**Formula:** (TP+TN)/total = (4+2) / 10 = 60%

#### 2. Misclassification Rate (Error Rate):
How often the model is wrong. <br>
**Formula:** (FP+FN)/total = (2+2) / 10 = 40%

#### 3. Sensitivity (Recall):
Rate of True Positive - Rate of prediction of high when true values are high?<br>
**Formula:** TP/totan(True(1)) = 4 / 6 = 66.6%

#### 4. Specificity :
Rate of False Negative - Rate of prediction of low when true values are low <br>
**Formula:** TN/total(True(0)) = 2 / 4 = 50%

#### 5. Precision:
Correct Prediction of True Values<br>
**Formula:** TP/total(Predicted(1)) = 4 / 6 = 66.6%

#### References:
1. [Simple Guide for Confusion Matrix](http://www.dataschool.io/simple-guide-to-confusion-matrix-terminology/)
2. [Confusion Matrix - Wiki](https://en.wikipedia.org/wiki/Confusion_matrix)
3. [SKLearn Implementation](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)

