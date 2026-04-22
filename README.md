# Comparative Analysis of Neural Network Architectures for Image Classification

## Overview

This project explores and compares the performance of different neural network architectures — Perceptron, Artificial Neural Network (ANN), and Convolutional Neural Network (CNN) — on an image classification task.

Instead of focusing on a single model, the aim here was to understand how model architecture affects learning, accuracy, and generalization when working with image data.

---

## Motivation

While learning deep learning, I wanted to move beyond simply implementing models and instead understand:

- Why deeper architectures perform better
- How convolutional layers improve image understanding
- What limitations exist in simpler models like Perceptron

This project is an attempt to build that intuition through hands-on experimentation and comparison.

---

## Dataset

- Grayscale image dataset (28 × 28 pixels)
- Each image represented as flattened pixel values
- Multi-class classification (10 classes: 0–9)

---

## Data Preprocessing

- Converted dataset into NumPy arrays
- Normalized pixel values from [0, 255] → [0, 1]
- Reshaped inputs:
  - Perceptron & ANN → flattened (28×28)
  - CNN → (28×28×1) format
- Applied one-hot encoding for labels

---

## Models Implemented

### 1. Perceptron (Baseline Model)
- Single Dense layer with Softmax activation
- Optimizer: SGD

**Purpose:** Establish a linear baseline for comparison

---

### 2. Artificial Neural Network (ANN)
- Architecture:
  - Dense(128) → ReLU
  - Dense(64) → ReLU
  - Output layer → Softmax
- Optimizer: Adam

**Purpose:** Capture non-linear patterns in data

---

### 3. Convolutional Neural Network (CNN)
- Conv2D(32) → ReLU
- MaxPooling
- Conv2D(64) → ReLU
- MaxPooling
- Dense(128) + Dropout
- Output layer → Softmax
- Optimizer: Adam

**Purpose:** Extract spatial features and improve classification accuracy

---

## Training Details

- Train-test split: 80/20
- Batch size: 32
- Epochs: 5
- Loss: Categorical Crossentropy

---

## Results

| Model        | Test Accuracy |
|-------------|-------------|
| Perceptron  | 89.15% |
| ANN         | 95.97% |
| CNN         | 98.38% |

---

## Observations

- The **Perceptron** struggled due to its linear nature and lack of hidden layers.
- The **ANN** significantly improved performance by learning non-linear relationships.
- The **CNN** achieved the best results by effectively capturing spatial patterns in image data.

> Key takeaway:  
> Model architecture plays a critical role in performance, especially for image-based tasks where spatial structure matters.

---

## Visualizations

The project includes:
- Training vs Validation accuracy plots
- Loss curves for each model
- Validation accuracy comparison graph
- Confusion matrix (CNN)
- Side-by-side prediction comparisons

---

## Tech Stack

- Python
- NumPy, Pandas
- TensorFlow / Keras
- Scikit-learn
- Matplotlib, Seaborn

---

## What I Learned

- Practical differences between linear and deep models
- Importance of architecture selection
- How CNNs extract hierarchical features from images
- Model evaluation using multiple metrics and visualizations

---

## Future Improvements

- Train models for more epochs for better convergence
- Experiment with deeper CNN architectures
- Hyperparameter tuning
- Apply transfer learning on more complex datasets



