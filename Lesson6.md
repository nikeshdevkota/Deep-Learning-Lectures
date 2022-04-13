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


  
  
