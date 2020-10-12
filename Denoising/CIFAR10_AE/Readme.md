# Denoising RGB images

`Dataset`: CIFAR10

`Model Architecture`: Skip Autoencoder 

`Loss`: Binary Cross Entropy

`Model Input shape`: (32,32,3)

`Optimizer`: RMSProp

## Technology Used

 - Tensoflow
 - Numpy
 - Matplot.lib
 - Python

# STEPS 

 1. Download CIFAR10 dataset and preprocess them.
 
 2. Add random Noise to image.
 
![orig_image](media/cifar10_orig.png)

 3. Train a skip Autoencoder
 
 4. Plot Image reconstruction loss
 
![Image reconstruction loss](media/image_reconstruction_loss.png)

 5. Train for Image Denoising and plot the loss.
 
 ![image denoise loss](media/image_denoising_loss.png)
 
 6. Sample the prediction on test set.
 
 ![test prediction](media/cifar10_predict.png)


## Usage

 python3 CIFAR10_skip_AutoEncoder.ipynb

## Features

-  Callbacks used: [`ReduceLROnPlateau`, `EarlyStopping`]
-  No Checkboard effect in result used `Transposed Convolution` instead of `Upsampling`
-  Prevented overfitting by using Regularization [`Dropout` and `BatchNormalization`]


