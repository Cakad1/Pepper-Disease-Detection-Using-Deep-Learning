# Pepper-Disease-Detection-Using-Deep-Learning
This project creates a CNN model to classify bell peppers as healthy or diseased (bacterial spot). Trained on an augmented image dataset, the model achieved 100% accuracy, supporting real-time disease detection to assist farmers in managing crop health and boosting yield.

## Table of Contents
- [Introduction](#introduction)
- [Project Aim](#project-aim)
- [Methodology](#methodology)
- [Training and Validation](#training-and-validation)
- [Results and Analysis](#results-and-analysis)
- [Deployment and Model Saving](#deployment-and-model-saving)
- [Conclusion](#conclusion)

## Introduction 
The detection of diseases in crops is a crucial task for ensuring food security and optimal agricultural yield. This project focuses on using deep learning to detect bacterial spot disease in bell peppers, a common plant disease that affects pepper quality and yield. The model differentiates between two classes: "healthy peppers" and "peppers affected by bacterial spot.
## Project Aim 
The primary objective of this project is to develop a Convolutional Neural Network (CNN)-based model capable of accurately distinguishing between healthy and diseased pepper plants.

## Methodology
**Data Preparation**

The dataset was divided into training (70%), validation (10%), and test (20%) sets using the splitfolders library to ensure model generalization.
Image preprocessing involved resizing images to 256x256 pixels and rescaling pixel values between 0 and 1 for normalization. Horizontal flipping and rotation augmentations were applied to improve model robustness against variations.

**Model Architecture**

The CNN model consists of several layers:
* **Input Layer** with dimensions corresponding to the image size and RGB channels.
* **Convolutional Layers** with ReLU activation and max-pooling to capture essential features.
* **Flatten Layer** to convert the multi-dimensional output of convolutions into a one-dimensional vector.
* **Dense Layers** for final classification, with softmax activation for outputting class probabilities.
The model was compiled with the Adam optimizer, Sparse Categorical Crossentropy loss, and accuracy as the metric for performance evaluation.

## Training and Validation

The model was trained for 20 epochs with the following results:
* Training accuracy reached 100%, while validation accuracy stabilized at 100% as well, showing the model's effectiveness.
* Training loss decreased significantly across epochs, indicating successful learning without overfitting.
  
**Evaluation**

The final evaluation on the test set yielded a loss of 0.006 and an accuracy of 100%, confirming the model's robustness and high performance.

## Results and Analysis
* **Training Curves** Plots of training and validation accuracy and loss over epochs showed consistent improvement, affirming that the model effectively learned the distinguishing features between the classes.
* **Sample Predictions** The model accurately predicted the disease status on test images, achieving high confidence for each class.
* **Class Names** The two classes predicted by the model are 'Pepper__bell___Bacterial_spot' and 'Pepper__bell___healthy.'
   
## Deployment and Model Saving
The trained model was saved using the Keras .keras format for future use and deployment. This allows the model to be loaded and used for real-time predictions in agricultural applications.

## Conclusion 
The CNN model developed successfully classifies bell pepper images into healthy or diseased categories with exceptional accuracy. This tool can be implemented in the field to aid farmers in early detection and management of bacterial spot disease, potentially improving yield and quality.
