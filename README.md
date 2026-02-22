
# Handcrafted Feature-Based Classification using COIL-20
## Overview

This project presents a complete handcrafted feature-based object classification pipeline using the COIL-20 dataset. Unlike deep learning approaches, this system relies on interpretable feature engineering techniques such as:
- Histogram of Oriented Gradients (HOG)
- Local Binary Patterns (LBP)
- Discrete Wavelet Transform (DWT)
- Dimensionality reduction techniques (PCA and LDA) are applied to overcome the Curse of Dimensionality, followed by classification using a Linear Support Vector Machine (SVM).
The system achieves:
**99.31% accuracy on clean images**
**87.2% accuracy under Gaussian noise**
This demonstrates that traditional computer vision techniques remain powerful, efficient, and robust alternatives to deep learning.

## Dataset
**COIL-20 (Columbia Object Image Library)**
- 1,440 grayscale images
- 20 object classes
- 72 images per object
- 5° rotation increments (0–360°)
- Image size: 128×128
The dataset tests rotation invariance, making classification more challenging.

## System Architecture
The pipeline follows:
Data Ingestion
↓
Preprocessing
↓
Feature Extraction (HOG + LBP + Wavelet)
↓
Dimensionality Reduction (PCA / LDA)
↓
Linear SVM Classification
↓
Evaluation Metrics

## Feature Extraction Details

* HOG
9 orientations
8×8 pixels per cell
2×2 cells per block
1764-dimensional feature vector
* LBP
Radius = 3
24 sampling points
Uniform patterns (26 bins)
* Wavelet
Haar Wavelet
LL sub-band used for structural representation

## Classifier
- Linear Support Vector Machine
- Kernel: Linear
- Regularization Parameter (C): 1.0
- 5-Fold Cross Validation

## Evaluation Metrics
Accuracy
Precision
Recall
F1-Score
20×20 Confusion Matrix

## Key Findings

HOG + Linear SVM gave highest accuracy.
LDA outperformed PCA for classification tasks.
Wavelet features improved noise robustness.
Handcrafted features can rival deep learning on controlled datasets.
System is lightweight and computationally efficient.

## Technologies Used
- Python
- OpenCV
- NumPy
- Scikit-learn
- PyWavelets
- Matplotlib

## Conclusion 
This project proves that handcrafted feature engineering remains a powerful, interpretable, and resource-efficient solution for object recognition. By combining geometric, textural, and frequency-domain features with supervised dimensionality reduction, we developed an accurate classification system.

This project proves that handcrafted feature engineering remains a powerful, interpretable, and resource-efficient solution for object recognition. By combining geometric, textural, and frequency-domain features with supervised dimensionality reduction, we developed a highly accurate and robust classification system.
