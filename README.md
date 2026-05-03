# Human Scream Detection | Audio Classification using Deep Learning

![ML](https://img.shields.io/badge/Machine%20Learning-Audio-blue)
![DeepLearning](https://img.shields.io/badge/Deep%20Learning-CNN-orange)
![Python](https://img.shields.io/badge/Python-Model-yellow)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---
## Project Overview

Built a machine learning system to detect human scream sounds from audio data.

The system processes audio files, extracts features like MFCC and spectrograms, and classifies sounds as scream or non scream using deep learning models.

Designed for safety monitoring and alert based systems.

---

## 🔍 Features

- Binary audio classification: scream vs non-scream  
- Preprocessed audio samples using MFCC features  
- CNN-based model architecture  
- Real-time and batch audio file inference capability  
- Configurable training and evaluation parameters  
- Simple file-based prediction pipeline  

---
## Architecture

```id="f6k2ps"
Audio Input → Feature Extraction (MFCC, Spectrogram) → CNN Model → Classification Output (Scream / Non Scream)
```

## 📁 Project Structure

```
scream-detection/
├── fileinfo.py                             # Utility for reading file metadata
├── modelloader.py                          # Loads and initializes the model
├── negative/                               # Folder containing non-scream audio
├── requirements.txt                        # Python dependencies
├── resources/                              # Additional media or assets
├── saved_model.pb                          # Saved TensorFlow model
├── sound_classifier_nueral.py              # Main classifier code
├── testing/                                # Folder with test audio files
├── ui.kv                                   # Kivy UI layout file

```

---

## ⚙️ Installation

1. Clone the repository:  
   `https://github.com/kd-abhidev/Human-scream-detection.git`  
   `cd Human-scream-detection`

2. Create a virtual environment (optional but recommended):  
   `python -m venv venv`  
   `source venv/bin/activate` (on Windows: `venv\Scripts\activate`)

3. Install dependencies:  
   `pip install -r requirements.txt`

---
## Workflow

1. Load audio dataset
2. Extract MFCC and spectrogram features
3. Train CNN model
4. Save trained model
5. Run inference on test audio
6. Classify as scream or non scream

---


## 🧪 Usage

### 1. Dataset Preparation

- Place your audio samples into the appropriate directories:
  - `negative/` for non-scream sounds
  - Create a similar directory (e.g. `positive/`) if using your own scream samples
- Use `datasetmaker.py` to process and prepare the dataset.

### 2. Model Loading & Inference

- The trained model is saved in `saved_model.pb`.
- Use `modelloader.py` to load the model.
- Run `sound_classifier_nueral.py` to perform classification on audio inputs.  
  This script uses the loaded model to analyze and predict whether an input sound is a scream or not.

### 3. Testing

- Use the `testing/` directory to store your test audio clips.
- Run the classification scripts on these samples to evaluate the model's performance.

---

## 📊 Evaluation

The model is evaluated based on:

- Accuracy  
- Precision and Recall  
- F1 Score  
- Confusion Matrix  

Evaluation metrics can be found in the logs or generated via the test script after training.

---

## Academic Project

This application was developed as part of an academic project.
The system was designed and implemented collaboratively by the following team members.

- Abhidev K D, UI Development
- Arjun K M, Backend Development
- Athul N A, Machine Learning
- Aswin T, Integration and Data Processing
- Ajay S, Integration and Data Processing

---

## 🎥 Examples

Below are example outputs for scream and non-scream audio predictions:

### ✅ Positive Prediction (Scream Detected)

![Positive Example](./examples/positive.gif)

### ❌ Negative Prediction (No Scream Detected)

![Negative Example](./examples/negative.gif)

---


## Use Cases

* Safety monitoring systems
* Public surveillance
* Emergency detection
* Smart alert systems

---

## Challenges Solved

* Processed raw audio into usable features
* Tuned CNN model for better accuracy
* Handled noise and non scream sounds
* Built prediction pipeline for testing

---

## Future Improvements

* Improve dataset size and diversity
* Add real time streaming detection
* Deploy as API service
* Integrate with alert system

