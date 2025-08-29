# 🧠 Epileptic Seizure Detection using EEG (FFT + ML)

##  Project Overview

This project focuses on **classifying epileptic seizures using EEG signals**. Instead of going fully into advanced deep learning, I used a **signal processing + machine learning approach** for better interpretability and simplicity.

The project demonstrates how **Fast Fourier Transform (FFT)** can be used to extract frequency features from EEG signals, which are then classified using **Logistic Regression** and **Random Forest** models.

##  What is Epilepsy?

Epilepsy is a neurological disorder where brain activity becomes abnormal, leading to seizures.

* Seizures are sudden surges of electrical activity in the brain.
* Detecting epilepsy early using EEG (Electroencephalogram) signals can significantly improve patient care.

  
## 📊 Dataset

The dataset is taken from the **UCI Epileptic Seizure Recognition Dataset**.

* Each EEG signal consists of **178 data points** (1-second recording).
* Labels are binary:

  * **1 → Seizure activity**
  * **0 → No seizure activity**
 

     
##  Tech Stack

* **Python**
* **Numpy, Pandas** (Data handling)
* **Matplotlib, Seaborn** (Visualization)
* **Scikit-learn** (ML models)
* **FFT (Numpy)** for frequency feature extraction
  

##  Methodology

1. **Exploratory Data Analysis (EDA)**

   * Visualized EEG signals for seizure vs. non-seizure.
   * Found that seizures often show **dominance of low-frequency components**.

2. **Baseline Models**

   * **Logistic Regression** and **Random Forest** trained directly on raw signals.
   * Results showed seizure class was harder to detect with raw features.

3. **FFT Feature Extraction**

   * Transformed EEG signals from the **time domain → frequency domain** using FFT.
   * Used frequency amplitudes as new features.

4. **Classification on FFT Features**

   * Applied Logistic Regression and Random Forest again.
   * Accuracy and F1-score improved significantly after FFT.


## 📈 Results

### Baseline (Raw Signals)

* Logistic Regression → **80% accuracy** but seizure class (1) almost missed.
* Random Forest → **86% accuracy**, seizure detection recall improved but still weak.

### FFT Features (Frequency Domain)

* Logistic Regression → **95% accuracy**, seizure class detected much better.
* Random Forest → **96% accuracy**, strong performance overall.

 **Conclusion**: FFT-based frequency features outperform raw signal features for seizure detection.


## Key Learnings

* Epileptic EEG signals are dominated by **low-frequency components**.
* Simple ML models + FFT can match/exceed deep learning accuracy for structured data.
