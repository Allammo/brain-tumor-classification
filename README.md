# Brain Tumor Classification from MRI Images

*Deep Learning · Transfer Learning · Medical Imaging · Multi-class Classification*

---

## Overview

A comparative study of deep learning architectures for multi-class brain tumor classification from MRI scans. The project evaluates four pre-trained convolutional neural networks on a dataset of 3,600+ MRI images spanning three tumor types, using transfer learning and fine-tuning throughout.

**Tumor classes:** Glioma · Meningioma · Pituitary tumor · No tumor

---

## Results

| Model | Training Accuracy | Misclassifications (per class) |
|---|---|---|
| DenseNet121 | >99% | ≤3 |
| EfficientNetB0 | >99% | ≤3 |
| ResNet18 | >99% | ≤3 |
| VGG16 | >99% | ≤3 |

All four architectures achieved stable convergence with fewer than 3 misclassifications per class across ~3,600 samples.

---

## Methodology

1. **Data preprocessing** — image resizing, normalization, augmentation (flip, rotation, zoom)
2. **Transfer learning** — ImageNet pre-trained weights, frozen base layers
3. **Fine-tuning** — unfreezing top layers, reduced learning rate
4. **Evaluation** — confusion matrices, training/validation loss curves, per-class accuracy

---

> **Dataset:** [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) — available on Kaggle. 

---


## Tech stack

Python · PyTorch · Torchvision · Scikit-learn · Matplotlib · Seaborn

---

## Key takeaways

- Transfer learning with fine-tuning is highly effective even on relatively small medical imaging datasets
- DenseNet121's dense connections provided strong gradient flow for this classification task
- Confusion matrices revealed that meningioma was the hardest class to separate — consistent with clinical literature
