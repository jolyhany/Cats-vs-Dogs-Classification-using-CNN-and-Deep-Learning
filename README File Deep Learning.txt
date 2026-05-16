Cats vs Dogs Classification using CNN and Deep Learning
Problem Description
This project builds a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images into two categories:
Cats
Dogs
The project applies Deep Learning techniques including:
Convolutional Layers
Max Pooling
Batch Normalization
Dropout
Data Augmentation
Two different experiments were performed using different optimizers:
Adam Optimizer
SGD Optimizer
The task is a Binary Classification Problem because the model predicts one of two classes (Cat or Dog).
---
Dataset
Dataset Used:
CIFAR-10 Dataset (Filtered for Cats and Dogs classes)
Dataset Link:
https://www.cs.toronto.edu/~kriz/cifar.html
The project filters:
Class 3 → Cat
Class 5 → Dog
Dataset is automatically downloaded using:
python
torchvision.datasets.CIFAR10(download=True)

---
Libraries Used
The project uses the following Python libraries:
python
tensorflow
torch
torchvision
numpy
pandas
matplotlib
scikit-learn

Install dependencies using:
pip install tensorflow torch torchvision numpy pandas matplotlib scikit-learn
---
Project Workflow
1. Import Libraries
Required libraries for Deep Learning, visualization, and preprocessing are imported.


2. Load Dataset
The CIFAR-10 dataset is downloaded and loaded using TorchVision.
https://universe.roboflow.com/dogs-vs-cats-cv74e/dogs-vs-cats-7swcg 



3. Filter Classes
Only:
Cats
Dogs
are selected from the CIFAR-10 dataset.


4. Data Preprocessing
Image preprocessing includes:
Resize images to 128×128
Normalize pixel values
Convert images to tensors


5. Data Augmentation
Data augmentation techniques:
Rotation
Zoom
Horizontal Flip
These techniques improve model generalization and reduce overfitting.


6. Build CNN Model
The CNN architecture contains:
Conv2D Layers
MaxPooling Layers
Batch Normalization
Flatten Layer
Dense Layers
Dropout Layer
Sigmoid Output Layer


7. Training
The model is trained using:
Binary Crossentropy Loss
Accuracy Metric
Two optimizers were tested:
Adam
SGD


8. Evaluation
The models are evaluated using:
Test Accuracy
Test Loss


Models Architecture
Experiment 1 — Adam Optimizer
Conv2D → 32 Filters
MaxPooling
Conv2D → 64 Filters
MaxPooling
BatchNormalization
Flatten
Dense(128)
Dropout(0.5)
Dense(1, sigmoid)
Optimizer:Adam


Experiment 2 — SGD Optimizer
Conv2D → 32 Filters
MaxPooling
Conv2D → 64 Filters
MaxPooling
Flatten
Dense(128)
Dropout(0.3)
Dense(1, sigmoid)
Optimizer:SGD


Results
Model	Accuracy	Loss
Adam	0.792109	0.478907
SGD	0.764289	0.485643
---

Best Model
The Adam optimizer achieved the best performance because:
Higher Accuracy
Lower Loss
This means the Adam optimizer improved learning efficiency and produced better classification results.
---

Visualization
The project includes:
Accuracy Graphs
Loss Graphs
These visualizations help analyze:
Training performance
Validation performance
Overfitting behavior
---

Save Model
The trained model is saved as:
cats_vs_dogs_model.h5
---
Instructions for Running the Project

Step 1: Install Required Libraries
pip install tensorflow torch torchvision numpy pandas matplotlib scikit-learn
---
Step 1: Open Google Colab
https://colab.research.google.com
---
Step 3: Mount Google Drive
The dataset zip file should be stored inside Google Drive.
Example path:/content/drive/MyDrive/DEEP LEARNING/dataset.zip
---
Step 4: Run the Notebook
Run all cells sequentially.
The notebook will:
Download dataset
Preprocess images
Train CNN models
Evaluate models
Display graphs
Save trained model
---
Output
The project outputs:
Training Accuracy
Validation Accuracy
Training Loss
Validation Loss
Comparison Table
Saved CNN Model
---
Conclusion
This project demonstrates how Convolutional Neural Networks (CNNs) can be used for image classification tasks.
Different optimizers were tested to compare their impact on model performance.
The Adam optimizer achieved the best overall results for Cats vs Dogs classification.