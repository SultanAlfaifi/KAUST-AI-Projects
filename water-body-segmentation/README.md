# 🛰️ Water Body Segmentation from Satellite Imagery

Fine-tuning a U-Net to detect and segment water bodies in satellite images using binary semantic segmentation.

## Overview

| | |
|---|---|
| **Task** | Binary semantic segmentation |
| **Dataset** | Satellite Images of Water Bodies (Kaggle) |
| **Classes** | Water · Non-Water |
| **Framework** | PyTorch + segmentation-models-pytorch |

## Highlights

- **U-Net** with **EfficientNet-B1** encoder pretrained on ImageNet
- Custom `WaterBodyDataset` with 85/15 train/val split
- **Mean IoU** tracked alongside loss — standard metric for segmentation
- Mask binarization from grayscale (0/255 → 0/1)
- NEAREST interpolation for mask resizing (preserves binary values)
- Loss & IoU curves + side-by-side prediction visualization

## Run

```bash
pip install torch torchvision segmentation-models-pytorch kagglehub tqdm matplotlib
python water_body_segmentation.py
# or open water_body_segmentation.ipynb in Google Colab
```

## Dataset

Auto-downloaded via `kagglehub` — no manual setup needed.

---
*Developed as part of KAUST AI training program*
