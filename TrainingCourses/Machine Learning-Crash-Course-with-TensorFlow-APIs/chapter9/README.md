# Chapter 9
## Regularization
![Alt text](https://developers.google.com/machine-learning/crash-course/images/RegularizationTwoLossFunctions.svg "overfitting")
If a model in which training loss gradually decreases, but validation loss eventually goes up, this generalization curve shows that the model is `overfitting` to the data in the training set. 
We can prevent overfitting by **penalizing** complex models, which is called `regularization`.</br>
模型訓練的過程中，若發生當training loss不斷的下降，validation loss卻開始上升的現象，就代表模型已經過度擬合了
這種情況通常是因為模型隨著訓練的過程，為了符合訓練資料而使結構變得越來越複雜所致，因此，要避免過度擬合的現象發生，我們會使用`正規化`來處罰結構複雜的模型

Minimize(Loss(Data|Model) + **Complexity(Model)**

常見的正規化方法有:
1. L1 regularization
2. L2 regularization
![Alt text](https://morvanzhou.github.io/static/results/ML-intro/L1l2regularization3.png "regularization")

由於加入了正規化的計算，多了一個稱為`lamda`的參數來調整懲罰的強度
![equation](https://latex.codecogs.com/gif.latex?Minimize\left&space;[&space;Loss\left&space;(&space;Data|Model\right&space;)&space;\right&plus;\lambda&space;Complexity\left&space;(&space;Model&space;\right&space;)&space;])
1. 當lamda過大時，模型結構可能會過於簡單，使得學習過程無法收斂而產生**underfitting**

2. 反之，當lamda過小時，處罰機制就變得沒有意義，使得模型結構過於複雜，產生**overfitting**




























