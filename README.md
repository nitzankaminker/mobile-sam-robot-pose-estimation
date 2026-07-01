# MobileSAM Robot Pose Estimation

## Project Overview

This project investigates the use of MobileSAM (Segment Anything Model) as a preprocessing stage for accurate robot pose estimation.

Instead of estimating the robot orientation directly from the original RGB image, the pipeline first extracts the robot contour using MobileSAM segmentation. The resulting contour representation is then used for pose estimation, reducing background noise and emphasizing the geometric information required for angle prediction.

---

## Project Objective

The goal of this project was to improve robot orientation estimation by using object contours rather than raw images.

The segmentation stage isolates the robot from the background, allowing the pose estimation model to focus only on the relevant object geometry.

---

## Pipeline

```mermaid
flowchart TD

A[Input Robot Image]
--> B[MobileSAM Segmentation]

B --> C[Extract Robot Contour]

C --> D[Pose Estimation Model]

D --> E[Predicted Robot Angle]
```

---

## Methodology

The project follows four main stages:

1. Load robot images.
2. Generate segmentation masks using MobileSAM.
3. Extract contour representations of the segmented robot.
4. Train a deep learning model to estimate the robot orientation from the contour images.

The notebook also includes visualization of the generated contours together with the complete training process.

---

## Results

The notebook demonstrates:

- Robot contour extraction using MobileSAM.
- Visualization of contour images.
- Training and validation loss curves.
- Stable convergence of the optimization process during training.
- Accurate robot angle estimation from contour-based representations.

---

## Technologies

- Python
- PyTorch
- MobileSAM
- OpenCV
- NumPy
- Matplotlib

---

## Skills Demonstrated

- Computer Vision
- Deep Learning
- Foundation Models
- Segment Anything Model (SAM)
- MobileSAM
- Image Segmentation
- Contour Extraction
- Robot Pose Estimation
- PyTorch
- Model Training
