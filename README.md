# Two-View 3D Reconstruction

## Introduction
This project demonstrates reconstructing a 3D view of a scene using two images captured from different perspectives. This is a simplified approach of Structure from Motion (SfM) used to determine the camera's pose relative to the reconstructed scene.

## Pipeline Overview
1. **Feature Matching**  
   Visualize and extract matching feature points between two images using provided correspondence data.
   
2. **Fundamental Matrix Estimation and RANSAC**  
   Use matched points to compute the Fundamental Matrix. Apply RANSAC for outlier rejection.
   
3. **Essential Matrix Estimation**  
   Compute the Essential Matrix using camera intrinsic matrices and the Fundamental Matrix.
   
4. **Camera Pose Extraction**  
   Extract possible camera poses (rotation and translation) from the Essential Matrix.
   
5. **Linear Triangulation**  
   Estimate 3D points by triangulating the matched features across both images.
   
6. **Cheirality Condition**  
   Validate the 3D points and select the correct camera pose based on the chirality condition.
