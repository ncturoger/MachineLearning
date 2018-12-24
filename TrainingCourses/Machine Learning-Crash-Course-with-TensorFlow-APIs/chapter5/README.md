# Chapter 5
## First Steps with TensorFlow
Tensorflow is a computational framework for building machine learning models. TensorFlow provides a variety of different toolkits that allow you to construct models at your preferred level of abstraction.
TF是一個用於機器學習的計算框架，提供了許多圖表的計算功能，透過上層所提供的API，我們可以簡化建置NN的過程

![Alt text](https://developers.google.com/machine-learning/crash-course/images/TFHierarchy.svg "TensorFlow")


```python
import tensorflow as tf

# Set up a linear classifier.
classifier = tf.estimator.LinearClassifier(feature_columns)

# Train the model on some example data.
classifier.train(input_fn=train_input_fn, steps=2000)

# Use it to predict.
predictions = classifier.predict(input_fn=predict_input_fn)
```



