# PRODIGY_ML_03
This repository contains the source code of the task-03:  Implement a support vector machine (SVM) to classify images of cats and dogs from the Kaggle dataset. Dataset:https://www.kaggle.com/datasets/tongpython/cat-and-dog

# 🐱🐶 Cat and Dog Classification using HOG + PCA + SVM

This project implements a machine learning pipeline to classify images of cats and dogs using classical computer vision techniques. The approach leverages **Histogram of Oriented Gradients (HOG)** for feature extraction, **Principal Component Analysis (PCA)** for dimensionality reduction, and **Support Vector Machine (SVM)** for classification.

## 📁 Dataset

- **Source**: [Kaggle: Cat and Dog Dataset](https://www.kaggle.com/datasets/tongpython/cat-and-dog)
- The dataset is downloaded using `kagglehub` and extracted into the working directory.
- Contains labeled images in two categories: `cat` and `dog`.

## 🔍 Feature Extraction

- All images are resized to **128×128** pixels.
- **HOG (Histogram of Oriented Gradients)** is applied to each image to extract structural features and texture information.
- HOG features are flattened into a 1D feature vector for each image.

## 📉 Dimensionality Reduction

- **PCA (Principal Component Analysis)** is applied to reduce the number of features while retaining most of the variance.
- Helps in reducing noise, speeding up training, and preventing overfitting.

## 🤖 Model

- **SVM Classifier** is used with an RBF (Radial Basis Function) kernel.
- **GridSearchCV** is used to find the optimal hyperparameters (e.g., `C` and `gamma`).

## 🧪 Training & Evaluation

- Data is split using `train_test_split` from scikit-learn.
- The model is trained on HOG + PCA-transformed features.
- Evaluation metrics:
  - **Accuracy Score**
  - **Confusion Matrix**
  - **Classification Report** (Precision, Recall, F1-Score)

## 📊 Results

- The model demonstrates high accuracy in distinguishing between cats and dogs.
- Misclassifications and model behavior are analyzed via confusion matrix.

## 🛠️ Tools & Libraries

- Python
- scikit-learn
- `skimage` (for HOG)
- `PIL` and `matplotlib`
- `kagglehub` (for dataset download)


