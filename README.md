[//]: # (Image Reference)

[image1]: ./example.png "Generated Faces"

# Face Generation 

## Overview
In this project, I defined and trained a DCGAN on a dataset of celebrity faces. The goal of this project is to get a generator network to generate new images of faces that look as realistic as possble. The image below is a result of the training:

![Generated Faces][image1]

## Project Instruction

### Instruction

1. Clone the repository and navigage to the downloaded folder.
	```
		git clone https://github.com/dhamijavarun/Face_Generator_DLND_Udacity
		cd Face-Generation
	```
2. Open the `dlnd_face_generation.ipynb` file. You can also find HTML version of the file.
	```
		jupyter notebook dlnd_face_generation.ipynb
	```
3. Read and follow the instructions! This repository does not include the dataset of faces. You can find and download it in the notebook.

## Project Information

### Contents

- Pre-processed Data
- Create a DataLoader
- Define the Model
	- Discriminator
	- Generator
	- Initialize the weights of your network
	- Build complete network
- Discriminator and Generator Losses
- Optimizers
- Training
- Training Loss
- Generator samples from training

### Model - Discriminator
| Layer | Input Dimension | Output Dimension | Batch Normalization|
|-------|-----------------|------------------|-------------|
|Conv1|3|64|False|
|Conv2|64|128|True|
|Conv3|128|256|True|
|FC|4096|1|False|

### Model - Generator
| Layer | Input Dimension | Output Dimension | Batch Normalization|
|-------|-----------------|------------------|-------------|
|FC|100|4096|False|
|Deconv2|256|128|True|
|Deconv3|128|64|True|
|Deconv4|64|3|False|

### Libraries

The libraries used are listed below.
- [PyTorch](https://pytorch.org) (Generator and Discriminator)

### Training Process
Training phase takes too long to complete so it's recommended to train the faces dataset on a GPU.
