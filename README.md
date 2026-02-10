# Automatic ECG Analysis Using Deep Learning

## Overview
This project performs automatic analysis of ECG (Electrocardiogram) signals using a deep neural network. The model processes 12-lead ECG signals and predicts multiple cardiac abnormalities, helping in early detection of heart rhythm disorders.

The system is based on a residual deep neural network architecture designed to classify different heart conditions from raw ECG signals.

---

## Key Features
- 12-lead ECG signal processing
- Deep learning–based classification
- Multi-label prediction of heart abnormalities
- Automated training and prediction pipeline
- Result visualization and output generation

---

## Predicted Heart Conditions
The model predicts probabilities for the following six abnormalities:

1. First-degree AV block (1dAVb)
2. Right bundle branch block (RBBB)
3. Left bundle branch block (LBBB)
4. Sinus bradycardia (SB)
5. Atrial fibrillation (AF)
6. Sinus tachycardia (ST)

---

## Tech Stack
- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Deep Learning (Residual Neural Network)

---

## Project Structure
```
ECG-ANALYSIS-USING-ML/
│
├── data/                     # ECG datasets
├── dnn_predicts/             # Model prediction outputs
├── outputs/                  # Generated figures and tables
│
├── datasets.py               # Dataset loading utilities
├── model.py                  # Neural network architecture
├── train.py                  # Training script
├── predict.py                # Prediction script
├── generate_figures_and_tables.py
├── requirements.txt          # Dependencies
└── README.md
```

---

## Model Details
- **Input shape:** (4096, 12)  
  - 4096 ECG signal points  
  - 12 leads
- **Output shape:** (6,)  
  - Probability for each abnormality
- **Architecture:** Residual deep neural network
- **Framework:** TensorFlow 2.x

---

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/akshaysharma2703/ECG-ANALYSIS-USING-ML.git
cd ECG-ANALYSIS-USING-ML
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

---

## Training the Model
```bash
python train.py PATH_TO_HDF5_DATA PATH_TO_LABEL_CSV
```

---

## Running Predictions
```bash
python predict.py PATH_TO_ECG_DATA PATH_TO_MODEL --output_file results.csv
```

---

## Generating Figures and Tables
```bash
python generate_figures_and_tables.py
```
Outputs will be saved in the `outputs/` folder.

---

## Applications
- Early detection of heart rhythm disorders
- Clinical decision support systems
- Automated ECG interpretation
- Remote cardiac monitoring

---

## Future Improvements
- Real-time ECG signal analysis
- Web or mobile deployment
- Integration with wearable devices
- Model explainability features

