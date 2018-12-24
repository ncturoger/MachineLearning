# Chapter 3
## Descending into ML
### Linear regression
`Linear regression` is a linear approach to modelling the relationship between a scalar response and one or more explanatory variables. Using the equation for a line, we could write down this relationship as follows:
![equation](https://latex.codecogs.com/gif.latex?y&space;=&space;mx&space;&plus;&space;b)

![Alt text](https://developers.google.com/machine-learning/crash-course/images/CricketLine.svg "Linear regression")


這個章節主要介紹ML中用來解決問題的最基本方法，線性回歸，透過線性的方法表示輸出與輸入參數之間的關係

---

### Training Loss
在訓練模型的時候，我們會需要用某些指標來表示模型的表現，loss就是一個用來表示預測輸出與實際答案差距的指標
- `Loss` is a number indicating how bad the model's prediction was on a single example

![Alt text](https://developers.google.com/machine-learning/crash-course/images/LossSideBySide.png "Training Loss")
- `Squared loss`: a popular loss function
![equation](https://latex.codecogs.com/gif.latex?(observation&space;-&space;prediction_{x})^{2})

- `Mean square error (MSE)` is the average squared loss per example over the whole dataset.
![equation](https://latex.codecogs.com/gif.latex?MSE&space;=&space;\frac{1}{N}&space;\sum_{x,y&space;\in&space;D}&space;(observation&space;-&space;prediction_{x})^{2})


