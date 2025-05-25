
# PixelCNN Homework Assignment

This repository contains the implementation and experimentation for a homework assignment based on **PixelCNN**, a generative model that models the joint distribution of image pixels using conditional probabilities.

## 📘 Overview

PixelCNN is an autoregressive model designed for image generation, where each pixel is modeled as conditioned on all previously generated pixels in a raster scan order. This notebook explores:

- Sampling methods for marginal and conditional probabilities
- Masked convolutional architectures
- Evaluating and visualizing image generation

## 📂 Notebook Contents

The notebook includes the following key sections:

### 1. **Model Architecture**
- Implements a simplified version of the PixelCNN using masked convolutions.
- Uses causal filters to ensure proper autoregressive conditioning.

### 2. **Marginal and Conditional Sampling**
- Estimates marginal probability of the first pixel.
- Estimates marginal and conditional probabilities of the middle pixel (pixel 14, 14) using sampling.
- Includes both standard and Gibbs sampling approaches to account for different conditioning contexts.

### 3. **Sampling Procedures**
- Pixel-by-pixel image generation with autoregressive sampling.
- Image completions conditioned on subsets of known pixel values.

### 4. **Training and Evaluation**
- Provides evaluation metrics like Negative Log-Likelihood (NLL).
- Shows visualizations of generated and reconstructed images.

## 🛠 Requirements

This notebook assumes the following Python libraries are installed:

- `torch`
- `torchvision`
- `matplotlib`
- `numpy`

You can install them via:

```bash
pip install torch torchvision matplotlib numpy
```

## ▶️ How to Run

- Download or clone the repository.<br>
- Open the notebook (PixelCNN.ipynb) in Jupyter Notebook or Google Colab.<br>
- Run the notebook cells in sequence to:
    - Train/load the model
    - Estimate marginal/conditional probabilities
    - Generate new samples <br>

- Make sure your environment supports GPU for faster sampling and model inference.

## 📊 Sample Results

**Marginal Estimations:** 
- The notebook provides estimated probabilities for individual pixels using sampling.<br>
- **Conditional Distributions**: Demonstrates conditioning on known pixels to predict missing parts of an image.<br>
- **Gibbs Sampling**: Visualizes how iterative updates over unknown pixels can refine image generation.<br>
- **Generated Images**: Autoregressively sampled digits from the trained model on the MNIST dataset.<br>
## 📚 References
- UVA Deep Learning Course: `https://uvadlc-notebooks.readthedocs.io/en/latest/tutorial_notebooks/tutorial12/Autoregressive_Image_Modeling.html`
- Advanced Course on Deep Generative Models – Exercise 4: Auto-regressive Models
Spring 2025, Dan Rosenbaum