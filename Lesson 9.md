# Deep Learning
## Lesson 9

<h3>AlexNet</h3>
AlexNet is considered one of the most influential papers published in computer vision, having spurred many more papers published employing CNNs and GPUs to accelerate 
deep learning. As of 2021, the AlexNet paper has been cited over 80,000 times according to Google Scholar.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167339848-01deb8a0-5435-4a82-9e0b-70a52038f938.PNG" width="550" title="CNN">
</p>
AlexNet is the name of a convolutional neural network (CNN) architecture,designed by Alex Krizhevsky in collaboration with Ilya Sutskever and Geoffrey Hinton, who 
was Krizhevsky's Ph.D. advisor.
<br><br>
AlexNet competed in the ImageNet Large Scale Visual Recognition Challenge on September 30, 2012.The network achieved a top-5 error of 15.3%,
more than 10.8 percentage points lower than that of the runner up. It was the first large scale CNN network that was able to do well on the ImageNet classification task.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167337663-17fe564c-49cf-4aae-80c9-38833a421940.PNG" width="550" title="CNN">
</p>

AlexNet contained five convolutional layers, 3 Max-Pool layers, 2 Normalizing layers and 2 fully connected layers before the final fully connected layer going to the output classes.

* <strong>First Layer(CONV1):</strong> Input image of size (227,227,3). The 96 filters of size (11,11) are applied at stride 4 to the input images. The output volume of this layer is (55,55,96).
* <strong>Second Layer(POOL1):</strong> It takes the output of the first convolution layer as its input. The filter of size (3,3) is applied to the input at stride 2. The output volume is (27,27,96)

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167339268-8c1d7184-18db-4cce-a83a-bfa5d98771cd.PNG" width="450"  title="CNN">
</p>

<h3>VGGNet</h3>
VGGNet is a Convolutional Neural Network architecture proposed by Karen Simonyan and Andrew Zisserman from the University of Oxford in 2014. It used smaller filters and deeper networks compared to the AlexNet model.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167340808-60d9c36b-5268-4ae2-93dd-573c91dfe2b1.PNG" width="450"  title="CNN">
</p>
<h3>Why use smaller filters?</h3>
Stack of three 3x3 conv (stride 1) layers has same effective receptive field as one 7x7 conv layer but has deeper and more non linearities and fewer parameters.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167345962-33589b66-fb8b-47cc-874a-0002b14694e7.PNG" width="450"  title="CNN">
</p>
The receptive field in Convolutional Neural Networks (CNN) is the region of the input space that affects a particular unit of the network. Unlike in fully connected networks, where the value of each unit depends on the entire input to the network, a unit in convolutional networks only depends on a region of the input.This region in the input is the receptive field for that unit.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167342233-feeaa083-aca9-4ef6-941c-e1fa43e8437d.PNG" width="550"  title="CNN">
</p>
<h3>GoogleNet</h3>
GoogLeNet is a 22-layer deep convolutional neural network that was presented in the ImageNet Large-Scale Visual Recognition Challenge 2014(ILSVRC14). It won the challenge.
<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/167348415-2a0afaff-2d54-405f-b60c-259ac5dec8e6.PNG" width="550"  title="CNN">
</p>
