# Chapter 13
## Neural Networks
面對非線性問題時，我們可能會透過`Feature crosses`的方式來解決問題
![Alt text](https://developers.google.com/machine-learning/crash-course/images/NonLinearSpiral.png "Nonlinear classification problem")
然而，面對更複雜的非線性問題時，我們無法透過`Feature crosses`的方式合成出足以解決問題的模型
這時候，就可以使用`Neural Networks`幫助我們找到模型可能的結構

### Structure
![Alt text](https://developers.google.com/machine-learning/crash-course/images/2hidden.svg "Structure")

- Input Layer
- Hidden Layers
- Output Layer
- Activation Functions
透過Activation Functions可將線性函數轉為非線性的模型，用來模擬神經元被觸發時所產生的變量
常用的函數有:
1. ReLU
![Alt text](https://developers.google.com/machine-learning/crash-course/images/relu.svg "ReLU")

2. Sigmoid
![Alt text](https://developers.google.com/machine-learning/crash-course/images/sigmoid.svg "Sigmoid")

### Characteristic
類神經網路具有以下特性:</br>
- A set of nodes, analogous to neurons, organized in layers.</br>
具有一組類似神經元的節點</br>
- A set of weights representing the connections between each neural network layer and the layer beneath it. The layer beneath may be another neural network layer, or some other kind of layer.</br>
節點間有一組權重互相連接</br>
- A set of biases, one for each node.</br>
每個節點都有一個bias值</br>
- An activation function that transforms the output of each node in a layer. Different layers may have different activation functions.</br>
會透過activation function將線性模型轉為非線性的關係</br>

## Failure Cases

- Vanishing Gradients
神經網絡權重的更新值與誤差函數梯度成比例，然而在某些情況下，梯度值會幾乎消失，使得權重無法得到有效更新，甚至神經網絡可能完全無法繼續訓練</br>
使用`ReLU activation function` 可以有效避免這個問題的發生

- Exploding Gradients
當類神經模型結構變得複雜，會使得整體模型變得不穩定，誤差梯度可在更新中累積，變成非常大的梯度，導致網絡權重的大幅更新，使得權重的值變得異常大
透過`批次標準化(batch normalization)`或是設定降低learning rate`可避免這個問題

- Dead ReLU Units
使用ReLU時，只要它加權總合的input小於0，它就很難再加到大於0，也就不會再對這個Neural Network有貢獻。
`降低learning rate`可以防止ReLU dying

## Dropout
Dropout是針對Neural Network有用的一種Regularization，透過隨機捨去一些unit避免模型產生過度擬合的情況

Dropout值表示丟掉units的比例
- 0.0 = 不執行Dropout Regularization
- 1.0 = 100%units通通丟掉，model學不到任何東西
- 0~1之間會比較常用














