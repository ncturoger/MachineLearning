# Chapter 11
## Classification
###Threshold
In order to map a logistic regression value to a binary category, you must define a `classification threshold` (also called the decision threshold)
對於邏輯回歸所輸出的機率，需要設定門檻值來決定輸出結果屬於哪個分類，這個門檻值稱為`分類門檻`

###Metrics
評估分類準確率的四大指標
![Alt text](confusion_matrix.PNG)

A true positive is an outcome where the model correctly predicts the positive class. Similarly, a true negative is an outcome where the model correctly predicts the negative class.

A false positive is an outcome where the model incorrectly predicts the positive class. And a false negative is an outcome where the model incorrectly predicts the negative class

True Positive：預測為Positive且預測準確True
True Negative：預測為Negative且預測準確True
Flase Positive：預測為Positive但預測錯False
Flase Negative：預測為Negative但預測錯False

###Accuracy
**Accuracy** is one metric for evaluating classification models.
<img src="https://latex.codecogs.com/gif.latex?Accuracy&space;=&space;\frac{Number\,&space;of\,&space;correct\,&space;predictions}{Total\,&space;number\,&space;of\,&space;predictions}" title="Accuracy = \frac{Number\, of\, correct\, predictions}{Total\, number\, of\, predictions}" />

For binary classification, accuracy can also be calculated in terms of positives and negatives as follows:
<img src="https://latex.codecogs.com/gif.latex?Accuracy&space;=&space;\frac{TP&plus;TN}{TP&plus;TN&plus;FP&plus;FN}" title="Accuracy = \frac{TP+TN}{TP+TN+FP+FN}" />

###Precision
Definition :
``
What proportion of positive identifications was actually correct?
``</br>
精確率的定義是所有被預測為Positive的情況有多少比例是正確判定的
<img src="https://latex.codecogs.com/gif.latex?Precision=&space;\frac{TP}{TP&plus;FP}" title="Precision= \frac{TP}{TP+FP}" />

###Recall
Definition :
``
What proportion of actual positives was identified correctly?
``</br>
召回率的定義是所有應該被判定為Positive的情況有多少比例是正確判定的
<img src="https://latex.codecogs.com/gif.latex?Recall=&space;\frac{TP}{TP&plus;FN}" title="Recall= \frac{TP}{TP+FN}" />

###ROC curve
An **ROC curve** (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds</br>
使用ROC圖可以用來表示分類模型在各個分類門檻下的表現
This curve plots two parameters:
- True Positive Rate
<img src="https://latex.codecogs.com/gif.latex?TPR=&space;\frac{TP}{TP&plus;FN}" title="TPR= \frac{TP}{TP+FN}" />

- False Positive Rate
<img src="https://latex.codecogs.com/gif.latex?FPR=&space;\frac{FP}{FP&plus;TN}" title="FPR= \frac{FP}{FP+TN}" />

![Alt text](https://developers.google.com/machine-learning/crash-course/images/ROCCurve.svg "ROC curve")
 
###Prediction Bias
一般情況下，預測結果平均值不應該和預期輸出的平均值相差太多
``
"average of predictions" should ≈ "average of observations"
``
<img src="https://latex.codecogs.com/gif.latex?Prediction\,Bias=&space;average\,of\,predictions&space;-&space;average\,of\,labels\,in\,data\,set" title="Prediction\,Bias= average\,of\,predictions - average\,of\,labels\,in\,data\,set" />








































