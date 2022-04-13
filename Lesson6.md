# Deep Learning
## Lesson 6


<h3>What are Activation Functions in a neural network?</h3>
Activation functions are used to determine(or activate) the output of neural network depending upon the input values. This function decides whether a neuron should be activated or not.

<h3>Types of Activation Function<h3>
  
* <strong>Sigmoid Activation Function:</strong>
  The ouput value ranges from 0 to 1. The function can be used to predict the probability however it is usually not used in recent times as it suffers from vanishing     gradient problem. 
   
  <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163190412-bc118475-2107-43c6-9cb3-7a0534a31693.PNG" width="750" title="CNN">
</p>

* <strong>Hyperbolic tangent Activation Function:</strong>
The hyperbolic tangent performs a little bit better than the sigmoid function. The output of the hyperbolic tangent lies between -1 to 1. However, this function also suffers from vanishing gradient problem.
  
   <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163191593-ff8826d7-1b04-4ce4-abb6-d5fdd284c41e.PNG" width="450" title="CNN">
</p>

* <strong>ReLU Activation Function:</strong>
The Rectified Linear Unit(ReLU) is one of the most commonly used activation function in present day for deep neural network modeling as it doesn't suffer from the vanishing gradient problem and is computationally efficient.The neurons will only be deactivated if the output is less than 0. 
  
   <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163192821-3924ad6e-e6fa-4ab3-8d64-f144a7ad36ce.PNG" width="450" title="CNN">
</p>

  * <strong>Leaky ReLU Activation Function:</strong>
The Leaky Rectified Linear Unit, or Leaky ReLU, is an activation function based on the ReLU, but instead of a flat slope it has a tiny slope for negative values. Before beginning training, the slope coefficient is calculated.

  <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163195252-09e6162d-8d2a-4ff4-ad64-d36e5d11315c.png" width="450" title="CNN">
</p>
  
 <h3>What is Data Processing?<h3>
 The task of changing the current data to a much more useable and desired form, i.e. making it more relevant and instructive, is known as data processing.
   
  <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163196579-2749f171-2345-4e77-b49c-5fcde3a39e52.PNG" width="750" title="CNN">
</p>

  <h3>What happens when all weights are initialized to zero?<h3>
    
 When all the weights are initialized to zero, all neurons are updated the same way and the network doesn't get trained very well. Small random number works for smaller neural networksbut are a problem for deep neural networks. 
    
<h3>Weight Initialization Strategies<h3>
* Use Uniform distribution
* Use Normal Distribution
* Use Xavier Normal Distribution
* Use Xavier Uniform Distribution
However, proper initialization is still a research topic. You can look into the topics shown in the picture below for delving deep into weight initialization.
  
 <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163199462-e36e1f36-d584-42ef-84fe-ffd26524e1af.PNG" width="750" title="CNN">
</p>

<h3>What is batch normalization?<h3>
 Normalization is a data pre-processing tool used to bring the numerical data to a common scale without distorting its shape. Batch normalization is a technique to make the neural network modeling faster and more stable through normalization of the layers' inputs by re-centering and re-scaling. In it, the values of activation functions are normalized with respect to a certain batch of inputs.
     
<h3>Advantages of Batch Normalization?<h3>
 * Improves gradient flow of network
 * Allows the use of higher learning rates
  
  
    
  
