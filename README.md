# Self-Normalizing Networks
Tutorials and implementations for "Self-normalizing networks"(SNNs) as suggested by Klambauer et al. ([arXiv pre-print](https://arxiv.org/pdf/1706.02515.pdf)). 

## Versions
- see [environment](environment.yml) file for full list of prerequisites. Tutorial implementations use Tensorflow > 2.0 (using Keras), but versions for Tensorflow 1.x 
  users based on the deprecated tf.contrib module are available.

#### Note for Tensorflow >= 1.4 users
Tensorflow >= 1.4 already has the function "tf.nn.selu" and "tf.contrib.nn.alpha_dropout" that implement the SELU activation function and the suggested dropout version. 
#### Note for Tensorflow >= 2.0 users
Tensorflow 2.3 already has selu activation function when using high level framework keras, "tf.keras.activations.selu". 
Must be combined with "tf.keras.initializers.LecunNormal", corresponding dropout version is "tf.keras.layers.AlphaDropout", 
more information available [here](https://www.tensorflow.org/api_docs/python/tf/keras/activations/selu).

## Tutorials

### Tensorflow 1.x 
- Multilayer Perceptron ([notebook](https://github.com/bioinf-jku/SNNs/blob/master/TF_1_x/SelfNormalizingNetworks_MLP_MNIST.ipynb))
- Convolutional Neural Network on MNIST ([notebook](https://github.com/bioinf-jku/SNNs/blob/master/TF_1_x/SelfNormalizingNetworks_CNN_MNIST.ipynb))
- Convolutional Neural Network on CIFAR10 ([notebook](https://github.com/bioinf-jku/SNNs/blob/master/TF_1_x/SelfNormalizingNetworks_CNN_CIFAR10.ipynb))

### Tensorflow 2.x (Keras)
- Convolutional Neural Network on MNIST ([python script](https://github.com/bioinf-jku/SNNs/blob/master/TF_2_x/MNIST-Conv-SELU.py))
- Convolutional Neural Network on CIFAR10 ([python script](https://github.com/bioinf-jku/SNNs/blob/master/TF_2_x/CIFAR10-Conv-SELU.py))

## Design novel SELU functions (Tensorflow 1.x)
- How to obtain the SELU parameters alpha and lambda for arbitrary fixed points ([notebook](https://github.com/bioinf-jku/SNNs/blob/master/TF_1_x/getSELUparameters.ipynb))

## Basic python functions to implement SNNs (Tensorflow 1.x)
are provided as code chunks here: [selu.py](https://github.com/bioinf-jku/SNNs/blob/master/TF_1_x/selu.py)

## Notebooks and code to produce Figure 1
are provided here: [Figure1](https://github.com/bioinf-jku/SNNs/blob/master/figure1/)

## Calculations and numeric checks of the theorems (Mathematica)
are provided as mathematica notebooks here:

- [Mathematica notebook](https://github.com/bioinf-jku/SNNs/blob/master/Calculations/SELU_calculations.nb)
- [Mathematica PDF](https://github.com/bioinf-jku/SNNs/blob/master/Calculations/SELU_calculations.pdf)

## UCI, Tox21 and HTRU2 data sets

- [UCI](http://persoal.citius.usc.es/manuel.fernandez.delgado/papers/jmlr/data.tar.gz)
- [Tox21](http://bioinf.jku.at/research/DeepTox/tox21.zip)
- [HTRU2](https://archive.ics.uci.edu/ml/machine-learning-databases/00372/HTRU2.zip)
