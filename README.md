# Air Quality PDF Estimation

Dataset: Consider NO2 as feature (x).
Link: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

This project implements Assignment-1: Learning Probability Density Functions using Roll-Number-Parameterized Non-Linear Models. It processes air quality data ($NO_2$), applies a custom non-linear transformation, and fits a Gaussian-style PDF to the resulting distribution.

# Project Overview

The objective is to take a feature $x$ ($NO_2$ levels), apply a non-linear transformation $z$ based on a specific University Roll Number, and then estimate the parameters $(\lambda, \mu, c)$ for the following model:

<img width="227" height="54" alt="Screenshot 2026-02-05 at 12 15 36 AM" src="https://github.com/user-attachments/assets/06710ebf-72a7-40a7-801a-c7f032a19a2b" />

# Implementation Details

1. Data Transformation

   Based on the roll number ($r = 102317203$), the following transformation parameters were calculated:
<img width="484" height="208" alt="Screenshot 2026-02-05 at 12 17 05 AM" src="https://github.com/user-attachments/assets/f1ea6244-245e-4133-93a2-e56c85bf92c1" />

2. Parameter Estimation
The parameters were learned using non-linear least squares (scipy.optimize.curve_fit) to match the histogram of the transformed data.

# Results
Based on the latest execution, the model learned the following parameters:

<img width="279" height="146" alt="Screenshot 2026-02-05 at 12 17 56 AM" src="https://github.com/user-attachments/assets/17956620-6379-4cb4-9a15-681b01d53090" />

# Visualization

The plot below shows the histogram of the transformed $z$ values overlaid with the learned probability density function curve.

<img width="866" height="550" alt="Screenshot 2026-02-05 at 12 19 09 AM" src="https://github.com/user-attachments/assets/92eee129-a449-4a79-ac69-1faff7007e3a" />
