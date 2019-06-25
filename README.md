# Face Generation

This is a repo for a project in Deep Learning udacity Nanodegree.

In this project, I use generative adversarial networks to generate new images of faces.

[![Sample Output](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/project-face-generation/assets/processed_face_data.png)](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/project-face-generation/assets/processed_face_data.png)


## Datasets

Datasets necessary for this implementation can be downloaded by clicking [here](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/November/5be7eb6f_processed-celeba-small/processed-celeba-small.zip).

There are 2 main components of this model:

1. **Discriminator**: 3-Layer CNN and 1 FC - Given a face image, distinguishes it as a real or a fake (generated) image

2. **Generator**: 4-Layer CNN - Given a latent vector z, generates a new face image from learned weights from images in training set. It tries to trick the 
Dircriminator to think that the generated image is REAL. 

## List of Hyperparameters used:

* Batch Size = **128**
* Generated Image Size = **32 x 32**  
* Eength of latent vector z = **100**  
* Number of Filters in Discriminator's first hidden layer = **128**
* Number of Filters in Generator's first hidden layer = **128**
* Initial Learning Rate, [beta1, beta2] = **0.0001, [0.3, 0.999]**
* Number of Epochs = **10**
