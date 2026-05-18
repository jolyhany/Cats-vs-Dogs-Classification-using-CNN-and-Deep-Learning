# Cats vs Dogs Classification using CNN and Deep Learning

## Problem Description
This project builds a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images into two categories:

- Cats
- Dogs

The project applies Deep Learning techniques including:

- Convolutional Layers
- Max Pooling
- Batch Normalization
- Dropout
- Data Augmentation

Two different experiments were performed using different optimizers:

- Adam Optimizer
- SGD Optimizer

The task is a **Binary Classification Problem** because the model predicts one of two classes (Cat or Dog).

---

# Dataset

## Dataset Used
CIFAR-10 Dataset (Filtered for Cats and Dogs classes)

## Dataset Links
- CIFAR-10 Dataset: https://www.cs.toronto.edu/~kriz/cifar.html
- Roboflow Dataset: https://universe.roboflow.com/dogs-vs-cats-cv74e/dogs-vs-cats-7swcg

The project filters:

- Class 3 → Cat  
- Class 5 → Dog  

Dataset is automatically downloaded using:

```python
torchvision.datasets.CIFAR10(download=True)
```

---

# Libraries Used

The project uses the following Python libraries:

```python
tensorflow
torch
torchvision
numpy
pandas
matplotlib
scikit-learn
```

Install dependencies using:

```bash
pip install tensorflow torch torchvision numpy pandas matplotlib scikit-learn
```

---

# Project Workflow

## 1. Import Libraries
Required libraries for Deep Learning, preprocessing, and visualization are imported.

---

## 2. Load Dataset
The CIFAR-10 dataset is downloaded and loaded using TorchVision.

---

## 3. Filter Classes
Only the following classes are selected:

- Cats
- Dogs

---

## 4. Data Preprocessing

Image preprocessing includes:

- Resize images to 128×128
- Normalize pixel values
- Convert images to tensors

---

## 5. Data Augmentation

Data augmentation techniques used:

- Rotation
- Zoom
- Horizontal Flip

These techniques improve model generalization and reduce overfitting.

---

# CNN Model Architecture

The CNN architecture contains:

- Conv2D Layers
- MaxPooling Layers
- Batch Normalization
- Flatten Layer
- Dense Layers
- Dropout Layer
- Sigmoid Output Layer

---

# Training

The model is trained using:

- Binary Crossentropy Loss
- Accuracy Metric

Two optimizers were tested:

- Adam
- SGD

---

# Experiments

## Experiment 1 — Adam Optimizer

### Architecture

- Conv2D → 32 Filters
- MaxPooling
- Conv2D → 64 Filters
- MaxPooling
- BatchNormalization
- Flatten
- Dense(128)
- Dropout(0.5)
- Dense(1, sigmoid)

### Optimizer
Adam

---

## Experiment 2 — SGD Optimizer

### Architecture

- Conv2D → 32 Filters
- MaxPooling
- Conv2D → 64 Filters
- MaxPooling
- Flatten
- Dense(128)
- Dropout(0.3)
- Dense(1, sigmoid)

### Optimizer
SGD

---

# Results

| Model | Accuracy | Loss |
|------|------|------|
| Adam | 0.792109 | 0.478907 |
| SGD | 0.764289 | 0.485643 |

---

# Best Model

The Adam optimizer achieved the best performance because it produced:

- Higher Accuracy
- Lower Loss

This indicates that Adam improved learning efficiency and produced better classification results.

---

# Visualization

The project includes:

- Accuracy Graphs
- Loss Graphs

These visualizations help analyze:

- Training Performance
- Validation Performance
- Overfitting Behavior

---

# Save Model

The trained model is saved as:

```bash
cats_vs_dogs_model.h5
```

---

# Instructions for Running the Project

## Step 1: Install Required Libraries

```bash
pip install tensorflow torch torchvision numpy pandas matplotlib scikit-learn
```

---

## Step 2: Open Google Colab

https://colab.research.google.com

---

## Step 3: Mount Google Drive

The dataset zip file should be stored inside Google Drive.

Example path:

```bash
/content/drive/MyDrive/DEEP LEARNING/dataset.zip
```

---

## Step 4: Run the Notebook

Run all cells sequentially.

The notebook will:

- Download dataset
- Preprocess images
- Train CNN models
- Evaluate models
- Display graphs
- Save trained model

---

# Output

The project outputs:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Comparison Table
- Saved CNN Model

---

# Conclusion

This project demonstrates how Convolutional Neural Networks (CNNs) can be used for image classification tasks.

Different optimizers were tested to compare their impact on model performance.

The Adam optimizer achieved the best overall results for Cats vs Dogs classification.
