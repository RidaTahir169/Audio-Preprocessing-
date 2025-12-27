---

```md
# Audio Preprocessing & MFCC Feature Extraction Pipeline

This repository implements a complete **audio preprocessing and MFCC feature extraction pipeline** using **Librosa**, **NumPy**, and **Matplotlib**.  
It is suitable for speech and audio machine learning tasks.

---

## Features

- Audio loading with original sample rate
- Resampling to 16 kHz
- Peak normalization
- Silence trimming
- Pre-emphasis filtering
- MFCC feature extraction
- Waveform and MFCC visualization
- MFCC tensor creation
- Additive noise robustness test

---

## Project Structure

```

.
├── audio_preprocessing.py
└── README.md

````

---

## Configuration

| Parameter | Value |
|---------|-------|
| Target sample rate | 16000 Hz |
| MFCC coefficients | 13 |
| Silence trim threshold | 25 dB |
| FFT window size | 1024 |
| Hop length | 512 |

---

## Audio Preprocessing Pipeline

1. **Resampling**  
   Converts audio to a fixed sample rate (16 kHz)

2. **Normalization**  
   Peak normalization to scale audio between `[-1, 1]`

3. **Silence Trimming**  
   Removes leading and trailing silence

4. **Pre-Emphasis**  
   Enhances high-frequency components

---

## MFCC Feature Extraction

MFCCs are extracted using:

```python
librosa.feature.mfcc(
    y=y,
    sr=16000,
    n_mfcc=13,
    n_fft=1024,
    hop_length=512
)
````

Extracted MFCCs are aligned and stacked into a tensor of shape:

```
(num_samples, n_mfcc, time_frames)
```

---

## Output

Example console output:

```
Features Tensor Shape: (2, 13, T)
Value Range: min_value max_value
```

`T` represents the minimum number of time frames across samples.

---

## Dependencies

Install required packages:

```bash
pip install librosa numpy matplotlib
```

---

## How to Run

```bash
python audio_preprocessing.py
```

The script uses Librosa’s built-in example audio files:

* `nutcracker`
* `vibeace`

No external audio files are required.

---

## Use Cases

* Speech recognition
* Audio classification
* Speaker identification
* Noise robustness evaluation
* Deep learning audio pipelines

```

---
Just say the word.
```
