# Deep Learning
## Lesson 13
## Generative Models

<h3>Supervised vs Unsupervised Learning</h3>

The requirement for labelled training data is the key difference between supervised and unsupervised learning. Unsupervised machine learning works with unlabeled or raw data, whereas supervised machine learning uses labelled input and output training data. The model learns the relationship between the labeled input and output data in supervised machine learning.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/172390487-0dabf005-1ccf-4de2-9917-6477f6013d83.png" width="650" title="CNN">
</p>

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/172392586-6794f8c3-d752-4f75-be13-0d7f7e51982d.png" width="450" title="CNN">
</p>

<h3>Generative Models</h3>

In machine learning, generative modeling is an unsupervised learning task that entails automatically detecting and learning regularities or patterns in input data so that the model may be used to produce or output new examples that could have been drawn from the original dataset.
Let's say we have a dataset with photographs of horses. We might want to create a model that can create a fresh image of a horse that has never existed but seems real since the model has learned the general laws that control a horse's appearance. This is the type of problem that generative modeling can tackle.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/172394449-a91ef20c-af47-4458-b870-03a945d5846f.png" width="550" title="CNN">
</p>

Typically, there are two types of generative models: explicit and implicit. Explicit models define a density function of the distribution, while implicit models learn a mapping that generates samples by transforming an easy-to-sample random variable.

<h3>PIXEL RNN</h3>
Using probabilistic density models (such as the Gaussian or Normal distribution) to quantify the pixels of a picture as a product of conditional distributions is an effective way to develop a generative model explicitly. This method transforms the modeling problem into a sequence problem, in which the next pixel value is determined by all of the preceding pixel values.

PixelRNNs are generative neural networks that sequentially predicts the pixels in an image along the two spatial dimensions. The network scans the image one row one pixel at a time in each row. Subsequently it predicts conditional distributions over the possible pixel values. The distribution of image pixels is written as product of conditional distributions and these values are shared across all the pixels of the image.

Reference Link: [Link](https://towardsdatascience.com/auto-regressive-generative-models-pixelrnn-pixelcnn-32d192911173)

<h3>Pixel CNN</h3>

The main drawback of PixelRNN is that training is very slow as each state needs to be computed sequentially. This can be overcome by using convolutional layers and increasing the receptive field. PixelCNNs are a class of powerful generative models with tractable likelihood that are also easy to sample from. The core convolutional neural network computes a probability distribution over a value of one pixel conditioned on the values of pixels to the left and above it.

<h3>Variational Autoencoders</h3>

In a vanilla autoencoder, the encoded vector can only be mapped to the corresponding input using a decoder. It certainly can’t be used to generate similar images with some variability.To achieve this, the model needs to learn the probability distribution of the training data. VAE is one of the most popular approach to learn the complicated data distribution such as images using neural networks in an unsupervised fashion.

<br>

 A variational autoencoder can be defined as being an autoencoder whose training is regularised to avoid overfitting and ensure that the latent space has good properties that enable generative process.in order to introduce some regularisation of the latent space, we proceed to a slight modification of the encoding-decoding process: instead of encoding an input as a single point, we encode it as a distribution over the latent space.The model is then trained as follows:
 
 * First, the input is encoded as distribution over the latent space
 * Second, a point from the latent space is sampled from that distribution
 * Third, the sampled point is decoded and the reconstruction error can be computed
 * Finally, the reconstruction error is backpropagated through the network

Reference Link: [Link1](https://towardsdatascience.com/deep-generative-models-25ab2821afd3)[Link2](https://towardsdatascience.com/understanding-variational-autoencoders-vaes-f70510919f73)

<h3>Generative Adversarial Network </h3>

In June 2014, Ian Goodfellow and his colleagues created the generative adversarial network (GAN), a class of machine learning frameworks. A GAN trained on images, for example, can create new photographs that appear to human observers to be at least superficially authentic, with many realistic traits.
The GAN model architecture is made up of two sub-models: a generator model for creating new instances/examples and a discriminator model for determining whether the generated examples are real, from the domain, or fake, generated by the generator model.

During training, the generator improves its ability to create realistic images, while the discriminator improves its ability to discern them apart. When the discriminator can no longer discern between actual and bogus images, the process approaches equilibrium.

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/172396249-c3c4f082-9def-4891-b18a-cf5f5f0a222f.png" width="650" title="CNN">
</p>

<p align="center">
  <br>
  <img src="https://user-images.githubusercontent.com/45029614/172396433-036c56a0-d169-4bfc-bfd3-6d0511c82724.png" width="650" title="CNN">
</p>


