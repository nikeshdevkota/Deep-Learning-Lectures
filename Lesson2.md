# Deep Learning
## Lesson 2

<h3>What is Image Classification?</h3>
Image classification is the process of categorizing and labeling groups of pixels or vectors within an image based on specific rules. For a computer, an image is represented as one large 3-dimensional array of numbers.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159401996-93d2762f-0070-4f89-8ff2-6ca4211d3575.PNG" width="350" title="hover text">
</p>

* In this example, the cat image is 248 pixels wide, 400 pixels tall, and has three color channels Red,Green,Blue.
* Therefore, the image consists of 248 x 400 x 3 numbers, or a total of 297,600 numbers.
* Each number is an integer that ranges from 0 (black) to 255 (white).
* The task of a machine learning algorithm is to turn this quarter of a million numbers into a single label, such as “cat”.

<h3>Challenges in image classification</h3>
Some of the challenges that that arise during image classification from a perspective of Computer Vision are as follows:
<br><br>

* <b>Viewpoint Variation</b>: An image can be viewed from many different perspective as the orientation of an object may differ with respect to the camera.
 <p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159404533-b1259464-5b3d-4b48-9599-13693ecac309.PNG" width="350" title="hover text">
</p>

* <b>Deformation</b>: The shape of an object may be deformed in many different ways.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159403955-a41873ef-62b1-408b-901f-5aed02dbcd3b.PNG" width="350" title="hover text">
</p>

* <b>Illumination</b>: The object may have variation in illumination conditions causing the pixels to change drastically.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159404300-537ea1c4-345d-4354-986b-87f025ada056.PNG" width="350" title="hover text">
</p>

* <b>Occlusion</b>: Sometimes the object may only be partially visible in the image.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159404884-bbdd249e-d303-451e-addc-e8c4d196a5a3.PNG" width="350" title="hover text">
</p>

* <b>Background Clutter</b>: The objects of interest may blend into their environment, making them hard to identify.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159404974-b0bf7284-79ab-4cc7-985c-31cec1763e03.PNG" width="220" title="hover text">
</p>

