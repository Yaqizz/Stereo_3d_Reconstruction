# Stereo 3D Reconstruction from Video Frames


This project focuses on **3D surface reconstruction from stereo video frames** using classical computer vision techniques. The pipeline includes SIFT-based feature detection and matching, fundamental matrix estimation, disparity map computation, and real-world depth estimation.

---

## 📌 Key Features

- **SIFT-based Feature Detection:** Robust to scale, rotation, and illumination changes
- **Feature Matching with NNDR:** Filters strong correspondences between frames
- **Fundamental Matrix Estimation:** Via 8-point algorithm and RANSAC
- **Epipolar Constraint Filtering:** Validates matches based on epipolar geometry
- **Stereo Rectification & Disparity Map:** Computes depth using Stereo SGBM
- **3D Metric Estimation:** Calculates real-world dimensions (e.g., pool area)

---

## 🧠 Methods Overview

- Extract SIFT keypoints and descriptors for each frame
- Use k-NN + ratio test (NNDR) for robust matching
- Estimate fundamental matrix with RANSAC to filter outliers
- Rectify images using camera parameters
- Generate disparity map using `cv2.StereoSGBM`
- Convert disparities to 3D points using known baseline and focal length


