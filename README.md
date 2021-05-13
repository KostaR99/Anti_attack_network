# AE-C-network


Neural network that consist of a convolutional autoencoder, that is used for denoisation of images and filling the missing pixels, and convolutional classificator.

Datasets that are used are CIFAR10, FASHON-MNIST and CATS VS DOGS.

On these datasets we can apply attacks like:
  1. FGSM attack
  2. Random noise attack
  3. Gaussian blur attack
  4. Missing pixels attack

Architecture of autoencoder:
  Encoder: 1 input layer, 2 conv2d layers with LeakyReLu activation (slope is 0.001). Kernel stride for out conv2d layers is 2
  Decoder: 2 conv2dTransposed layers with LeakyRelu activation (slope is 0.001) and conv2d layer. Kernel stride for our conv2dTranspose layers is 2
  
Architecture of clasificator:
  4 cycles of conv2d layers with LeakyReLu activation function and maxPooling. After each cycle there is a dropout layer.
  
  Flaten layer
  
  3 cycles of Dense layers with leakyReLu activation. After each cycle there is a dropout layer and batch norm layer. At the end there is a dense layer with number of units same     as the number of dataset classes with softmax activation function.
  
  Project is done in Tensorflow 2.4
  
  Additional libraries needed are:
    1. Matplotplib
    2. numpy
    3. random

Also i used tf.datasets api for loading CATS VS DOGS DATASET


