# 🖼️Image Classification System (CIFAR-10)


![Framework](https://img.shields.io/badge/Framework-TensorFlow%20%7C%20Keras-blue)
![Dataset](https://img.shields.io/badge/Dataset-CIFAR--10-orange)
![Model Type](https://img.shields.io/badge/Model-CNN-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Overview

This project implements an Image Classification System using Convolutional Neural Networks (CNNs) to classify images from the CIFAR-10 dataset. The model is built from scratch using deep learning techniques and evaluated using accuracy metrics and a confusion matrix.

The objective of this project is to understand and implement CNN architecture for image recognition tasks using modern deep learning frameworks.

---

## 🚀 What This Project Does

- Loads and preprocesses image data
- Performs image normalization
- Builds and trains a Convolutional Neural Network (CNN)
- Evaluates model performance using:
  - Accuracy
  - Confusion Matrix


---

## 🧠 Concepts & Skills Applied

- Deep Learning (CNN Architecture)
- Image Preprocessing & Normalization
- Model Training & Evaluation
- Confusion Matrix Analysis
- Keras / TensorFlow
- GPU Acceleration
- Performance Monitoring

---

## 📂 Dataset

**CIFAR-10 Dataset**

The CIFAR-10 dataset contains:
- 60,000 32x32 color images
- 10 object classes:
  - Airplane
  - Automobile
  - Bird
  - Cat
  - Deer
  - Dog
  - Frog
  - Horse
  - Ship
  - Truck

Split:
- 50,000 training images
- 10,000 testing images

---

## 🏗️ Model Architecture

The CNN model includes:

- Convolutional Layers (Feature Extraction)
- ReLU Activation Functions
- MaxPooling Layers
- Flatten Layer
- Fully Connected (Dense) Layers
- Softmax Output Layer

The architecture is designed to extract spatial features and classify images into 10 categories progressively.

---

## ⚙️ Preprocessing Steps

- Dataset loading
- Reshaping (if required)
- Pixel value normalization (0–255 → 0–1)
- Train-test split (if custom dataset used)
- Label encoding

---

## 📊 Model Evaluation

The model performance was evaluated using:

- ✅ Accuracy Score  
- ✅ Loss Curve  
- ✅ Confusion Matrix  

### Key Observations

- The CNN successfully learned spatial patterns from the images.
- Training accuracy increased steadily across epochs.
- Validation accuracy showed stable generalization.
- Confusion matrix highlighted minor misclassification between visually similar classes (e.g., cat vs dog).

---

## 📦 Requirements

- Python 3.x
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook


---


## 👨‍💻 Author

**Debaswini-M**  

---


