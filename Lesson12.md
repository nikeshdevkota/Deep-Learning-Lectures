# Deep Learning
## Lesson 12
## Visualizing and Understanding Deep Neural Networks

<h3>Visualization technique</h3>
Large Convolutional Network models have recently demonstrated impressive classification performance on the ImageNet benchmark. But, without clear understanding
of how and why they work, the development of better models is reduced to trial-and-error. With visualization technique, we can determine what each layer in the network is learning and from that we can gain some insights to improve performance. 

Visualization  also allows us to observe the evolution of features during training and to diagnose potential problems with the model.

<h3>Visualizing First Layer</h3>
In Alexnet, the first convolutional layer consists of filters, each convolutional filter has shape 3 * 11 * 11 and there are 64 number of filters. These convolutional layers
get slid over the input image. Then, we take the inner products between some chunk of input image and weights of the convolutional filter and that gives us our output after the first convolutional layer.

No matter which architecture we use, we can always find that the first layers of any convolution network is looking for oriented images and opposing colors which is similar to theory by Hubel and Wiesel. The theory summarized that the human visual system is known to detect things like oriented edges at the very early layer of the human visual system.

In the first layer, we visualize 64 (each of 3 * 11 * 11 size) features as images.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170627446-7fd38e1c-57a4-42b5-9304-5bb64bab686f.PNG" width="250" title="CNN">
</p>

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170627573-2ef18834-43a9-486e-9b49-6e02b0a08891.PNG" width="850" title="CNN">
</p>

<h3>Visualizing Intermediate Layer</h3>

If we draw the exact same visualization for the intermediate layers, it is actually a lot less interpretable.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170631541-72d75e90-0448-4130-a495-9f6f4270152f.PNG" width="650" title="CNN">
</p>

<h3>Visualizing Last Layer</h3>
To understand what's happening in the convolution network, we can look at what's happenning in the last layer of the network. 

Often before the last layer, we have a fully connected layer. In AlexNet, we have a 4096-dimensional feature vector for an image before the classifier. We can run the network on many images, and collect the feature vectors.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/170632221-93bff3e1-3727-49b6-8bea-2f37a1390f74.PNG" width="650" title="CNN">
</p>

In nearest neighbors classifier, we look at the nearest neighbors in pixel space. It didn't have features of images that were quite similar to the query image but rather they were similar looking images in terms of fixels. When we look at nearest neighbours in feature space in ConvNet, we get the images that are quite similar to the query image.

<h3>Dimensionality Reduction</h3>
Dimensionality reduction refers to techniques that reduce the number of input variables in a dataset. More input features often make a predictive modeling task more challenging to model, more generally referred to as the curse of dimensionality.

<h3>Visualizing Activations</h3>
The visualization for the intermediate layers, it is actually a lot less interpretable but visualizing activation is interpretable. We can visualize <strong> "what kind of things in the input are each of those features in that covolution layer looking for?"</strong>

<h3>Maximally activating patches</h3>

Another thing we can do to visualize the intermediate layer is visualizing what type of patches from input images cause maximal activation in different neurons.<br>
One simple way to get a hint of the features that neurons learn is by measuring their responses to test images. We feed many images to the network, and then for a particular neuron of interest, we extract patches of those images which maximally activated it.

Reference Link: [Link](https://ml4a.github.io/ml4a/visualizing_convnets/)

<h3>Occlusion Experiments</h3>

* Block some part of the image, run it through the network and monitor the probability of the classifier. Repeat the proces a number of times.
* Figure out which part of the input image cause the network to make its classification decision.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/171357653-542fca25-772c-40c0-9fad-e00d8aeb54ab.PNG" width="650" title="CNN">
</p>

The occlusion experiments tell us that our convolution neural network is actually learning some meaning patterns like detecting the face of a dog from the input. That means that the model is truly picking up the location of a dog instead of identifying based on the surrounding context like a sofa or a couch.

Reference Link: [Link](https://towardsdatascience.com/visualizing-convolution-neural-networks-using-pytorch-3dfa8443e74e)

<h2>Gradient Techniques</h2>

<h3>Saliency Maps</h3>

* How to tell which pixels matter for classification?
* Why does the neural network predict a particular label? 
* What did it see in the image that led to a particular prediction? 

Saliency maps help us visualize where the convolutional neural network is focusing in particular while making a prediction. Generally, we visualize saliency maps as heatmaps overlayed on the original image. We can also visualize them as colored pixels concentrated around the area of interest of an object.

<h3>Guided Backpropagation</h3>


* Neurons act like detectors of a particular image features.
* Interested in what image features that the neuron detects, doesn't care about what it doesn't detect.
* Like DeconvNets, in Guided Backpropagation we only backpropagate positive error signals – i.e. we set the negative gradients to zero (ref). This is the application of the ReLU to the error signal itself during the backward pass.

<h3>Gradient Ascent</h3>

* Generate a synthetic image that maximally activates the neuron.
* Updating the pixels of the image which causes the neuron to be maximally activated.
* Has a regularizer which forces the generated image to look natural.
