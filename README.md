\documentclass[12pt]{article}
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage{hyperref}

\begin{document}

% Title
\title{\textbf{From Pixels to 3D Worlds: Two-View 3D Reconstruction}}
\author{}
\date{}
\maketitle

% Introduction
\section*{Introduction}
This project demonstrates the process of reconstructing a 3D view of a scene using two images captured from different perspectives. By matching features between the images and applying linear algebra and computer vision techniques, we achieve Two-View 3D Reconstruction. This simplified approach is a subset of Structure from Motion (SfM) and enables us to determine the camera's pose relative to the reconstructed scene.

\section*{Pipeline Overview}
\begin{enumerate}
    \item \textbf{Feature Matching}  
    Visualize and extract matching feature points between two images using provided correspondence data.
    
    \item \textbf{Fundamental Matrix Estimation and RANSAC}  
    Use matched points to compute the Fundamental Matrix. Apply RANSAC for outlier rejection, ensuring robust estimation.
    
    \item \textbf{Essential Matrix Estimation}  
    Compute the Essential Matrix using camera intrinsic matrices and the Fundamental Matrix.
    
    \item \textbf{Camera Pose Extraction}  
    Extract possible camera poses (rotation and translation) from the Essential Matrix.
    
    \item \textbf{Linear Triangulation}  
    Estimate 3D points by triangulating the matched features across both images.
    
    \item \textbf{Cheirality Condition}  
    Validate the 3D points and select the correct camera pose based on the chirality condition.
\end{enumerate}

\end{document}
