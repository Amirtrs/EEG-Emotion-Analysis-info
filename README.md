# EEG-Emotion-Analysis-info
EEG Signal Processing and Emotion Classification with EEGLAB : MATLAB project for EEG feature extraction, topographic mapping, and affective state classification.


# EEG Analysis and Emotion Recognition Using EEGLAB

This repository contains MATLAB code integrated with EEGLAB for analyzing EEG data, extracting features, and performing emotion classification. The project processes EEG data with advanced preprocessing and visualization techniques, utilizing EEGLAB for topographic mapping, frequency band analysis, and signal filtering.

## Project Features

### Data Loading and Organization
- Loads EEG data from `.mat` files.
- Organizes data into structures for trials, channels, and labels.

### Preprocessing with EEGLAB
- Imports EEG data into EEGLAB structures.
- Assigns channel locations based on the 10-20 system.
- Filters EEG signals for frequency bands:
  - **Theta (4-8 Hz)**
  - **Alpha (8-12 Hz)**
  - **Beta (12-30 Hz)**
  - **Gamma (30-64 Hz)**

### Feature Extraction
1. **Power Spectral Density (PSD)**:
   - Computes PSD for each frequency band using Welch’s method.
   - Extracts topographic maps for frequency power distribution.
2. **Band Power Calculation**:
   - Calculates band-specific power for individual channels.
   - Normalizes power values for visualization.
3. **Descriptive Statistics**:
   - Extracts median, mean, and variance for affective labels (Valence and Arousal).

### Visualization
- **Topographic Maps**:
  - Generates maps for Theta, Alpha, Beta, and Gamma bands.
  - Displays dynamic maps for different time points within trials.
- **EEG Signal Plots**:
  - Visualizes raw signals and their corresponding PSD.
- **Channel Group Analysis**:
  - Segments EEG channels into regions (e.g., Frontal, Parietal, Occipital) for regional analysis.

### Classification
- Categorizes trials into:
  - **High/Low Valence**
  - **High/Low Arousal**
- Implements KNN classification for Valence and Arousal prediction.
- Evaluates models with metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-Score

### Output
- Classification results stored in `results.xlsx`.
- Topographic maps and signal visualizations generated for each frequency band.

---

## Getting Started

### Prerequisites
1. MATLAB with the following toolboxes:
   - Signal Processing Toolbox
   - Statistics and Machine Learning Toolbox
2. **EEGLAB**:
   - Download and install the latest version of [EEGLAB](https://sccn.ucsd.edu/eeglab/index.php).

### Dataset Setup
1. Place EEG `.mat` files in a directory (e.g., `data_preprocessed_matlab`).
2. Ensure each file follows the naming convention:
   - `s01.mat`, `s02.mat`, ..., `s32.mat`.

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Amirtrs/EEGLAB-EEG-Analysis.git
