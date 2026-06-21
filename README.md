# Network Traffic Prediction using Time-Series-to-Image Learning

## Overview

This project explores a novel approach for network traffic prediction by transforming traffic matrix time-series data into image representations and applying deep learning models for forecasting.

Traditional traffic prediction models operate directly on numerical traffic matrices. This implementation investigates image-based learning, enabling powerful feature extraction through computer vision architectures such as:

- AlexNet
- ResNet + CNN
- Vision Transformer (ViT)
- LSTM
- Bi-LSTM
- GRU
- Bi-GRU

The objective is to improve prediction accuracy by leveraging spatial and temporal relationships captured through image representations.

---

## Features

- Traffic Matrix → Image Conversion
- Image Feature Extraction
- CNN-Based Learning
- Vision Transformer Integration
- LSTM and GRU Forecasting Models
- Performance Evaluation using:
  - MSE
  - RMSE
  - MAE

---

## System Architecture

Traffic Matrix Data
        ↓
Image Conversion
        ↓
Feature Extraction
(AlexNet / ResNet / ViT)
        ↓
Sequence Learning
(LSTM / GRU / Bi-LSTM / Bi-GRU)
        ↓
Traffic Prediction

---

## Image Conversion Techniques

### 1. Normalization + Inversion

Traffic matrices are:

- Normalized to [0,1]
- Converted into grayscale images
- Inverted to improve feature activation

### 2. Difference-Based Transformation

Consecutive traffic matrices are:

- Subtracted
- Passed through a sigmoid function
- Converted into pixel values (0–255)

This highlights traffic pattern changes over time.

---

## Models Implemented

### Feature Extractors

- AlexNet
- ResNet + CNN
- Vision Transformer (ViT)

### Prediction Models

- LSTM
- Bi-LSTM
- GRU
- Bi-GRU

---

## Dataset

The implementation supports commonly used network traffic datasets such as:

- GEANT Dataset
- Abilene Dataset

Dataset structure should contain traffic matrices collected over time.

---

## Project Structure

```bash
project/
│
├── data/
│   ├── raw/
│   ├── processed/
│
├── image_conversion/
│   ├── normalization.py
│   ├── difference_based.py
│
├── models/
│   ├── alexnet.py
│   ├── resnet_cnn.py
│   ├── vit.py
│   ├── lstm.py
│   ├── gru.py
│
├── training/
│   ├── train.py
│
├── evaluation/
│   ├── metrics.py
│
├── results/
│
├── requirements.txt
│
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/network-traffic-prediction.git

cd network-traffic-prediction
```

### Create Virtual Environment

```bash
python -m venv venv
```

Activate:

```bash
source venv/bin/activate
```

or

```bash
venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Training

```bash
python train.py
```

---

## Evaluation Metrics

The model is evaluated using:

### Mean Squared Error (MSE)

```math
MSE = (1/n) Σ(y - ŷ)^2
```

### Root Mean Squared Error (RMSE)

```math
RMSE = √MSE
```

### Mean Absolute Error (MAE)

```math
MAE = (1/n) Σ|y - ŷ|
```

---

## Results

The image-based approach demonstrates improved feature extraction and prediction capability compared with conventional traffic matrix forecasting methods.

Performance is evaluated on:

- GEANT Network Dataset
- Abilene Network Dataset

using MSE, RMSE, and MAE metrics.

---

## Future Improvements

- Multi-modal learning
- Advanced transformer architectures
- Traffic anomaly detection
- Real-time deployment
- Edge AI integration
- Network congestion forecasting

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- OpenCV
- Matplotlib

---

## Disclaimer

This repository is an implementation inspired by academic research in network traffic prediction. The original paper and datasets belong to their respective authors and publishers.

---

## Author
Mansi Gupta
Under guidance of Dr. Kriti (Assistant Professor, Amity University Punjab)
