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

<h3>Challenges in Image Classification</h3>
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

<h3>Data Driven Aprroach</h3>
So to fix the above problems, we’re going to provide the computer with many examples of each class and then develop learning algorithms that look at these examples and learn about the visual appearance of each class.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159405930-63926b0a-8c7b-48eb-952c-817ff33272bd.PNG" width="420" title="hover text">
</p>

<h3>Nearest Neighbor Classifier</h3>
Nearest Neighbor Classifier is a simple machine learning approach which allows us to get an idea about the basic approach to an image classification problem.The nearest neighbor classifier will take a test image, compare it to every single one of the training images, and predict the label of the closest training image.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159406948-b2cec82f-f85e-46c0-9801-3d33685209d9.PNG" width="420" title="hover text">
</p>

<h3>K-Nearest Neighbor Classifier</h3>
Instead of finding the single closest image in the training set, we will find the top k closest images, and have them vote on the label of the test image. In particular, when k = 1, we recover the Nearest Neighbor classifier.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159407429-ed8f11fe-602f-441f-9519-d5180d38c5ae.PNG" width="650" title="hover text">
</p>

<h3>Validation sets for Hyperparameter Tuning</h3>
In the K-Nearest Neighbor Classifier, we have to choose the best value of k. But how do we do that? One way is to use hit and trail method for many values of k and see what value fits best. Since the test data should only be used near the end, we should use a validation dataset to find out the best hyperparameters for the machine learning model.The validation data can be obtained by reducing the training dataset size inton a smaller one and using the remaining as validation dataset.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159408646-16393f17-aecd-474a-ba83-9370aaefdfcf.PNG" width="650" title="hover text">
</p>

<h3> Cross Validation</h3>
In cases where the size of your training data (and therefore also the validation data) might be small, people sometimes use a more sophisticated technique for hyperparameter tuning called cross-validation.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/159408994-5cf983d5-cc3d-4d37-aa5b-76bc9554cd4e.PNG" width="450" title="hover text">
</p>



