🧠 CIFAR-10 Image Classification with Convolutional Neural Networks
This project demonstrates how to build, train, and evaluate a simple Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images from the CIFAR-10 dataset. The model achieves over 70% test accuracy with just a few lines of code, making it a great starting point for deep learning beginners.
📦 Dataset
CIFAR-10 is a labeled subset of the 80 million tiny images dataset. It consists of:
- 60,000 32×32 color images
- 10 mutually exclusive classes
- 50,000 training images and 10,000 test images
Class labels:
['airplane', 'automobile', 'bird', 'cat', 'deer',
 'dog', 'frog', 'horse', 'ship', 'truck']


🛠️ Project Structure
- Data Loading & Preprocessing: Normalize pixel values to [0, 1]
- Visualization: Display sample images with class labels
- Model Architecture:
- 3 × Conv2D layers with increasing filters (32 → 64 → 64)
- 2 × MaxPooling2D layers
- Flatten + Dense layers for classification
- Training: 10 epochs using Adam optimizer and SparseCategoricalCrossentropy loss
- Evaluation: Accuracy and loss plots + final test metrics
🧪 Model Summary
Conv2D(32, kernel_size=3x3, activation='relu')
MaxPooling2D(pool_size=2x2)
Conv2D(64, kernel_size=3x3, activation='relu')
MaxPooling2D(pool_size=2x2)
Conv2D(64, kernel_size=3x3, activation='relu')
Flatten()
Dense(64, activation='relu')
Dense(10)  # Output layer


📈 Training Performance
- Optimizer: Adam
- Loss Function: SparseCategoricalCrossentropy (with logits)
- Metrics: Accuracy
- Validation: CIFAR-10 test set
Plots generated:
- Training vs Validation Accuracy
- Training vs Validation Loss
✅ Results
After training for 10 epochs, the model achieved:
- Test Accuracy: ~70%
- Test Loss: Reported after evaluation
🚀 Getting Started
Requirements
- Python ≥ 3.7
- TensorFlow ≥ 2.x
- Matplotlib
Installation
pip install tensorflow matplotlib


Run the Project
python cnn_cifar10.py


📚 References
- TensorFlow Keras Guide
- CIFAR-10 Dataset
- CNN Glossary
- TensorFlow Quickstart for Experts

