# Chapter 14
## Embedding
對於非數值型的資料，通常會以one-hot encoding的方式進行處理
![Alt text](https://developers.google.com/machine-learning/crash-course/images/InputRepresentationWithValues.png "Categorical data")
然而One-hot encoding具有以下問題:
1. 每個向量之間都是獨立的，無法表示data之間的關聯性
2. N種data就會需要用N維的Vector來表示，使得feature運算量過於複雜

這時我們就可以透過`Embedding`來表示data的特性
![Alt text](https://developers.google.com/machine-learning/crash-course/images/linear-relationships.svg "Embedding")
Embedding中的每個Dimension都有意義，距離越近的data表示關聯性越大
同時也將N種類的data向量**降維**成K個Dimension的變量，降低運算量



