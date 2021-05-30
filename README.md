# Custom Neural Networks
* Create a customized Feedforward Neural Network by changing the number of layers, activation functions, loss function and optimizer.
* Refer to the documentation of any class/method by using help(class/method)
* Please refer to this [repo](https://github.com/Taarak9/Neural-Networks) for more information.

## Installation
```bash
$ [sudo] pip3 install custom-neuralnet
``` 
## Usage

```python3
>>> from custom-neuralnet import FNN
```
### Creating a Feedforward Neural Network
```python3
# number of input nodes
n_inputs = 27
loss_fn = "ce"
nn = FNN(n_inputs, loss_fn)

# Add a layer with 9 nodes and activation function ReLU
nn.add_layer(9, "relu")
# Add a layer with 3 nodes and activation function sigmoid
nn.add_layer(3, "sigmoid")

# Note the last layer you added will be the output layer of the NN
# Compile the nn
nn.compile(training_data, epochs, mini_batch_size, eta, gamma=None, optimizer="GD", mode="batch", shuffle=True, test_data, task="classification")
```
