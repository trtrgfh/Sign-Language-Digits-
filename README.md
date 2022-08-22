# Sign-Language-Digits-Recognition
<img alt="Python" src="https://img.shields.io/badge/python-%2314354C.svg?style=for-the-badge&logo=python&logoColor=white"/> <img alt="Python" src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white" />  <img alt="Numpy" 
src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" />  <img alt="Pandas" 
src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" /> <img alt="Scikit-Learn" 
src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white" /> <img alt="TensorFlow" src="https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white"/> <img alt="Keras" 
src="https://img.shields.io/badge/Jupyter-%23F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white" /> 

## Dataset
- Images of sign language digits
- 1080 training examples of 64 pixel by 64 pixel RGB image 
- 120 validation examples of 64 pixel by 64 pixel RGB image 

## Convolutional Neural Network
- Architecture: Conv2d -> ReLU -> MaxPooling2D -> Conv2d -> ReLU -> MaxPooling2D -> Flatten -> Dense
- Train_acc: 0.8861, Val_acc: 0.8083

## Residual Network 
- Architecture: CONV2D -> BATCHNORM -> RELU -> MAXPOOL -> CONVBLOCK -> IDBLOCK*2 -> CONVBLOCK -> IDBLOCK*3 -> CONVBLOCK -> IDBLOCK*5 -> CONVBLOCK -> IDBLOCK*2 -> AVGPOOL -> FLATTEN -> DENSE 

##### IDBLOCK (Identity Block)
- Main path: Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization
- Input is added with the output to pass through a ReLU activation
- Add()([X, X_shortcut]) -> ReLU

##### CONVBLOCK (Convolutional Block)
- Main path: Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization
- Shortcut path: Conv2d -> BatchNormalization
- Add()([X, X_shortcut]) -> ReLU

##### Evaluate
- Train_acc: 0.9583, Val_acc: 0.8667

## Pre-Trained Model on The SIGNS datasets
- Train_acc: 0.9500, Val_acc: 0.9500









