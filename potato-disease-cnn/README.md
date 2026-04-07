# 🥔 Potato Disease Classification using CNN

A PyTorch CNN trained from scratch to classify potato leaf diseases from the PlantVillage dataset.

## Overview

| | |
|---|---|
| **Task** | Multi-class image classification |
| **Dataset** | PlantVillage — Potato leaves |
| **Classes** | Early Blight · Late Blight · Healthy |
| **Framework** | PyTorch |

## Highlights

- **CNN built from scratch** with 5 convolutional layers + BatchNormalization
- **Residual (skip) connection** from layer 2 → layer 4 with dimension matching via 1×1 conv
- Data augmentation (RandomRotation) applied only on training set
- Training & validation loss/accuracy curves plotted per epoch

## Model Architecture

```
Input (3×32×32)
  → Conv1 + BN + ReLU + MaxPool  →  (16×16×16)
  → Conv2 + BN + ReLU + MaxPool  →  (32×8×8)   ─── skip ───┐
  → Conv3 + BN + ReLU + MaxPool  →  (64×4×4)               │
  → Conv4 + BN + ReLU + MaxPool  →  (128×2×2) ←── + skip ──┘
  → Conv5 + BN + ReLU + MaxPool  →  (256×1×1)
  → FC(512) → FC(3)
```

## Results

| Model | Best Val Accuracy |
|---|---|
| CNN (no skip) | 98.61% |
| CNN + Residual | 97.22% |

> 10 epochs · Adam · lr=0.001 · input 32×32

## Run

```bash
pip install torch torchvision kagglehub tqdm matplotlib
python potato_disease_classification_using_cnn.py
```

## Dataset

Auto-downloaded via `kagglehub` — no manual setup needed.

---
*Developed as part of KAUST AI training program*
