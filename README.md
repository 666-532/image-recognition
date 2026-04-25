# MNIST Image Clustering using Unsupervised Learning

## Project Overview

This project explores **unsupervised learning** techniques to cluster handwritten digit images from the MNIST dataset.
The goal is to group similar images without using labels.

The project applies **K-Means clustering** and improves clustering quality using **Principal Component Analysis (PCA)** for dimensionality reduction.

Dataset used: MNIST handwritten digit dataset.

---

## Objectives

* Understand unsupervised learning for image data
* Apply clustering algorithms on image datasets
* Evaluate clustering performance using Silhouette Score
* Visualize clusters of handwritten digits

---

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* OpenCV

---

## Dataset

The MNIST dataset contains:

* 70,000 handwritten digit images
* Image size: 28 × 28 pixels
* 10 digit classes (0–9)

Each image contains **784 pixel values** after flattening.

---

## Methodology

### Step 1: Load Dataset

The MNIST dataset was loaded using Kaggle dataset tools.

### Step 2: Data Preprocessing

* Images were normalized by dividing pixel values by 255
* Each image was flattened from 28×28 to a 784-dimensional vector

### Step 3: Dimensionality Reduction

Principal Component Analysis (PCA) was applied to reduce dimensionality.

784 features → 50 features

This improves clustering performance and reduces noise.

### Step 4: Clustering

K-Means clustering was applied to group similar images.

Cluster count tested:

* k = 3
* k = 7
* k = 10
* k = 15

### Step 5: Evaluation

Clustering performance was evaluated using the Silhouette Score.

Best result:

k = 10
Silhouette Score ≈ 0.08

Although the score is relatively low, this is common when clustering high-dimensional image data.

---

## Challenges Faced

### 1. Understanding Image Flattening

Images must be converted from 2D (28×28) to 1D vectors (784 features) before applying K-Means.

### 2. High Dimensional Data

Clustering raw pixel values resulted in poor cluster separation.

### 3. Low Silhouette Score

Initial clustering produced low silhouette scores (~0.07–0.08).

### 4. Choosing Optimal k

Different cluster counts were tested, but k=10 performed best.

---

## Solutions Implemented

### Dimensionality Reduction

PCA was applied to reduce the number of features.

This improved clustering efficiency and slightly improved silhouette scores.

### Data Normalization

Pixel values were normalized to improve distance calculations.

### Cluster Visualization

Cluster images were displayed to verify whether clusters grouped similar digits.

---

## Results

Silhouette Scores observed:

| k  | Score |
| -- | ----- |
| 3  | lower |
| 7  | lower |
| 10 | ~0.08 |
| 15 | ~0.07 |

The best clustering performance was observed at **k = 10**, which aligns with the number of digit categories.

---

## Key Learnings

* Unsupervised learning can group images without labels
* High-dimensional image data is difficult to cluster
* Dimensionality reduction is essential before clustering
* Silhouette scores for image clustering are often low

---

## Future Improvements

Possible improvements include:

* Using Autoencoders for feature extraction
* Applying Spectral Clustering
* Using CNN embeddings before clustering
* Implementing DBSCAN for density-based clustering

---

## Author

Abdullah Satti
BS Artificial Intelligence Student
