👕 Fashion MNIST Image Classification with TensorFlow
This project demonstrates how to build, train, and evaluate a neural network using TensorFlow and Keras to classify grayscale images of clothing items from the Fashion MNIST dataset. It serves as a beginner-friendly introduction to deep learning for computer vision tasks.
📌 Project Overview
The goal is to classify 28x28 grayscale images into one of 10 fashion categories, such as T-shirts, trousers, and sneakers. The model is trained on 60,000 labeled images and evaluated on 10,000 test images.
🧰 Tech Stack
- Language: Python
- Framework: TensorFlow 2.x with Keras API
- Libraries:
- NumPy
- Matplotlib
🗂️ Dataset
- Source: Fashion MNIST
- Size: 70,000 images (60,000 training + 10,000 testing)
- Classes: | Label | Class        | |-------|--------------| | 0     | T-shirt/top  | | 1     | Trouser      | | 2     | Pullover     | | 3     | Dress        | | 4     | Coat         | | 5     | Sandal       | | 6     | Shirt        | | 7     | Sneaker      | | 8     | Bag          | | 9     | Ankle boot   |
🚀 How It Works
1. Data Loading & Exploration
- Load the Fashion MNIST dataset directly from TensorFlow.
- Visualize sample images and inspect dataset dimensions.
2. Preprocessing
- Normalize pixel values to the range [0, 1].
- Visualize the first 25 training images with their labels.
3. Model Architecture
Built using tf.keras.Sequential:
model = tf.keras.Sequential([
    tf.keras.layers.Flatten(input_shape=(28, 28)),
    tf.keras.layers.Dense(128, activation='relu'),
    tf.keras.layers.Dense(10)
])


4. Compilation
model.compile(optimizer='adam',
              loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True),
              metrics=['accuracy'])


5. Training
model.fit(train_images, train_labels, epochs=10)


6. Evaluation
test_loss, test_acc = model.evaluate(test_images, test_labels, verbose=2)


7. Prediction & Visualization
- Attach a Softmax layer to convert logits to probabilities.
- Visualize predictions alongside confidence scores and true labels.
📊 Results
- Achieved ~91% accuracy on training data.
- Slightly lower accuracy on test data due to minor overfitting.
- Visualizations help interpret model confidence and misclassifications.
📌 Key Learnings
- How to preprocess image data for neural networks.
- Building and training a simple feedforward neural network.
- Evaluating model performance and visualizing predictions.
- Understanding overfitting and model generalization.
📁 Project Structure
fashion-mnist-classifier/
├── fashion_mnist_classifier.py   # Main script
├── README.md                     # Project documentation
└── requirements.txt              # Dependencies (optional)


✅ Requirements
- Python 3.7+
- TensorFlow 2.x
- NumPy
- Matplotlib
Install dependencies:
pip install tensorflow numpy matplotlib


📚 References
- TensorFlow Keras Guide
- Fashion MNIST Dataset

