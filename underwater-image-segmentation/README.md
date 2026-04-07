# 🌊 Multi-Class Segmentation for Underwater Imagery

Fine-tuning a pretrained U-Net for pixel-level segmentation of underwater scenes using the SUIM dataset.

## Overview

| | |
|---|---|
| **Task** | Semantic segmentation |
| **Dataset** | SUIM (Semantic Segmentation of Underwater Imagery) |
| **Classes** | 8 (divers, fish, reefs, robots, plants, wrecks, sea-floor, background) |
| **Framework** | PyTorch + segmentation-models-pytorch |

## Classes

| ID | Category |
|---|---|
| 0 | Background (waterbody) |
| 1 | Human divers |
| 2 | Aquatic plants & sea-grass |
| 3 | Wrecks and ruins |
| 4 | Robots (AUVs/ROVs) |
| 5 | Reefs and invertebrates |
| 6 | Fish and vertebrates |
| 7 | Sea-floor and rocks |

## Highlights

- **U-Net** with **EfficientNet-B1** encoder pretrained on ImageNet
- Custom `SegDataset` class with index-based train/test split
- NEAREST interpolation for mask resizing (preserves class labels)
- Training & validation loss curves over 10 epochs

## Run

```bash
pip install torch torchvision segmentation-models-pytorch kagglehub tqdm matplotlib
python multi_class_segmentation_for_underwater_imagery.py
```

## Dataset

Auto-downloaded via `kagglehub` — no manual setup needed.

---
*Developed as part of KAUST AI training program*
