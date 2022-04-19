# Deep Learning
## Lesson 7


<h3>What happens when loss changes quickly in one direction and slowly in another direction</h3>

There is very little progress in the gradient descent in the shallow direction and jitter along the steep direction.

 <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163305143-711a74d0-e38f-4612-9718-edd569154cf4.PNG" width="750" title="CNN">
</p>

<h3>Disadvantages of SGD</h3>

* <h3>Noisy Derivatives</h3>
  We don’t compute the precise derivate of loss function in Stochastic Gradient Descent, instead, we’re estimate it on a small batch. So, we’re not always going in the
  optimal direction, because our derivatives are ‘noisy’.
* <h3>Local Minima Problem</h3>
  The gradient descent gets stuck.In the picture below, the first loss curve has a local minima and the gradient descent gets stuck at that dip.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163306003-e86424f5-87e5-42db-99c2-d20a82c62820.PNG" width="450" title="CNN">
</p>

* <h3>Saddle Point Problem</h3>

  In mathematics, a **saddle point** or minimax point is a point on the surface of the graph of a function where the slopes (derivatives) 
  in orthogonal directions are all zero (a critical point), but which is not a local extremum of the function. Hence, the gradient gets stuck at the saddle point.
  Saddle points are very common in the higher dimension compared to the local minima.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163306547-08155d92-1f9d-4db8-89df-30361e0ca57d.PNG" width="350" title="CNN">
</p>

<h3>What are optimizers?</h3>
 Optimizers help to reduce the loss function by changing the weights and the learning rate attributes. SGD, Adagrad,RMSProp,Adadelta,Adam etc are types of optimizers found in deep learning.

<h3>SGD with momentum</h3>

By adding a momentum term in the gradient descent, gradients accumulated from past iterations will push
the cost further to move around a saddle point even when the current gradient is negligible or zero. This removes the saddle problem.
Also, adding exponentially weighed averages can provide a better estimate closer to the actual derivate than the noisy calculations.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163311157-45cead0a-6ffa-4c78-aacd-da0a192ac03e.PNG" width="850" title="CNN">
</p>

<h3>AdaGrad Optimizer</h3>

The learning rate is different for each weight parameter in the AdaGrad Optimizer. The frequency of the parameter determines the learning rate i.e higher the frequency of occurence, lower is the learning rate and vice versa.It divides the learning rate by the sum of squares of all previous gradients of the parameter.

When the network gets larger and larger, there is insignificant change in the new learning rates, and the new weight parameter is almost similar to the old weight parameter and the neural network is unable to learn any further. AdaDelta and RMSProp solve this problem.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/163983658-e110352d-d2e7-4a15-9318-e546fc078a86.PNG" width="850" title="CNN">
</p>

<h3>RMSProp</h3>

RMSProp uses  learning rate to update the weight parameters in a neural network. In this technique, the recent moving averages are given more significance in order to prevent the new learning rates from being constant.

<h3>Adam Optimizer</h3>
The adaptive moment adaptation optimization is a stochastic gradient descent approach that uses adaptive first-order and second-order moment estimation.
