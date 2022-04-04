# Deep Learning
## Lesson 5

<h3>Introduction to Convolution Neural Networks</h3>
Convolution Neural Networks are specific architecture of Neural Networks that are highly effective at dealing with image data.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/161522174-e07a64ee-a8e0-40ac-b55f-138fed995faa.png" width="750" title="CNN">
</p>

<h3>Different Layers in Convolution Neural Network?</h3>

* <strong>Input layer:</strong> The input layer contains the image dat given as input to the Convolution Neural Network. The size of an image is a 3D matrix.

* <strong>Convolution layers:</strong> 
 Convolution layers are created in neural networks when multiple image filters are applied to the input image. The multiplication between an input image and an image kernel is a dot product. Basically, a convolution layer transforms the input image data and extract features from it.

* <strong>Activation Functions:</strong> 
 The activation function is the final component of the convolutional layer, and it increases the output non-linearity. In a convolution layer, the ReLu or Tanh function is commonly employed as an activation function.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/161530143-b053691b-2415-4c3c-aa59-671a29c3f01b.png" width="750" title="CNN">
</p>

* <strong>Image Kernels:</strong>
[Image Kernels ](https://setosa.io/ev/image-kernels/) are small matrices used to apply effects such as blurring or sharpening images. In machine learning, they are used for the feature extraction process to determine the important portions of an image. An image kernel size is samller than the input image.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/161528554-92ebf242-985a-43dd-ae02-81eef2109bf7.png" width="550" title="CNN">
</p>

* <strong>Pooling layers:</strong>
The pooling layer reduces the spatial size of the image representation to reduce the number of parameters and computation in the network. It operates on each feature map separately.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/161532169-353d6913-ffd9-468f-9c83-77990ac07b53.jpeg" width="550" title="CNN">
</p>
* <strong>Fully Connected layer:</strong>
A convolutional neural network's final layer is a fully linked layer. This layer recognizes and categorizes the image objects.

<h3>What are strides in CNN?</h3>
Stride is a filter parameter in a neural network that controls the amount of movement in an image or video. When the stride of a neural network is set to 1, for example, the filter moves one pixel (or unit) at a time.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/161536313-12e49c9d-cf9a-4eef-b025-bc4444ad5b8b.png" width="550" title="CNN">
</p>

<h3>How to determine the size of a feature map?</h3>
If an input image has a size of n x n and filters size f x f and p is the Padding amount and s is the Stride, then the dimension of the feature map is given by:
<p align="center"> Dimension = floor[ ((n-f+2p)/s)+1] x floor[ ((n-f+2p)/s)+1]</p>
