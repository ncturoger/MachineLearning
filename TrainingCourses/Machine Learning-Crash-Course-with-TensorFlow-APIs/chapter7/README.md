# Chapter 7
## Representation
### Feature Engineering
`Feature engineering` means transforming raw data into a feature vector. Expect to spend significant time doing feature engineering.</br>
從資料中提取數據、建立特徵向量的過程，稱為特徵工程
![Alt text](https://developers.google.com/machine-learning/crash-course/images/OneHotEncoding.svg "Feature Engineering")

面對非數值型的資料，會使用one-hot encoding來處理
![Alt text](https://cdn-images-1.medium.com/max/1000/1*MWciJw4Kwx_kaBSl0AbsRQ.png "one-hot encoding")

---
### Qualities of Good Features
- Avoid rarely used discrete feature values
- Prefer clear and obvious meanings
- Don't mix "magic" values with actual data
- Account for upstream instability

作為一個好的特徵數據，須具備以下特質:
1. 避免使用出現次數過於稀少的離散資料，例如ID、 型號等等
2. 特徵數據要有明確的意義，且數值盡可能方便排錯與維護
3. 避免使用魔法數字等意義不明的數值作為特徵數據
4. 特徵值不應該隨著時間變化

---
### Cleaning Data
面對品質較差、分布較為離散的原始數據，我們可以利用`Data Cleaning`的方式來改善其特徵，常見的方法有:
1. Scaling feature values
Scaling means converting floating-point feature values from their natural range (for example, 100 to 900) into a standard range</br>
對特徵的數值進行比例縮放至特定的範圍:
- Helps gradient descent converge more quickly.</br>
可以幫助梯度下降法收斂得夠加快速
- Helps avoid the `NaN trap`, in which one number in the model becomes a NaN</br>
避免空值造成訓練出錯誤的模型
- Helps the model learn appropriate weights for each feature. Without feature scaling, the model will pay too much attention to the features having a wider range.</br>
透過比例調整，我們能夠讓數據集中在特定的範圍，避免模型權重過度仰賴某些數值較大的特徵

For example, we can use Z-score for scaling:
![equation](https://latex.codecogs.com/gif.latex?scalevalue&space;=&space;(value&space;-&space;mean)&space;/&space;stddev)


2. Handling extreme outliers
For the extreme outliers, we can reduce the amount of them with `Logarithmic` or `Clipping`</br>
我們可以透過指數、資料修剪來去除極端值

![Alt text](https://developers.google.com/machine-learning/crash-course/images/ScalingLogNormalization.svg "Logarithmic")

![Alt text](https://developers.google.com/machine-learning/crash-course/images/ScalingClipping.svg "Clipping")

3. Binning
In the data set, latitude is a floating-point value. However, it doesn't make sense to represent latitude as a floating-point feature in our model. That's because no linear relationship exists between latitude and housing values.</br>
對於離散型的數據，線性模型所產生的連續關係是沒有意義的，因此我們可以使用Binning來對這些數據進行分桶處理，將數值區間轉化為一個種類特徵，降低模型產生的連續關係
![Alt text](https://developers.google.com/machine-learning/crash-course/images/ScalingBinningPart2.svg "Binning")

例如: 37.4可能標示如下
```
[0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0]
```





