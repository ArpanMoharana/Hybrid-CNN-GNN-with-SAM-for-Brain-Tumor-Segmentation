# 🧠 Hybrid CNN–GNN with Automated SAM Refinement for Brain Tumor Segmentation

This project presents a hybrid deep learning framework for **accurate brain tumor segmentation** from multi-parametric MRI images.

The system integrates:
- 🧠 CNN (U-Net) for local feature extraction  
- 🌐 GNN for global spatial reasoning  
- ✂️ SAM (Segment Anything Model) for boundary refinement  

---

![Detailed All Models](https://raw.githubusercontent.com/ArpanMoharana/Hybrid-CNN-GNN-with-SAM-for-Brain-Tumor-Segmentation/main/Visual%20Output/DETAILED%20ALL%20MODELS.png)
## 📌 Project Overview

Brain tumor segmentation is a challenging task due to variability in tumor shape, size, and location.

Traditional approaches often:
- Capture only local features (CNNs), or  
- Miss spatial relationships (lack global context)
  ![All Models](https://raw.githubusercontent.com/ArpanMoharana/Hybrid-CNN-GNN-with-SAM-for-Brain-Tumor-Segmentation/main/Visual%20Output/all%20models.png)

This project addresses these limitations by combining:
- **CNN → local features**
- **GNN → structural understanding**
- **SAM → precise boundary refinement**

The pipeline is fully automated and does not require manual segmentation input.

---

## 🚀 Key Contributions

- Hybrid CNN + GNN architecture  
- Automated prompt generation for SAM  
- Fully automated segmentation pipeline  
- Improved tumor localization and boundary precision  
- Safety mechanism to reduce over-segmentation

## Low-Level System Design

![Low Level System Design](https://raw.githubusercontent.com/ArpanMoharana/Hybrid-CNN-GNN-with-SAM-for-Brain-Tumor-Segmentation/main/Visual%20Output/Low%20Level.png)

## High-Level System Design

![High Level System Design](https://raw.githubusercontent.com/ArpanMoharana/Hybrid-CNN-GNN-with-SAM-for-Brain-Tumor-Segmentation/main/Visual%20Output/high%20level%20system%20design.png)
---

## 🏗️ Architecture Overview
MRI Input
│
▼
CNN (U-Net)
│
▼
GNN
│
▼
Hybrid Mask
│
▼
Auto Bounding Box
│
▼
SAM Refinement
│
▼
Final Segmentation

## Step-by-Step Pipeline

![Pipeline](https://raw.githubusercontent.com/ArpanMoharana/Hybrid-CNN-GNN-with-SAM-for-Brain-Tumor-Segmentation/main/Visual%20Output/pipeline.png)
---

## 🔬 Methodology

### 1. Preprocessing
- MRI normalization
- Noise reduction

### 2. CNN (U-Net)
- Extracts local texture features  
- Generates initial tumor segmentation  

### 3. GNN
- Models spatial relationships between regions  
- Reduces false positives  

### 4. Hybrid Fusion
- Combines CNN + GNN outputs  

### 5. SAM Integration
- Automatically generates bounding box  
- Refines tumor boundary  

### 6. Safety Mechanism
- Prevents over-segmentation  
- Falls back to hybrid output if needed
  ## Visual Segmentation Results

![Visual Results](https://raw.githubusercontent.com/ArpanMoharana/Hybrid-CNN-GNN-with-SAM-for-Brain-Tumor-Segmentation/main/Visual%20Output/visual.png)

---

## 📊 Model Performance

| Metric | Value |
|------|------|
| Dice Score | **0.8585** |
| Precision | **0.7921** |
| Recall | **0.9430** |
| Inference Time | **0.0109 sec** |

> High recall ensures minimal missed tumor regions, which is critical in medical diagnosis.

---
## NOTE - This project was developed and executed on Google Colab using Google's T4 GPU.
