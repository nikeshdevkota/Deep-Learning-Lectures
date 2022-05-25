# Deep Learning
## Lesson 11
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

* 3 x 3 Transpose convolution, stride 2 pad 1

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170243073-771555fd-165d-4abd-b62c-4ff7d21cfd81.PNG" width="650" title="CNN">
</p>

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170244872-a6a501fa-fe96-462f-9d02-37dfff88c3e6.PNG" width="650" title="CNN">
</p>

<h3>Classification and Localization</h3>

* <strong>Localization</strong> : Find where the object is and draw a bounding box around it.<br><br>
Sometimes, we want to do more than classify objects in an image. We may want to know where the object is and so on. For e.g in the below image, we may also want to know where the cat is along with identifying <strong>"the cat"</strong> as a cat. 

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170246141-092ace4a-17f8-4e30-a395-99997ee02d6b.PNG" width="350" title="CNN">
</p>

In Classification and Localization problem, we have two losses i.e softmax loss for clasification. Another loss is the regression loss for localization since the bounding box cordinates may not be same as the actual box cordinates.

<h3>Object Detection</h3>
Object Detection combines the concepts of image localization and classification. Given an image, an object detection algorithm would return bounding boxes around all objects of interest and assign a class to them.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170248330-a2ac40c6-6362-450c-8139-934715e0e6a0.PNG" width="350" title="CNN">
</p>

<h3>Region Proposals in Object Detection</h3>
* Find “blobby” image regions that are likely to contain objects
* Relatively fast to run; e.g. Selective Search gives 1000 region proposals in a few seconds on CPU
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170249492-dc9701f0-cd74-40ae-a679-6255234533ce.PNG" width="350" title="CNN">
</p>
