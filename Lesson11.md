# Deep Learning
## Lesson 10
## Detection and Segmentation

<h3>Semantic Segmentation</h3>
Input an image and label each pixel in the image with a category label.


<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170239187-3ba99170-924d-4c0d-8dd3-4564e84148c6.PNG" width="650" title="CNN">
</p>

<h3>Semantic Segmentation Design</h3>
Design network as a bunch of convolutional layers with downsampling and upsampling inside the network.Downsampling and Upsampling allows the network to work at lower resolution for many of the layers inside the network.
<br> <br>

* <strong>Downsampling</strong>: Reducing the size of the image by using average pooling, max pooling etc.
* <strong>Upsampling</strong>: Increase the spatial resolution of our predictions in the second half of the network so that the output image is the same size as the input image.

Some of the upsampling texhniques are max-unpooling, Bed of Nails, Nearest Neighbour unpooling etc. 

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170240143-ceb0c2fb-6f2f-45d3-9b65-90c154617144.PNG" width="650" title="CNN">
</p>

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170240528-83b91a6c-52f4-480a-bfb2-81bcd6cce8cd.PNG" width="650" title="CNN">
</p>

All of the above techniques are fixed functions and are not learning how to do the upsampling. Transpose Convolutions, however can perform learnable upsampling.

<h3>Transpose Convolutions</h3>

* Normal 3 x 3 convolution, stride 2 pad 1
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170242300-3e829c4f-ecb9-47a3-9f3e-9bfb664785c0.PNG" width="650" title="CNN">
</p>

