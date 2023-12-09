# Key Points Detection

## Introduction
This repository contains the implementation of three different methods for key points detection. The project aims to explore various approaches to accurately detect key points in images. The methods implemented include a custom Deep Neural Network (DNN) built from scratch, a U-Net based approach, and the utilization of YOLO for pose estimation.

## Methods Used

### 1. From Scratch using DNN
- **Preprocessing**: 
  - Used `albumentations` library for data augmentation to enhance the model's ability to generalize.
- **Modeling**:
  - Employed `MobileNetV3` as the base model.
  - Added two output layers on top of it for regression and classification tasks.

### 2. Using U-Net
- **Preprocessing**:
  - Converted the key points into heatmaps and resized them to 224x224 pixels.
  - Applied `albumentations` for data augmentation.
- **Modeling**:
  - Developed a U-Net model from scratch.
  - Trained the model on the processed dataset.

### 3. Using YOLO for Pose Estimation
- **Preprocessing**:
  - Annotated the images and organized the data into a YOLO-compatible format.
- **Modeling**:
  - Utilized YOLO for pose estimation to identify key points.

## Conclusion
Upon evaluation, the models were ranked based on their performance in key points detection. The results are as follows:
- **Best Performance**: YOLO
- **Second Best**: Custom DNN
- **Third**: U-Net

The YOLO-based approach showed superior accuracy and efficiency in key points detection, followed by the custom DNN and U-Net models.
