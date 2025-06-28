# Audio-Emotion-Detection

This project extracts rich, handcrafted audio features from the **RAVDESS dataset** to enable tasks like **speech emotion recognition**. It combines **librosa**, **OpenSMILE**, and statistical analysis to generate over **690 features per audio file**.

---

## 📁 Dataset

We use the [RAVDESS] dataset, a well-structured emotional speech/audio dataset:

## ⚙️ Features Extracted

- **MFCCs** (with deltas + delta-deltas)
- **Spectral features**: centroid, contrast, bandwidth, rolloff, flatness
- **Prosodic features**: RMS, F0 dynamics
- **Voice quality**: jitter, shimmer, HNR (via OpenSMILE)
- **Perceptual features**: Chroma, Tonnetz
- **Temporal dynamics**: velocity/acceleration for MFCCs, RMS, spectral
- **Statistical descriptors**: mean, std, min, max, median, skew, kurtosis

Total: **~693 features per file**

## 🚀 How It Works

1. **Load & preprocess WAV files**
2. **Extract features** using Librosa + OpenSMILE
3. **Aggregate statistics**
4. **Normalize** with `StandardScaler`
5. **Save** `.npy` files for features, labels, and scaler

---

