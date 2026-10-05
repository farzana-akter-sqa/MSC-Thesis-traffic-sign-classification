# MSC-Thesis-traffic-sign-classification
MSc Thesis at Jahangirnagar University: A comparative study of MobileNetV2, ResNet50, VGG19, and EfficientNetB0 on a custom 22-class traffic sign dataset (10,647 images).
# 🚗 Traffic Sign Classification using Deep Learning Comparative Study
**Master of Science (MSc) Thesis | Department of Computer Science and Engineering, Jahangirnagar University**

## 📝 Project Overview
This repository contains the official implementation, custom dataset details, and evaluation code for my MSc thesis. The research addresses class imbalance issues found in traditional benchmark datasets (like GTSRB) by introducing a brand-new, equitably balanced custom traffic sign dataset. It evaluates the accuracy-efficiency trade-offs of four state-of-the-art Convolutional Neural Networks (CNNs) under identical transfer learning experimental conditions.

## 🎓 Academic Credentials & Administration
* **Author:** Farzana Akter (Prity)
* **Institution:** Jahangirnagar University
* **Degree:** M.Sc. in Computer Science and Engineering
* **Supervised by:** Bulbul Ahammad, Lecturer (CSE, JU)
* **Date of Submission:** July 2026

## 📊 Dataset Specifications
Unlike heavily skewed public sets, this study features a proprietary, custom-built dataset:
* **Total Images:** 10,647 images
* **Total Classes:** 22 distinct traffic sign categories
* **Class Distribution:** Highly balanced (each class represents ~4% of the entire dataset on average)
* **Dimensions:** 128 × 128 pixels with 3 color channels (RGB)

## 🛠️ Tech Stack & Unified Protocol
* **Language:** Python
* **Framework:** TensorFlow (Keras)
* **Optimizer & Loss:** Adam (Learning Rate: 0.001) | Categorical Cross-Entropy
* **Protocol:** ImageNet frozen backbone models, identical data augmentation (rotation, zoom, contrast, translation), dropout rate of 0.30, shallow classification heads, trained across 20 epochs.

## 📈 Quantitative Performance Results
The models demonstrated the following macro-averaged evaluation accuracies on the custom evaluation set:

| Architecture | Accuracy (%) | Precision (Macro) | Recall (Macro) | F1-Score (Macro) |
| :--- | :---: | :---: | :---: | :---: |
| **EfficientNetB0** | **97%** | **0.97** | **0.98** | **0.97** |
| **MobileNetV2** | **96%** | **0.96** | **0.96** | **0.96** |
| **ResNet50** | **96%** | **0.97** | **0.96** | **0.96** |
| **VGG19** | **93%** | **0.93** | **0.94** | **0.93** |

### Key Research Insights:
1. **EfficientNetB0** achieved the highest performance due to its compound scaling architecture balancing depth, width, and resolution.
2. **MobileNetV2** proved to be an outstanding, lightweight alternative ideal for edge deployments and resource-constrained environments.
3. **ResNet50** displayed significant stability in preventing gradient degradation within closely related visual groups (e.g., speed limit variances) via its residual skip connections.

## 📁 Repository Structure
* `/dataset` - Breakdown of the 22 class allocations and distributions.
* `/notebooks` - Preprocessing workflows, data augmentation configurations, and training code.
* `/models` - Architecture summaries and frozen feature-extraction head layouts.
* `/results` - Normalized confusion matrices and accuracy/loss curves.
* `/report` - Thesis abstract and documentation copy.
