<img src="https://github.com/trtrgfh/Sign-Language-Digits-Recognition/assets/73056232/6f907dc1-1470-4b06-aaf8-a3dd070eaae4" width="450"/>

# Sign Language Digits Recognition

# Project Overview
The goal of this project is to develop an accurate and efficient system for recognizing hand-sign digits in sign language using Convolutional Neural Networks (CNN) and Residual Networks (ResNet).

# Installation and Setup
## Python Packages Used
- **Data Manipulation:** numpy, scipy, h5py
- **Data Visualization:** matplotlib, PIL
- **Machine Learning:** tensorflow, tensorflow.keras

# Data
Datasets used can be found in the datasets foleder which contains:
- 1080 training examples of 64 pixel by 64 pixel RGB image 
- 120 validation examples of 64 pixel by 64 pixel RGB image 

# Results and evaluation
## Convolutional Neural Network
- Architecture: Conv2d -> ReLU -> MaxPooling2D -> Conv2d -> ReLU -> MaxPooling2D -> Flatten -> Dense
- Train_acc: 0.8861, Val_acc: 0.8083

## ResNet50 Model
- Architecture: CONV2D -> BATCHNORM -> RELU -> MAXPOOL -> CONVBLOCK -> IDBLOCK * 2 -> CONVBLOCK -> IDBLOCK * 3 -> CONVBLOCK -> IDBLOCK * 5 -> CONVBLOCK -> IDBLOCK * 2 -> AVGPOOL -> FLATTEN -> DENSE 
- Train_acc: 0.9583, Val_acc: 0.8667

#### IDBLOCK (Identity Block)
- Main path: Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization
- Input is added with the output to pass through a ReLU activation
- Add()([X, X_shortcut]) -> ReLU

#### CONVBLOCK (Convolutional Block)
- Main path: Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization
- Shortcut path: Conv2d -> BatchNormalization
- Add()([X, X_shortcut]) -> ReLU

## Pre-Trained ResNet50 on The SIGNS datasets
- Train_acc: 0.9500, Val_acc: 0.9500
