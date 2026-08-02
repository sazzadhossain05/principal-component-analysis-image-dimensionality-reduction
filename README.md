# Principal Component Analysis for Image Dimensionality Reduction

## Overview
This project implements Principal Component Analysis (PCA) from scratch for dimensionality reduction on handwritten digit images. 

## Dataset
The project uses the Digits dataset from scikit-learn, which contains 1,797 grayscale images of handwritten digits (0-9), each of size 8x8 pixels. Each image is represented as a vector of 64 pixel values.

## Methods
The PCA pipeline was implemented manually using the following steps:

1. **Data Loading and Reshaping** — loaded the Digits dataset and flattened each 8x8 image into a 64-dimensional vector, forming a matrix with samples in rows and pixel values in columns.
2. **Mean Subtraction** — computed and subtracted the mean of each feature across all samples to center the data.
3. **Covariance Matrix Computation** — computed the covariance matrix of the transposed image matrix to capture feature-level variance.
4. **Singular Value Decomposition (SVD)** — applied SVD to the covariance matrix to obtain the eigenvector matrix U, representing the principal components.
5. **Dimensionality Reduction** — selected the top r eigenvectors such that 99% of the total variance is preserved, and projected the original data onto the reduced space.
6. **Reconstruction and Visualization** — reconstructed and plotted digit images in the reduced dimension space to verify the quality of the approximation.

## Tools and Libraries
- Python 3
- NumPy
- SciPy (SVD)
- Matplotlib
- scikit-learn (dataset loading)
- Jupyter Notebook

## Files
- `plot_digits_last_image.ipynb` — main Jupyter notebook with full PCA implementation and visualizations
- `plot_digits_last_image.py` — Python script version of the implementation
- `bonus assignment/Untitled.ipynb` — working notebook used during development
- `solution/` — final submitted report in PDF and DOCX formats
- `Bonus Assignment.pdf` — original assignment question provided by the instructor

## Results
The number of principal components required to preserve 99% of the variance was identified and used to reconstruct digit images with minimal loss of visual information. The reduced-dimension images were plotted alongside the originals to demonstrate the effectiveness of PCA for image compression and dimensionality reduction.


