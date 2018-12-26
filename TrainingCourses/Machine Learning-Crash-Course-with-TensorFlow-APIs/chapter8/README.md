# Chapter 8
## Feature Crosses
`Feature Crossing`是一種透過將現有特徵互相組合，形成新的合成特徵的方法，主要運用於下列兩種情境:
1. Encoding Nonlinearity
當我們面對無法使用線性模型解決的問題時，我們可以利用`Feature Crossing`來表示非線性的關係
如下圖，我們無法以線性模型
![equation](https://latex.codecogs.com/gif.latex?y&space;=&space;b&space;&plus;&space;w_{1}x_{1}&plus;w_{2}x_{2})
來區分橘點與藍點
![Alt text](https://developers.google.com/machine-learning/crash-course/images/LinearProblem2.png "Feature Crosses")

因此我們利用`Feature Crossing`將x1與x2合成一個新的特徵x3
![equation](https://latex.codecogs.com/gif.latex?x_{3}&space;=&space;x_{1}x_{2})

此時我們即可以新的模型方程式來找出橘點與藍點間的關係
![equation](https://latex.codecogs.com/gif.latex?y&space;=&space;b&space;&plus;&space;w_{1}x_{1}&space;&plus;&space;w_{2}x_{2}&space;&plus;&space;w_{3}x_{3})

2. Crossing One-Hot Vectors
機器學習的實驗中，很少會組合連續特徵。不過卻會經常組合由`One-Hot encoding`所產生的特徵向量，將特徵組合視為特定條件的新特徵值來進行訓練
如經緯度的特徵向量分別為:
```
binned_latitude = [0, 0, 0, 1, 0]
binned_longitude = [0, 1, 0, 0, 0]
```

則我們可以透過合成
binned_latitude X binned_longitude

來獲得經緯度之間的關聯特徵
```
binned_latitude_X_longitude(lat, lon) = [
  0  < lat <= 10 AND 0  < lon <= 15
  0  < lat <= 10 AND 15 < lon <= 30
  10 < lat <= 20 AND 0  < lon <= 15
  10 < lat <= 20 AND 15 < lon <= 30
  20 < lat <= 30 AND 0  < lon <= 15
  20 < lat <= 30 AND 15 < lon <= 30
]
```
















