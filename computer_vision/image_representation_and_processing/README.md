# 🧠 OpenCV Image Processing Projects

This repository contains four Jupyter notebooks showcasing a wide range of image processing techniques using OpenCV and NumPy. Each notebook builds on foundational concepts and demonstrates practical applications in computer vision.

---

## 📁 Contents

| Notebook | Description |
|---------|-------------|
| `1_Image_Basics_and_Drawing.ipynb` | Covers image loading, grayscale conversion, RGB channel splitting, and basic drawing (lines, rectangles, circles). |
| `2_Image_Transformations_and_Operations.ipynb` | Demonstrates translation, rotation, resizing, flipping, cropping, arithmetic and bitwise operations, masking, color space conversion, histograms, and blurring. |
| `3_Morphological_Operations.ipynb` | Explores erosion, dilation, opening, closing, gradient operations, and synthetic noise removal using morphological filters. |
| `4_Edge_Detection_and_Filtering.ipynb` | Implements Prewitt and Sobel filters manually, and applies Canny edge detection with Gaussian blurring. |

---

## 🛠️ Requirements

To run these notebooks, install the following Python packages:

```bash
pip install opencv-python numpy matplotlib imutils



🚀 How to Use
- Clone or download this repository.
- Ensure the following images are present in the working directory:
- image1.png
- colors.jpg
- rgb_image.jpg
- grayscale_image.jpg
- Open each .ipynb file in Jupyter Notebook or VS Code.
- Run the cells sequentially to view image outputs and transformations.

🎯 Key Concepts Covered
- Image loading and color space conversion
- Channel splitting and pixel inspection
- Drawing primitives (lines, rectangles, circles)
- Geometric transformations (translation, rotation, resizing)
- Bitwise and arithmetic operations
- Masking and region isolation
- Histogram plotting and analysis
- Blurring techniques (average, Gaussian, median)
- Morphological filtering (erosion, dilation, opening, closing, gradient)
- Edge detection (Prewitt, Sobel, Canny)

📎 Notes
- Visual outputs use both cv.imshow() and matplotlib.pyplot for display.
- Synthetic noise is added using NumPy to demonstrate filtering techniques.
- The imutils library simplifies resizing operations.


