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
