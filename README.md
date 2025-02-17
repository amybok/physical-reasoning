# Physical Reasoning: Predicting the Stability of Block Towers with Computer Vision Methods

## Overview

This project explores the use of deep learning and computer vision techniques to predict the stability of block towers based on RGB images. The task requires a model to infer physical reasoning principles like gravity and balance purely from visual data. The study evaluates multiple deep-learning architectures to determine their effectiveness in solving this problem.

## Dataset

### Source: 
ShapeStacks dataset

### Content: 
7,680 RGB images of block towers captured from various angles and lighting conditions.

### Task:
Predict the stable height of a given tower before it collapses.

### Classes: 
Stability levels range from 1 to 6.

## Methodology

### 1. Model Selection

The following deep learning models were tested:

**ResNet50:** Deep CNN model with residual connections for feature extraction.

**EfficientNetB0:** Optimized for computational efficiency and accuracy.

**MobileNetV3 (Small & Large):** Designed for lightweight applications while maintaining performance.

### 2. Image Preprocessing

**CLAHE (Contrast Limited Adaptive Histogram Equalization):** Improves contrast while limiting noise.

**Data Augmentation:** Flipping, translation, rotation, and brightness adjustments to enhance model generalization.

**Depth Estimation:** Uses Depth Anything V2 to segment the block tower from the background.

### 3. Training & Evaluation

**Split:** 80% training, 20% validation.

**Loss Function:** Categorical cross-entropy.

**Metrics:** Accuracy, validation loss.

**Hyperparameter Tuning:** Batch sizes (16, 32, 64)

**Optimizers:** Adam, RMSProp

Fine-tuning MobileNetV3Large with additional dense layers and dropout regularization.

## Results

### Best Model: MobileNetV3Large with data augmentation.

Test Accuracy: 55.72% (after fine-tuning and augmentation).

## Challenges Identified:

* Difficulty in generalizing complex structures and occluded blocks.

* Performance drop due to class imbalance (fewer samples for higher stability levels).

* Camera angle variations affecting predictions.

## Conclusion & Future Work

* MobileNetV3Large performed best among tested models.

* Data augmentation significantly improved accuracy.

* Additional techniques, such as multi-task learning and contrastive learning, could further enhance model performance.

* Future work may explore physics-based modelling for improved physical reasoning.

## Specifications

**Frameworks:** TensorFlow, Python

**Hardware:** 
* Kaggle notebook with the following specifications: RAM: 29GB, Disk size: 57.6 GB, GPU: T4 GPU, and CPU: 4 x Intel Xeon CPU.
* Other local environments are a Macbook Air M2 with RAM: 16GB, Disk size: 512GB and a Macbook Pro M1 with RAM: 16GB and Disk size: 1TB
