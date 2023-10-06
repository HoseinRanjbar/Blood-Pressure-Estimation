# Blood-Pressure-Estimation
Blood Pressure Estimation from PPG Signals Using Machine Learning

## Introduction

In today's healthcare landscape, the continuous and non-invasive monitoring of blood pressure is of paramount importance, given its role as a critical indicator of cardiovascular health. This repository explores the intersection of photoplethysmography (PPG) signals and blood pressure estimation.
By delving into the intricacies of PPG signals, signal processing techniques, and machine learning algorithms, we aim to bridge the gap between these signals and accurate blood pressure measurements, ultimately contributing to a future where unobtrusive and continuous blood pressure monitoring enhances patient comfort and healthcare outcomes.
There is a relationship between PPG signals and blood pressure, and below, this relationship is demonstrated:

<p align="center">
  <img src="./Images/ppg-bp.png" width="300" >
</p>

# Dataset: 

The dataset can be found in the **./datasets**.


# Phase 1

The goal in Phase 1 is to estimate blood pressure from segmented PPG signals. In below segmented PPG signals are shown:

<p align="center">
  <img src="./Images/ppg_phase1.png" width="1000" >
</p>

## The following steps are executed in the **blood_pressure_estimation_phase1.ipynb**:

1- Loading datasets: load **s1_train.npy** and **s1_test.npy**.

2- Preprocessing: Normalization - Elimination of short signals

3- Base line model: Use average for base line model

4- Upsampling: Set length of signals to 200ms

5- Defining and training a linear regression model, followed by making predictions on a test dataset

6- We define and train a ridge regression model, and then proceed to utilize it for making predictions on a test dataset.

7- Defining and training a lasso model, followed by using it to make predictions on a test dataset.

# Phase 2

In phase2, we are going to get a little closer to the real issue. For this purpose, we have 50 training data samples available in the 's2_train.np' file. Each sample includes the PPG signal of a patient along with the corresponding blood pressure signal. These signals were sampled at a frequency of 125 Hz and captured over a duration of 8 to 10 minutes. In this section, the objective is to design a system for estimating blood pressure from the PPG signal. To accomplish this, you need to extract both the training samples of the PPG signal and the corresponding blood pressure values from the provided signals. To do so, The follow steps are executed in the **blood_pressure_estimation_phase1.ipynb**:

1- Loading datasets: load **s2_train.npy** and **s2_test.npy**. In below a PPG signal is shown:

<p align="center">
  <img src="./Images/ppg_phase2.png" width="1000" >
</p>


2- Preprocessing: Normalization - Elimination of short signals

3- Identifying the systolic and diastolic points within the signal.

3- Base line model: Calculate Systolic & Diastolic average for base line model.

5- Upsampling: Set length of signals to 2000ms.

6- Defining and training a linear regression model, followed by making predictions on a test dataset.

7- We define and train a ridge regression model, and then proceed to utilize it for making predictions on a test dataset.

8- Defining and training a lasso model, followed by using it to make predictions on a test dataset.
