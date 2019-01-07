# Chapter 12
### Regularization for Sparsity
進行模型訓練時，我們可能會使用`Feature crosses`來使模型更加貼近訓練資料，然而隨著模型變數的複雜化，過多的crossing feature也可能成為模型的噪音係數，因此我們可能會透過`正規化(regularization)`來減少這些噪音係數的數量

### L1 vs L2 regularization
最大的差別在於懲罰值的不同:
- L2 penalizes ![Alt text](https://latex.codecogs.com/gif.latex?weight^{2} "L2")

- L1 penalizes ![Alt text](https://latex.codecogs.com/gif.latex?\left&space;|&space;weight&space;\right&space;|)

從微分的結果來看
- The derivative of L2 is 2 * weight.
- The derivative of L1 is k (獨立於weight的常數)

由於L2正規化的懲罰值會隨著weight變動，只能得到趨近於零的結果，
L1正規化則獨立於weight，可能得到0
因此我們會選用**L1正規化**來減少噪音係數的數量



