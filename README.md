# AE-C-network


Neural network that consist of a convolutional autoencoder, that is used for denoisation of images, and convolutional clasificator.

Datasets that are used are CIFAR10 and FASHON-MNIST with added random noise.

Architecture of autoencoder:
  Encoder: 1 input layer, 2 conv2d layers with LeakyReLu activation (slope is 0.001). Kernel stride for out conv2d layers is 2
  Decoder: 2 conv2dTransposed layers with LeakyRelu activation (slope is 0.001) and conv2d layer. Kernel stride for our conv2dTranspose layers is 2
  
Architecture of clasificator:
  4 cycles of conv2d layers with LeakyReLu activation function and maxPooling. After each cycle there is a dropout layer.
  
  Flaten layer
  
  3 cycles of Dense layers with leakyReLu activation. After each cycle there is a dropout layer and batch norm layer.
  
  At the end there is one dense layer with number of outputs that is equal to the number of classes in our dataset
