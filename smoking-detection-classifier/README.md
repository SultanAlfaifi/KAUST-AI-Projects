# 🚭 Smoking Detection Classifier

Binary image classifier using Transfer Learning (ResNet-18) to detect whether a person is smoking or not.

## Overview

| | |
|---|---|
| **Task** | Binary image classification |
| **Dataset** | Smoking Dataset (Kaggle) |
| **Classes** | Smoking · Not Smoking |
| **Framework** | PyTorch + torchvision |

## Highlights

- **ResNet-18** pretrained on ImageNet, fine-tuned for binary classification
- Custom `SmokingDataset` class with label extraction from filenames
- `BCEWithLogitsLoss` with `sigmoid` thresholding at inference — numerically stable
- Separate train / validation / test splits with augmentation on train only
- Augmentations: RandomRotation(15) + ColorJitter(brightness=0.2)

## Run

```bash
pip install torch torchvision kagglehub tqdm matplotlib
python smoking_detection_classifier.py
```

## Dataset

Auto-downloaded via `kagglehub` — no manual setup needed.

---
*Developed as part of KAUST AI training program*
