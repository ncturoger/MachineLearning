# Chapter 6
## Generalization
訓練模型時，模型可能會因為要盡量fit training data中的每一個數據進而發展成一個只符合training data的模型，導致當新的data加入時，還是產生錯誤的預測結果，稱為**過度擬合(overfitting)**

---
## Splitting Data
The previous module introduced the idea of dividing your data set into two subsets:
- training set—a subset to train a model.
- test set—a subset to test the trained model.
- **Never train on test data**.

![Alt text](https://developers.google.com/machine-learning/crash-course/images/PartitionTwoSets.svg "Splitting Data")


- workflow with two partitions **(may overfitting)**
![Alt text](https://developers.google.com/machine-learning/crash-course/images/WorkflowWithTestSet.svg "workflow with two partitions")

To avoid overfitting, we use the `validation set` to evaluate results from the `training set`. Then, use the `test set` to double-check your evaluation after the model has "passed" the validation set.
為了避免過度擬合現象的發生，我們將資料分為`訓練`、`測試`與`驗證`三種資料集
在訓練的過程中，驗證資料集可以做為第一層防線，用來驗證模型是否有過度擬合訓練資料，接著再使用測試資料集對通過第一層驗證的模型做第二次check
![Alt text](https://developers.google.com/machine-learning/crash-course/images/WorkflowWithValidationSet.svg "workflow with three partitions")






