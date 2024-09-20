# Magnetic Maps Inclination Prediction using convolutional neural networks (CNNs)

## Overview
The purpose of this Project is to train a CNN predictor that can predict inclinations of the magnetization of a source body in the subsurface, given a magnetic data map. 

During this project:
* understand the workflow of training a CNN.
* use Keras to train a CNN and make predictions.

## What is inclination?

The Earth's magnetic field can be represented by a three-dimensional vector. A typical procedure for measuring its direction is to use a compass to determine the direction of magnetic North. Its angle relative to true North is the declination (D) or variation. Facing magnetic North, the angle the field makes with the horizontal is the inclination (I) or magnetic dip. The intensity (F) of the field is proportional to the force it exerts on a magnet.
![img](https://drive.google.com/uc?id=1-IJX4-gJRTmkxgP-diI5p0pndLIPJPf1)

## Preprocessing Data
* Import Package
* Load data
* Simple data transformation
* Data Visualization

![image](https://github.com/Yuteng0927/Deep-Learning-Project/blob/main/Image/Data_Visualization.png)

## Data Training and Prediction
* Prepare training, validation and test data
* Build and train your CNNs
* Check learning curves

![image](https://github.com/Yuteng0927/Deep-Learning-Project/blob/main/Image/Fitting_curve.png)

1. The accuracy and val_accuracy increase.
2. The loss and val_loss decrease.
3. The curves of training and validation data sets are pretty close, which represent our trained model is good, neither underfitting nor overfitting the data.

* Check the accuracies on test data maps
loss: 0.3626 - accuracy: 0.8440
* Make predictions on synthetic test data maps

![image](https://github.com/Yuteng0927/Deep-Learning-Project/blob/main/Image/Prediction.png)

## Make predictions on field data
Geoloy 101: Norite is a mafic intrusive igneous rock composed largely of the calcium-rich plagioclase labradorite, orthopyroxene, and olivine. The name norite is derived from Norge, the Norwegian name for Norway. Norite also known as orthopyroxene gabbro (https://en.wikipedia.org/wiki/Norite). Here is a picture of norite.
![image](https://drive.google.com/uc?id=1j_kpdMFM6BmmJQRzPPmOIsvpIGhY0kmJ)

The magnetic data measured over this area is shown below (left). We observe strong magnetic anomalies resulting from the norite intrusions. In our project, we will focus on the anomalies located in the northwest region, which are shown below (right).
![image](https://drive.google.com/uc?id=1A8NmHyxM1CZ6acqhswX9cjfHo9EmCX5S)
![image](https://drive.google.com/uc?id=1TJRzFz0Uv8yVLGfltkq6RZEd_ENgl3WJ)

* Read the magnetic data

![image](https://github.com/Yuteng0927/Deep-Learning-Project/blob/main/Image/Predict_fieldData.png)
* Make prediction
The predicted inclination is: (0, 10]

