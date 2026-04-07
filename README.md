# KAUST AI Training — Deep Learning Projects

A collection of computer vision projects completed as part of the KAUST AI training program, covering classification, semantic segmentation, and transfer learning using PyTorch.

---

## Projects

### 🥔 [Potato Disease Classification](./potato-disease-cnn/)
Classifying potato leaf diseases from the PlantVillage dataset using a CNN built from scratch.

- 5-layer CNN with BatchNormalization
- Residual (skip) connection from layer 2 → layer 4
- **Best Val Accuracy: 98.61%** (10 epochs)
- Dataset: PlantVillage — 3 classes (Early Blight, Late Blight, Healthy)

---

### 🌊 [Underwater Image Segmentation](./underwater-image-segmentation/)
Pixel-level segmentation of underwater scenes into 8 semantic categories.

- U-Net with EfficientNet-B1 encoder (pretrained on ImageNet)
- Dataset: SUIM — divers, fish, reefs, robots, and more
- Fine-tuned classifier head, frozen encoder backbone

---

### 🚭 [Smoking Detection Classifier](./smoking-detection-classifier/)
Binary classifier detecting whether a person is smoking or not.

- ResNet-18 fine-tuned for binary classification
- BCEWithLogitsLoss with sigmoid thresholding
- Separate train / validation / test evaluation

---

### 🛰️ [Water Body Segmentation](./water-body-segmentation/)
Detecting and segmenting water bodies in satellite imagery.

- U-Net with EfficientNet-B1 encoder
- Binary segmentation (water vs. non-water)
- Mean IoU tracked alongside loss

---

## Stack

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=flat&logo=googlecolab&logoColor=white)

- **Framework**: PyTorch + torchvision
- **Models**: CNN from scratch, ResNet-18, U-Net + EfficientNet-B1
- **Tools**: segmentation-models-pytorch, kagglehub, tqdm, matplotlib

---

*KAUST AI Training Program — 2025*
