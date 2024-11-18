HRV Analysis Using ECG Signals
Overview

This project analyzes Heart Rate Variability (HRV) from ECG signals, specifically using Record 100 from the MIT-BIH Arrhythmia Database. The main tasks performed in this project include:

    Signal Preprocessing: Filtering and noise removal.
    R-Peak Detection: Using wavelet transform.
    HRV Computation: Time-domain and frequency-domain analysis.
    Heart Rate Calculation: Based on RR intervals.
    Visualization: ECG signals, HRV metrics, and power spectral density (PSD).

This project is aimed at providing insights into cardiac health and autonomic nervous system function.
Objectives

    Primary Objective: Analyze ECG signals to extract HRV metrics for assessing autonomic nervous system function.
    Sub-objectives:
        Apply filtering to remove noise and artifacts from ECG data.
        Detect R-peaks using wavelet transform.
        Calculate HRV metrics like SDNN, RMSSD, LF/HF ratio, and perform frequency-domain analysis (PSD).
        Calculate heart rate from RR intervals and visualize HRV trends.

Dataset

    Dataset: MIT-BIH Arrhythmia Database (Record 100)
    Sampling Frequency: 360 Hz
    Annotations: Expert-labeled R-peak locations and beat classifications.

Methodology

    Data Loading and Preprocessing:
        The ECG signal is loaded using the wfdb library.
        A bandpass filter is applied to remove baseline wander and high-frequency noise.

    R-Peak Detection:
        Wavelet transform (using the 'db4' wavelet) is applied to extract R-peaks.

    HRV Metric Computation:
        Time-domain HRV metrics like SDNN and RMSSD are computed.
        Frequency-domain HRV analysis using Power Spectral Density (PSD) and Fast Fourier Transform (FFT).

    Heart Rate Calculation:
        Instantaneous heart rate is derived from RR intervals.

    Visualization:
        Visualizations include the raw ECG, filtered ECG, R-peaks, and HRV metrics.

Requirements

    Python 3.x
    Required libraries:
        numpy
        matplotlib
        wfdb
        pywt
        scipy
        pandas

Install the required libraries with:

pip install numpy matplotlib wfdb pywt scipy pandas

How to Run the Project

    Clone the repository:

git clone https://github.com/yourusername/hrv-analysis.git
cd hrv-analysis

Run the analysis script:

    python hrv_analysis.py

    View the visualizations and check the hrv_results.csv file for computed metrics.

Results

    Time-domain HRV metrics:
        SDNN (Standard Deviation of NN intervals)
        RMSSD (Root Mean Square of Successive Differences)
    Frequency-domain HRV metrics:
        LF (Low Frequency) Power
        HF (High Frequency) Power
        LF/HF Ratio
    Heart Rate (BPM) calculated from RR intervals.

Output

The results of the analysis are saved in hrv_results.csv, and visualizations are saved as PNG images.
