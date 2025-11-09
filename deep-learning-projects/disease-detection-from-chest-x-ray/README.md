🩺 Chest X-ray Pneumonia Classification with CNN
This project builds a binary image classifier using Convolutional Neural Networks (CNNs) to detect pneumonia from chest X-ray images. It leverages the publicly available Chest X-ray Pneumonia dataset and includes data balancing, augmentation, training, evaluation, and visualization.

📁 Dataset Overview
- Source: Kaggle - Chest X-ray Pneumonia
- Classes:
- NORMAL: Healthy chest X-rays
- PNEUMONIA: X-rays showing signs of pneumonia
- Structure:
chest_xray/
  ├── train/
  │   ├── NORMAL/
  │   └── PNEUMONIA/
  ├── test/
  └── val/



⚙️ Project Workflow
1. 📦 Environment Setup
import kagglehub
import os, shutil, random
import numpy as np
import tensorflow as tf
from tensorflow.keras import Sequential, layers, models
from tensorflow.keras.preprocessing.image import ImageDataGenerator
import seaborn as sns
from sklearn.metrics import confusion_matrix, classification_report
import matplotlib.pyplot as plt


2. 📥 Dataset Download & Balancing
- Downloaded using kagglehub
- Balanced training set by undersampling the majority class
- Saved to /kaggle/working/train_balanced
3. 🧪 Data Augmentation & Preprocessing
- Applied transformations: rotation, zoom, shift, flip
- Rescaled pixel values to [0, 1]
- Used ImageDataGenerator for both training and testing
4. 🧠 Model Architecture
Sequential([
  Input(shape=(150,150,3)),
  Data Augmentation,
  Conv2D(4, (3,3)) + MaxPooling,
  Conv2D(8, (3,3)) + MaxPooling,
  Flatten,
  Dense(8, relu, L2 regularization),
  Dropout(0.4),
  Dense(1, sigmoid)
])


- Optimizer: Adam
- Loss: Binary Crossentropy
- Metrics: Accuracy
5. 📊 Training & Evaluation
- Trained for 15 epochs
- Evaluated on test set
- Plotted accuracy/loss curves
- Generated classification report and confusion matrix

📈 Results
🔹 Accuracy & Loss Curves
Accuracy and Loss
🔹 Confusion Matrix
Confusion Matrix
🔹 Classification Report
              precision    recall  f1-score   support

      Normal       0.78      0.91      0.84       234
   Pneumonia       0.94      0.84      0.89       390

    accuracy                           0.87       624
   macro avg       0.86      0.88      0.86       624
weighted avg       0.88      0.87      0.87       624


🧠 Key Features
- Balanced training data for fair learning
- Augmentation to improve generalization
- Lightweight CNN architecture
- Visual diagnostics for performance

🚀 How to Run
- Clone the repo or copy the notebook to Kaggle
- Ensure kagglehub is installed
- Run all cells sequentially
- View saved plots: accuracy_loss.png, confusion_matrix.png

📌 Notes
- Data augmentation is applied both via ImageDataGenerator and Keras layers
- Model is simple and interpretable—ideal for educational or baseline use
- Can be extended with transfer learning (e.g., ResNet, VGG)

📚 References
- Kaggle Dataset
- TensorFlow Documentation
- Keras ImageDataGenerator

🧑‍💻 Author
Mhmd — Passionate about building robust ML pipelines and sharing practical resources for real-world impact.

