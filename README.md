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
- Conv2d -> ReLU -> MaxPooling2D -> Conv2d -> ReLU -> MaxPooling2D -> Flatten -> Dense
- train_acc: 0.8861, val_acc: 0.8083

## Residual Network 
- CONV2D -> BATCHNORM -> RELU -> MAXPOOL -> CONVBLOCK -> IDBLOCK*2 -> CONVBLOCK -> IDBLOCK*3 -> CONVBLOCK -> IDBLOCK*5 -> CONVBLOCK -> IDBLOCK*2 -> AVGPOOL -> FLATTEN -> DENSE 
### IDBLOCK (Identity Block)
- main path: Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization
- input is added with the output to pass through a ReLU activation
- Add()([X, X_shortcut]) -> ReLU

### CONVBLOCK (Convolutional Block)
- main path: Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization -> ReLU -> Conv2d -> BatchNormalization
- shortcut path: Conv2d -> BatchNormalization
- Add()([X, X_shortcut]) -> ReLU

### Evaluate
- train_acc: 0.9583, test_acc: 0.8667

### Use a pre-trained model on the SIGNS datasets
- train_acc: 0.9500, test_acc: 0.9500









