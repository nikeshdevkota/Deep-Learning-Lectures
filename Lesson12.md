# Deep Learning
## Lesson 12
## Visualizing and Understanding Deep Neural Networks

<h3>Visualization technique</h3>
Large Convolutional Network models have recently demonstrated impressive classification performance on the ImageNet benchmark. With visualization technique, 
we can determine what each layer in the network is learning and from that we can gain some insights to improve performance. 

<h3>First Layer Filters</h3>
In Alexnet, the first convolutional layer consists of filters, each convolutional filter has shape 3 * 11 * 11 and there are 64 number of filters. These convolutional layers
get slid over the input image. Then, we take the inner products between some chunk of input image and weights of the convolutional filter and that gives us our output after the 
first convolutional layer.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170627446-7fd38e1c-57a4-42b5-9304-5bb64bab686f.PNG" width="450" title="CNN">
</p>

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170627573-2ef18834-43a9-486e-9b49-6e02b0a08891.PNG" width="450" title="CNN">
</p>

