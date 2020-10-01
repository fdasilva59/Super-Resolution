# Image Super-Resolution on Scaleway GPU instances

This repository contains the jupyter notebook example used in the Scaleway's webinar with Kevin Messy (in French) "Éditeurs d’applications mobiles : augmentez la résolution des photos de vos clients"

## Goals of this demo

- Simple example suitable for a first overview of Image Super-Resolution
- Simple demo to fit with the timing of the presentation
- Ditactic example to show how to use Sub-Pixel Convolutional Network to increase image resolution by a factor of 2
- This code is an example and is not intended for production usage (Especially, no serving modules has been implemented here)
- This demo is focusing on the Inference part (A trained model is provided) 

## Sub-Pixel Convolutional Network

The demo's source code has been prepared by Olga Petrova. In addition to the inference code provided in this repository, you can find the training source code in this Scaleway tutorial : ["Achieving Super Resolution with a Sub-Pixel Convolutional Neural Network on Scaleway GPU"](https://www.scaleway.com/en/docs/super-resolution-with-gpu/) (Note that, you will have to bring your own dataset for the training).

### Model training

For your information, in order to train our model, a proprietary dataset of 600000 images (faces) has been used

The training has been performed on a [Scaleway RENDER-S instance](https://www.scaleway.com/en/gpu-instances/) (loaded with 1 Nvidia P100 GPU)
	
The training took 3-4 minutes / epoch, and our model has been trained on 20 epochs

## How to use

In order to execute this notebook, you will need a Jupyter Notebook environment, with Pytorch running on a GPU instance.
