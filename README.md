
# Recipe Name Generation

This repo holds several examples of methods for generating fictitious
recipe names. I wanted to generate food names, but was only able to
acquire a recipe dataset. So, I decided to use the recipe names to
train models to create new recipe names.

## Models

In this project, I trained Seq2Seq autoencoders on recipe names to create
a means of going between names and representative encodings. I also trained
a Generative Adversarial Network (GAN) with the autoencoder to create a
means of generating seemingly realistic recipe names.

## Notebooks

In this repo, I provide a couple of notebooks. They are:

### `foodnames_autoencoder.ipynb`

In this notebook, I only trained the autoencoder. Then, I select random
encodings and use those to generate the fake recipe names.

### `foodnames_gan.ipynb`

This notebook adds the GAN component. While the autoencoder should in
principle train no differently from in the first notebook, this
notebook includes the concept of GANs in the design.

## Setup

I developed this notebook from Arch Linux using Keras front-end on
Tensorflow 2.0. However, I do not suspect that there would be issues
using plain Keras or an older version of Tensorflow (I only used tf.keras
because of compatibility issues between Keras and the Tensorflow 2.0 beta).
You will need Jupyter notebook to run any of the notebooks, as well as Numpy.

## Licenses

The dataset used in the notebooks called Recipe Box provided by Eight Portions
run by Ryan Lee. The dataset is covered by the ODC Attribution License. As the
license requests attribution, I presume that mentioning that the license file
is downloaded by any of the notebooks, along with this blurb, should be
sufficient to cover the terms of use. However, if this is insufficient, I
encourage the author to contact me so that I can fix any issues. The webpage
I initially found the dataset at can be found [here](https://eightportions.com/datasets/Recipes/).

My code is modifiable to be used with other datasets. Therefore, the value of
the code is not bound to the specific data. The code itself will be covered
under the GNU Public License (GPL), a copy of which is provided with this repo.

