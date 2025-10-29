🧠 TensorFlow Fundamentals & Benchmarking
A hands-on walkthrough of TensorFlow basics, including tensor operations, eager vs graph execution, activation functions, and performance benchmarking against NumPy. Ideal for beginners and intermediate learners exploring deep learning workflows in Python.
📌 Project Highlights
- TensorFlow 2.x constants, variables, and operations
- Legacy TensorFlow 1.x: placeholders and sessions
- Element-wise and matrix operations
- Broadcasting, reduction, and activation functions
- Gradient computation using tf.GradientTape
- Performance comparison: TensorFlow vs NumPy
- Forward propagation with activation modularity
📁 Structure
├── tensorflow_basics.py         # Core TensorFlow operations and examples
├── forward_propagation.py       # NumPy-based forward pass with activation functions
├── benchmark_numpy_vs_tf.py     # Performance comparison of large matrix multiplication
├── README.md                    # Project overview and instructions


🚀 Getting Started
Prerequisites
- Python 3.8+
- TensorFlow 2.x
- NumPy
- Matplotlib (optional for visualization)
Installation
pip install tensorflow numpy matplotlib


Run Examples
python tensorflow_basics.py
python forward_propagation.py
python benchmark_numpy_vs_tf.py


🔍 Key Concepts
✅ TensorFlow 2.x
- tf.constant, tf.Variable
- Eager execution (default)
- Broadcasting and reduction (tf.reduce_sum, tf.reduce_mean)
- Gradient computation with tf.GradientTape
🕰️ TensorFlow 1.x Legacy
- tf.placeholder
- tf.Session
- Graph execution with feed_dict
🧮 Tensor Operations
- Element-wise: tf.add, tf.subtract, tf.multiply, tf.divide
- Matrix multiplication: tf.matmul
- Activation functions: sigmoid, ReLU, tanh (NumPy-based)
⚙️ Benchmarking
Compare performance of large matrix multiplication using:
- np.dot (NumPy)
- tf.matmul (TensorFlow)
📊 Sample Output
Result of a * x + b: 25.0
New result after updating x: 30.0
Neural Network Layer Output:
 [[2.5 3.0]
  [5.5 6.0]]
Scaled Image:
 [[127.5 64.0]
  [32.0 16.0]]
NumPy Duration: 1.234567 seconds
TensorFlow (CPU) Duration: 0.987654 seconds


🙌 Acknowledgments
Inspired by foundational deep learning tutorials and guided by mentors like Daniel Bourke and Lara Wehbe. This project is part of a broader effort to build intuitive, well-documented ML pipelines.
📌 License
This project is licensed under the MIT License.

