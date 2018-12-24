# Chapter 4
## Reducing Loss
模型訓練的過程，就是不斷的透過計算誤差，改善參數的迴圈來找出最佳的模型

![Alt text](https://developers.google.com/machine-learning/crash-course/images/GradientDescentDiagram.svg "Reducing Loss")

---

## Gradient descent
其中，梯度下降法就是一個用來降低loss的常用方法，利用該點的斜率進行loss的修正，用learning rate來決定修正的幅度，直到找到loss曲線的最低點

![Alt text](https://developers.google.com/machine-learning/crash-course/images/GradientDescentGradientStep.svg " Gradient descent")

- `Learning rate`: Gradient descent algorithms multiply the gradient by a scalar known as the learning rate


