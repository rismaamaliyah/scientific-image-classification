# Scientific Image Classification using CNNs with TensorFlow

## Project Overview
Scientific research increasingly produces large volumes of image-based data that require inspection and categorization. This project aims to automate the classification of scientific images using deep learning techniques. A Convolutional Neural Network (CNN) was developed to classify images into six distinct categories representing different scientific imaging modalities.

The model was trained an over 19,000 scientific images and evaluated using multiple performance metrics, including accuracy, confusion matrices, and classification reports. To support deployment across different platforms, the trained model was exported into TensorFlow SavedModel, TensorFlow Lite, and TensorFlow.js formats.

## Problem Statement
Manual classification of scientific and biomedical images is time-consuming, repetitive, and prone to human error, especially when handling large-scale datasets.

Additionally, visually similar categories such as Histopathology, Macroscopy, and Microscopy can be challenging to distinguish consistently.

The challenge of this project was to build a robust image classification model capable of automatically identifying scientific image categories while maintaining high classification accuracy across multiple classes.

## Objectives

### Main Objectives
Develop an image classification model capable of accurately classifying scientific images into six predefined categories.

### Specific Objectives
- Perform multi-class image classification using CNN architectures.
- Build a deep learning model using TensorFlow and Keras.
- Achieve strong classification performance on unseen test data.
- Evaluate model performance using accuracy, confusion matrix, precision, recall, and F1-score.
- Export the trained model into multiple deployment-ready formats:
  - TensorFlow SavedModel
  - TensorFlow Lite (TFLite)
  - TensorFlow.js (TFJS)
- Demonstrate model inference on new images.

## Dataset / Data Source

### Dataset
[**Scientific Image Classification Dataset**](https://www.kaggle.com/datasets/rushilprajapati/data-final)

### Characteristics
- Total images: ~19,100
- Classes: 6
| Class |
| ----- |
| Blot-Gel |
| FACS |
| Histopathology |
| Macroscopy |
| Microscopy |
| Non-scientific |

### Description
The dataset contains various scientific and biomedical imaging modalities collected for scientific image classification research and machine learning applications. Images include microscopy images, histopathology slides, electrophoresis results, flow cytometry, and non-scientific control images.

## Tools & Technologies

### Programming Language
- Python

### Libraries
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
- TensorFlow.js
- Split-Folders
- Pillow

### Development Environment
- Google Colab

### Model Export Formats
- SavedModel
- TensorFlow Lite (TFLite)
- TensorFlow.js (TFJS)

## Methodology / Process

### 1. Data Preparation
- Downloaded and explored the scientific image dataset.
- Inspected class distribution and image organization.
- Split dataset into:
  - Training Set (70%)
  - Validation Set (20%)
  - Test Set (10%)

### 2. Data Preprocessing
- Resized images to 224x224 pixels.
- Normalized pixel values using `ImageDataGenerator`.
- Generated training, validation, and testing pipelines.

### 3. CNN Model Development
Built a Sequential CNN architecture consisting of:
- Conv2D Layers
- Batch Normalization
- MaxPooling2D Layers
- Dense Layers
- Dropout Layers
- Softmax Output Layer

### 4. Training and Optimization
- Adam Optimizer
- Categorical Crossentropy Loss
- EarlyStopping
- ModelCheckpoint
- Class Weighting to address class imbalance

### 5. Model Evaluation
Evaluated model performance using:
- Accuracy
- Loss Curves
- Confusion Matrix
- Classification Report
  - Precision
  - Recall
  - F1-Score

### 6. Model Deployment Preparation
Converted the trained model into:
- TensorFlow SavedModel
- TensorFlow Lite
- TensorFlow.js

Performed inference testing to validate deployment readiness.

## Key Findings / Insights

### Performance
- Achieved approximately **93% test accuracy** on unseen data.
- Achieved validation accuracy exceeding **90%** during training.
- Demonstrated strong classification capability across six images categories.

### Confusion Matrix Insights
- Histopathology, Macroscopy, and Non-scientific classes achieved strong classification performance.
- Microscopy images were occasionally confused with Macroscopy and Histopathology due to visual similarities in biological structures.
- Applying class weighting improved class balance and recall performance for minority classes.

### Technical Insights
- Batch Normalization and Dropout significantly improved model stability and reduced overfitting.
- Class weighting helped address dataset imbalance across scientific imaging categories.
- Exporting to SavedModel, TFLite, and TFJS enabled model deployment flexibility across cloud, mobile, and web environments.

## Skills Demonstrated
- Deep Learning
- Computer Vision
- Image Classification
- Convolutional Neural Network (CNN)
- TensorFlow
- Keras
- Data Preprocessing
- Model Evaluation
- TensorFlow LIte
- TensorFlow.js
- Machine Learning Development
- Python

