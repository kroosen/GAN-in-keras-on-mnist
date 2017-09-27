# GAN-in-keras-on-mnist

A GAN approach for generating handwritten digits with a deep neural network written in Keras.

In both notebooks, the MNIST dataset is used.
A generative adversarial network (GAN) is deployed to create unique images of handwritten digits. The generated images look like they're taken from the dataset (that is the purpose), but they are generated from scratch (actually, from noise) and are all unique.

![GAN block diagram](https://docs.google.com/uc?id=0By4QvxAkAiNCcGl4VERMOUdNT0U)

# 2 models

In *GAN-keras-mnist-MLP.ipynb*, a multilayer perceptron network is used for the generator and the discriminator
In *GAN-keras-mnist-DCGAN.ipynb*, a transposed convolutional (or deconvolutional) network is used for the generator and a regular convolutional network is used for the discriminator.

Otherwise, the approach is kept the same

# Samples

You can see some generated samples within each of the notebooks

# Known issues

Further experimentation is required.

- Make the discriminator layers untrainable while training the entire GAN stack. Can d.trainable = False be used, or is it required to set each layer's trainiable attribute to False?
- Why is the DCGAN generator not producing different digits with uniform frequencies? Some digits occur more than others.
