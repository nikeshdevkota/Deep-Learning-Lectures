# Deep Learning
## Lesson 10

<h3>RNN</h3>
A recurrent neural network (RNN) is a special type of an artificial neural network adapted to work for time series data or data that involves sequences.Examples of RNN 
application include Image Captioning, Language Translation etc.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/169200626-77bf6b9e-4f5f-4af6-994c-5a5ecf6cbba4.PNG" width="650" title="CNN">
</p>

<h3>Types of RNN</h3>

* <strong>One to Many</strong>
    *  A single input can produce multiple outputs.
    *  Example: Image Captioning
    
* <strong>Many to One</strong>
  *   Multiple outputs can produce a single output.
  *   Example: Sentiment Classification 
 
* <strong>Many to Many</strong>
  * Multiple inputs produce multiple outputs
  * Example: Machine Translation
  
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/169202328-170a08de-411f-46a6-8cd1-cc61fd129ec4.PNG" width="750" title="CNN">
</p>

 RNNs are referred to as recurrent because they do the same task for each element of a sequence, with the outcome relying on past calculations. RNN consist of 
 * <strong>Input State</strong>: At time step t, x(t) is used as the network's input. 
 * <strong>Hidden State</strong>: At time t, h(t) represents a hidden state and serves as the network's "memory." h(t) is calculated using the current input and the hidden state from the previous time step.
 <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/169201713-f7f9a9cd-1420-4c21-bad4-7a34d3ff4f9e.PNG" width="550" title="CNN">
</p>

 * <strong>Weights</strong>: Weights are matrices that are multiplied with the inputs and the hidden state.
 * <strong>Output</strong>: It refers to the output y(t) of the network. 

 <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/169201925-ad1ea765-ba94-4e0c-9406-283de3e65f40.PNG" width="550" title="CNN">
</p>

<h3>LSTM</h3>

The back propagation through time in vanilla RNN network suffers from exploding gradient and vanishing gradient. Since the gradient vanishes, RNN may leave out important information from beginning thus having a short term memory.

To solve the problem of vanishing gradient, we can use LSTM network.

 <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/169217616-5b293d5b-b1d5-4430-a1d0-993bd2b74741.PNG" width="550" title="CNN">
</p>

The LSTM network has internal mechanism called gates that can regulate the flow of information. These gates can learn which data in a sequence is important to keep or throw away to make predictions.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/169218859-586aac64-ef01-471d-89a5-ac847a8b147f.PNG" width="650" title="CNN">
</p>


