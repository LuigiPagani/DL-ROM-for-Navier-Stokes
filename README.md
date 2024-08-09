# Deep Learning-Based Reduced Order Modeling for Navier-Stokes Equations

Welcome to the repository dedicated to developing and applying Deep Learning-based Reduced Order Models (DL-ROMs) for efficiently solving the Navier-Stokes equations. This project is part of the Numerical Analysis for Machine Learning course at Politecnico di Milano for the academic year 2023/2024.

## Project Overview

This repository explores the application of DL-ROMs to the Navier-Stokes equations, which are fundamental in fluid dynamics. The main objective is to leverage deep learning, specifically autoencoders, to reduce the dimensionality of high-dimensional Partial Differential Equation (PDE) solutions and significantly cut down computational costs while maintaining accuracy.

## Contents

- **DL_ROM.ipynb**: A Jupyter notebook that implements the DL-ROM methodology for the Navier-Stokes boundary value problem, showcasing the process from data generation to model training and evaluation.
- **NAML_Report.pdf**: A detailed report that provides an in-depth explanation of the DL-ROM approach, the architecture used, the application to the Navier-Stokes problem, and a comparison of accuracy and computational efficiency with traditional methods.

## Key Concepts

### 1. **Deep Learning-Based Reduced Order Models (DL-ROMs)**
DL-ROMs are fully data-driven approaches designed to approximate the solution of parameterized PDEs using deep learning architectures, particularly autoencoders. The goal is to create a low-dimensional representation of the PDE solutions, reducing computational requirements without compromising the accuracy of the results.

### 2. **Navier-Stokes Boundary Value Problem**
The Navier-Stokes equations, which describe fluid flow, serve as the primary application for the DL-ROM developed in this project. The challenge lies in the equations' nonlinear nature and the wide range of scales in fluid flow, making them an ideal case study for reduced-order modeling.

### 3. **Neural Network Architecture**
The DL-ROM consists of two main components:
- **Autoencoder**: Reduces the dimensionality of the high-fidelity solution space.
- **Feed-Forward Neural Network (FFNN)**: Maps the input parameters to the latent space, incorporating Fourier features to capture periodic patterns in the data.

### 4. **Training and Evaluation**
The model was trained using a dataset of 41 trajectories with different parameter sets. The training process involved optimizing the autoencoder to minimize reconstruction error and the FFNN to accurately map the parameters to the reduced latent space.

### 5. **Performance and Comparisons**
The DL-ROM was evaluated against a traditional Finite Element Method (FEM) solver, demonstrating a significant speedup (up to 3.21×10^5) with a relative error of just 1.66%. These results highlight the efficiency and accuracy of the DL-ROM approach, particularly for high-dimensional, non-linear systems.


## Conclusion

This project demonstrates the potential of deep learning in reducing the computational complexity of solving high-dimensional PDEs, particularly in fluid dynamics. The DL-ROM approach offers a powerful alternative to traditional methods, with significant speedups and high accuracy, making it a valuable tool in both academic research and practical applications.

## Getting Started

To run the notebooks, it is highly recommended to open them in Google Colab using the button provided at the beginning of each Jupyter notebook.
