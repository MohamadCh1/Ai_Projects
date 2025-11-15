🧭 Image Alignment Using ORB Feature Matching
This Python script aligns an input image to a template image using ORB (Oriented FAST and Rotated BRIEF) feature detection and homography transformation. It visualizes keypoint matches and overlays the aligned image on the template for comparison.

📦 Requirements
Make sure the following Python packages are installed:
pip install numpy opencv-python imutils



📁 Files
- image.jpg: The input image to be aligned.
- main.png: The template image used as reference.
- align_image.py: The main Python script.

🚀 How It Works
- Grayscale Conversion
Converts both input and template images to grayscale for feature detection.
- Feature Detection with ORB
Detects keypoints and computes descriptors using OpenCV's ORB detector.
- Feature Matching
Matches descriptors using brute-force Hamming distance and retains the top matches based on a percentage threshold.
- Homography Estimation
Computes a homography matrix using RANSAC to estimate the transformation between the input and template images.
- Image Warping
Applies the homography to warp the input image to align with the template.
- Visualization
- Displays matched keypoints if debug=True.
- Shows side-by-side comparison of aligned and template images.
- Displays a blended overlay of the aligned image and template.

🧪 Usage
Run the script from the terminal:
python align_image.py


Make sure image.jpg and main.png are in the same directory.

🔧 Parameters
You can customize the alignment behavior by modifying the following parameters in the align_image function:
- max_features: Maximum number of ORB features to detect (default: 500).
- keep_percent: Percentage of top matches to retain (default: 0.2).
- debug: Set to True to visualize keypoint matches.

🖼 Output
- Matched Keypoints: Shows ORB matches between input and template (if debug=True).
- Aligned Image: Side-by-side comparison of aligned and template images.
- Overlay: Blended visualization of alignment quality.

📌 Notes
- Ensure both images have sufficient texture and features for ORB to detect.
- Homography may fail if too few good matches are found.
- Resize operations are used for better visualization and do not affect alignment accuracy.


