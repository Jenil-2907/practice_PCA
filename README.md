# This is for learing how PCA works practically on image compression.

## Overview
This project demonstrates Principal Component Analysis (PCA) for compressing and reconstructing face images from a dataset of 39 images (64x64 pixels each).

## How PCA Works Here

1. **Data Preparation**:
   - Images are loaded and flattened into vectors (4096 dimensions each)
   - Data is centered by subtracting the mean face

2. **PCA Process**:
   - Computes covariance matrix of the centered data
   - Performs eigenvalue decomposition to get eigenvectors/values
   - Selects top 20 principal components (eigenvectors)

3. **Dimensionality Reduction**:
   - Projects original data onto these 20 components
   - Reduces data from 4096D to just 20D while preserving key features

4. **Reconstruction**:
   - Uses the reduced data and principal components to approximate original images
   - Shows comparison between original and reconstructed versions

## Key Observation
The reconstructed images maintain many facial features despite using only 20 components (99.5% data reduction),
for best result I would recommend taking k around 25-28.

## Requirements
- Python 3
- NumPy
- OpenCV
- Matplotlib
