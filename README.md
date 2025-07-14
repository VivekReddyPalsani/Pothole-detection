# Advanced Pothole Detection for Autonomous Vehicles

This repository contains three Jupyter notebooks that explore different stages of pothole detection and localization using deep learning. All experiments use dash-cam imagery to train and evaluate models that can help autonomous vehicles identify and avoid potholes.

## Code Files

1. **`CNN.ipynb`**  
   - Implements an initial convolutional neural network (CNN) classifier.  
   - Trains on positive (pothole) and negative (no-pothole) samples.  
   - Uses `ImageDataGenerator` for augmentation, early stopping to avoid overfitting, and evaluates performance with confusion matrices.  

2. **`MobileNetV2.ipynb`**  
   - Builds on the classifier by using a pretrained MobileNetV2 backbone.  
   - Modifies the top layers for bounding-box regression (localization).  
   - Preprocesses images to 224×224, scales annotations accordingly, and trains with a custom loss for box coordinates.  
   - Monitors training with learning-rate scheduling and visualizes loss/accuracy curves.  

3. **`Faster_RCNN.ipynb`**  
   - Outlines a proof-of-concept for integrating Faster R-CNN with a ResNet50 FPN backbone.  
   - Includes notes on region proposal networks, sliding-window techniques, and future steps for real-time deployment.  
   - Drafts code skeleton for model setup, inference, and performance benchmarking.  
