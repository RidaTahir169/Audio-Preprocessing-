Speech Preprocessing
Overview
This project demonstrates a basic speech and audio preprocessing pipeline using Librosa, NumPy, and Matplotlib.
It loads example audio files provided by Librosa, applies common preprocessing steps, extracts Mel-Frequency Cepstral Coefficients (MFCCs), visualizes intermediate results, and performs a simple noise experiment.

The code is designed for educational purposes and as a foundation for speech recognition or audio-based machine learning workflows.

Features
Load built-in Librosa audio samples
Resample audio to a fixed sampling rate (16 kHz)
Normalize audio amplitude
Trim silence from audio signals
Apply smoothing using a moving average filter
Visualize raw and processed waveforms
Extract and visualize MFCC features
Combine MFCCs into a single feature tensor
Add synthetic noise for robustness testing
Requirements
Python Version
Python 3.8 or higher
Dependencies
Install the required libraries using pip:

pip install librosa numpy matplotlib
