# Brain-Inspired EEG-to-Spike Simulation

# Description

Inspired by biological neural systems, this project processes EEG signals into spike trains to realistically simulate neuron activity using the Brian2 framework.

---

# Project Aim

This project explores how brainwave data can be transformed into biologically meaningful spike representations and fed into a spiking neuron model. Using real EEG data, we simulate how a neuron reacts to different power levels in specific brainwave bands — especially the alpha band — by generating spike trains and observing firing behavior.

---

# 📁 Project Structure

| File                     | Description                                  |
|--------------------------|----------------------------------------------|
| `brain,_inspired.ipynb`  | Main Jupyter Notebook with the full pipeline |
| `README.md`              | Project documentation (this file)            |

---

# ⚙️ How It Works

1. **EEG Data Loading**  
   Loads EEG signals from the MNE sample dataset.

2. **Preprocessing**  
   Applies a band-pass filter (1–40 Hz) to remove noise and artifacts.

3. **Spectral Analysis (PSD)**  
   Calculates Power Spectral Density using Welch’s method, with a focus on the alpha band (8–13 Hz).

4. **Spike Encoding**  
   Normalized alpha power is converted into a rate-based binary spike train.

5. **Neuron Simulation (Brian2)**  
   The spike train is fed into a simulated neuron built using Brian2. The neuron integrates input and fires (spikes) if its membrane potential exceeds a threshold.

6. **Visualization**  
   Plots the generated spike train and visualizes neuron firing events across a 100ms time window.

---

## 🧪 Technologies & Libraries Used

- Python 3.x  
- [MNE-Python](https://mne.tools/stable/index.html) – EEG preprocessing and loading  
- [Brian2](https://brian2.readthedocs.io/en/stable/) – Neuron modeling and spike simulation  
- NumPy, SciPy, Matplotlib, Scikit-learn  
- Jupyter Notebook

---

## 🚀 How to Run

1. Clone the repository or download the `.ipynb` notebook file.
2. Install required packages:
   ```bash
   pip install mne brian2 matplotlib scipy scikit-learn
3. Open the notebook in Jupyter and run each cell step by step.
4. Observe how the EEG-based spike train influences the neuron's firing behavior
