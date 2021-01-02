
# neural-network-mnist-ocr

Note that the concepts of a neural network is not explained in this Jupyter Notebook. For a better explanation, please go to [this](https://github.com/dandycheng/ml-simple-xnor-neural-network/) repository.

### The neural network has a configuration of:
- 784 input nodes
- 1 hidden layer (70 nodes)
- 10 output nodes

### Activation functions:
- Hidden layer 1 -> Sigmoid
- Output layer -> Softmax

### Hyperparameters
- Learning rate: a\[1e−5\]  to  1.5 
- Regularization:  3e−5 
- Batches:  10 
- Learning rate: 1 _(Constant learning rate)_

The learning rate of the neural network is manually tuned between epochs in order to prevent overfitting by observing the accuracy plot. As a result, the following shows the cost and gradient of the neural network.

![Network cost and gradient plot](https://raw.githubusercontent.com/dandycheng/ml-neural-network-mnist-ocr/main/imgs/Network%20cost%20and%20gradient%20plot.png)

After 11 epochs, we are able to obtain a training accuracy of 92.84 %, and a test accuracy of 92.72%. This result is relatively good as the model fits the data well, and does not overfit.

![Network accuracy plot](https://github.com/dandycheng/ml-neural-network-mnist-ocr/blob/main/imgs/Network%20accuracy%20plot.png?raw=true)

In the Jupyter Notebook, we fed a test image with the number 7.

![Test image](https://github.com/dandycheng/ml-neural-network-mnist-ocr/blob/main/imgs/Test%20image.png?raw=true)

With the Softmax as the activation function, we are able to predict the number 7, where ```P(7) ~ 0.92```.
The following shows the output layer values when the test image was fed:


```
Predicted number: 7
Actual number: 7
Output layer
[[0.00870439]
 [0.00528639]
 [0.00671943]
 [0.01977806]
 [0.00428522]
 [0.00609562]
 [0.00858216]
 [0.92023741]
 [0.00695449]
 [0.01335683]]
```
