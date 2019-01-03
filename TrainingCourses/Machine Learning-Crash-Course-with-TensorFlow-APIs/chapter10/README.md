# Chapter 10
## Logistic Regression
邏輯回歸是一種監督式學習方法，主要用於對樣本進行分類
線性回歸的輸出一般是連續的，而邏輯回歸的輸出會是介於0~1之間的機率

###Sigmoid function
透過`sigmoid function`，我們可以將回歸輸出轉化成0~1之間的機率</br>
![equation](https://latex.codecogs.com/gif.latex?y=\frac{1}{1&plus;^{e^{(-z)}}})</br>

y代表輸出的機率
z代表模型的函式，通常以![equation](https://latex.codecogs.com/gif.latex?w_{1}x_{1}&space;&plus;&space;w_{2}x_{2}&space;&plus;&space;...&space;w_{N}x_{N})的形式表示

![Alt text](https://developers.google.com/machine-learning/crash-course/images/SigmoidFunction.png "sigmoid")

###Loss function for Logistic Regression
線性回歸所使用的loss function為squared loss
邏輯回歸則是使用**Log Loss**來評估模型的表現
![equation](https://latex.codecogs.com/gif.latex?LogLoss&space;=&space;\sum_{(x,y)\in&space;D}-ylog(y^{'})-(1-y)log(1-y^{'}))


































