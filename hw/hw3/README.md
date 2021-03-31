# CPE 695 - Applied ML HW 3 Written

> I pledge my Honor that I have abided by the Stevens Honor System - Joshua Schmidt 3/30/21

## Question 1

1. Explain what is the bias-variance trade-off? Describe few techniques to reduce bias and variance respectively.

Bias is the difference between the average output of a given model and the target value. Variance is the spread or variability of the model output. Models with high bias tend to pay little attention to the training data and oversimplify the output. Models with high variance tend to pay too much attention to the training data and are overfit. Models with low variance and bias are a good fit to the training data. Finding the right balance between variance and bias to produce the best possible model is the bias-variance trade-off. Typically if a model has a large number of parameters, the variance is high and the bias is low (and vice-versa for a lower number of parameters). To reduce bias, increase the number of parameters, try a different model, or ensure the training data is truly representative of the target. To reduce variance, decrease the number of parameters, use ensemble learning, or train the model with more data.

2. What is k-fold cross-validation? Why do we need it?

Cross-validation is a sampling procedure used to test the accuracy of a given machine learning model on a given dataset. The parameter k refers to how many groups the data is split into during this process - the number of times the cross-validation occurs. The procedure is as follows. First the dataset is randomly shuffled, then it is split into k groups. For each group, the current group is taken as the training dataset, and the remaining groups as testing. The model is fit on the training set and evaluated on the test set. The scores are kept and the model is discarded. At the end of this loop the model is summarized based on these evaluation scores. K-fold cross-validation is used to estimate the skill of and compare different machine learning models. K-folds are needed to provide robustness to the cross-validation.


3. Assume the following confusion matrix of a classifier. Please compute its precision, recall, and f1-score.

$precision = \frac{true\_positives}{true\_positives + false\_positives}$  
$precision = \frac{50}{50 + 40}$  
$precision = 0.556$

$recall = \frac{true\_positives}{true\_positives + false\_negatives}$  
$recall = \frac{50}{50 + 30}$  
$recall = 0.625$

$f1\_score = \frac{2 \cdot precision \cdot recall}{precision + recall}$  
$f1\_score = \frac{2 \cdot 0.556 \cdot 0.625}{0.556 + 0.625}$  
$f1\_score = 0.5885$
