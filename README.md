# 🔬 Skin Lesion Classification & Interpretability (ISIC 9-Class)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Kaggle](https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white) 

A robust, lightweight Convolutional Neural Network (CNN) ensemble designed to classify dermoscopic images into 9 distinct skin cancer categories. This project emphasizes clinical trust through Explainable AI (XAI), utilizing Grad-CAM to provide high-resolution, pixel-level visual evidence for every model prediction.

## 📖 Overview
Automated melanoma and skin lesion classification requires both high accuracy and computational efficiency. This repository implements an ensemble of **EfficientNet-B0** and **MobileNetV3-Small**. By fusing the feature maps of these two pre-trained architectures, the model achieves superior feature extraction for complex dermatological textures while maintaining a memory footprint small enough for standard hardware constraints.

### Key Features
* **Lightweight Ensemble Architecture:** Fuses 1280 features from EfficientNet-B0 and 576 features from MobileNetV3-Small.
* **Explainable AI (XAI):** Integrated `pytorch-grad-cam` pinpoints exactly which morphological features (e.g., asymmetrical borders, pigmentation networks) drove the final prediction.
* **Clinical Dataset:** Trained and evaluated on the ISIC (International Skin Imaging Collaboration) dataset.
* **Research Ready:** Codebase is structured for full reproducibility, modularity, and easy extraction of metrics/visualizations for peer-reviewed journal manuscripts.

---

## 🗄️ Dataset Structure
This project utilizes a 9-class subset of the ISIC archive. The data loader expects the following directory structure:

```text
Dataset/
├── Train/
│   ├── actinic keratosis
│   ├── basal cell carcinoma
│   ├── dermatofibroma
│   ├── melanoma
│   ├── nevus
│   ├── pigmented benign keratosis
│   ├── seborrheic keratosis
│   ├── squamous cell carcinoma
│   └── vascular lesion
└── Test/
