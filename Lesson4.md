# Deep Learning
## Lesson 4

<h3>Introduction to Neural Networks</h3>
Artificial Neural networks are a network of artificial neurons(perceptrons) which mimick the human brain neural networks to produce a meaningful output. Neural networks consist of the input layer, hidden layer and the output layer. The input layer accepts the input 

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160355531-d1b2d967-6f4e-4753-a64e-067827f1c9ce.PNG" width="550" title="hover text">
</p>

The neural network relies on a training dataset to predict an outcome based upon the input and hidden layer. Each feature or input in the neural network layer has a weight attached to it.

<h3>Forward Propagation & Backpropagation in  Neural Networks</h3>

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160356685-444c6024-5a38-4c94-bf3b-51655768b622.PNG" width="550" title="hover text">
</p>

Forward Propagation refers to the computational movement from input layers toward the output layer and back propagation refres to the computational movement from the output layer to the the input layers.

<h3>Why do we need Backpropagation in  Neural Networks</h3>

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160366819-3841d88a-e2aa-43b3-92d1-df1263ef4fdb.PNG" width="550" title="hover text">
</p>

In a neural network, the predicted output depends upon:

* Input Values
* Activation Function
* Beta Coefficients of the inputs(weights associated with inputs)
* Optimizers(Biased Terms)

Backpropagation in neural networks is a suitable method used to reduce the loss function and hence improve the prediction accuracy. In backward propagation, we compute the gradient of the loss function with respect to the inputs to adjust the weights to minimize the loss function.




