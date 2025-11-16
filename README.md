# Brain Tumor Classification Using CNN

This project applies a Convolutional Neural Network (CNN) to classify brain MRI images into two categories: **tumor** and **non-tumor**. The model is implemented using TensorFlow and trained on grayscale MRI images sized at 256×256 pixels.

## Overview

The notebook includes the complete workflow for building, training, and evaluating a CNN model using a custom class (`MY_CNN_MODEL`). The workflow consists of:

- Loading and preprocessing image data  
- Applying data augmentation  
- Splitting data into training, validation, and testing sets  
- Building a CNN architecture  
- Training the model with early stopping  
- Plotting accuracy/loss curves  
- Generating confusion matrices  
- Computing test accuracy and classification metrics  

## Model Architecture

The CNN includes:

- Multiple convolutional layers with ReLU activation  
- Max pooling layers  
- Dropout layers to reduce overfitting  
- Dense layers for classification  
- A sigmoid output layer for binary classification  

The model is compiled with the Adam optimizer and binary cross-entropy loss.

## Data Processing

The dataset is read from an image directory containing two classes.  
Preprocessing includes:

- Random flips  
- Random rotations  
- Random zoom  
- Random contrast adjustments  
- Normalization to `[0, 1]`  

## Experiments

Two model instances were tested with different train/validation/test splits:

### Model Instance #1  
- Split: 60% train, 20% validation, 20% test  
- Test Accuracy: **83.33%**

### Model Instance #2  
- Split: 70% train, 20% validation, 10% test  
- Test Accuracy varied, with metrics reported in the notebook

## Evaluation

The notebook provides:

- Accuracy and loss plots over epochs  
- Confusion matrices for train, validation, and test sets  
- Precision, recall, f1-score, and support metrics  

## Contents

- Full implementation in `AI_Project_Submission.ipynb`  
- CNN class handling data setup, model construction, training, and evaluation  
- Visualizations for understanding training behavior and model performance  
