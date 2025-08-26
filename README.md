# 🚗 Comparative Analysis of CNN, MobileNetV2, and SmolVLM on the Stanford Cars Dataset

A machine learning project comparing the performance of three deep learning architectures—Custom CNN, MobileNetV2, and SmolVLM—on the Stanford Cars dataset for fine-grained image classification.

---

## 📌 Project Overview

This project investigates how different deep learning architectures perform when fine-tuned on the Stanford Car dataset. Models are evaluated based on:

- Classification accuracy  
- Training convergence speed  
- Computational efficiency  

---

## 🎯 Research Objectives

### Primary Objective
**How do different deep learning architectures (custom CNN, MobileNet V2, and SmolVLM) compare when fine-tuned on the Stanford Car dataset?**

### Secondary Objectives
- Evaluate model performance across multiple metrics.
- Determine if transfer learning significantly outperforms models trained from scratch.

---

## 📚 Dataset: Stanford Cars (huggingface Harsh9699/Stanford_car_75_25_split)

- **Total Images**: 16,185  
- **Classes**: 196 car types (make, model, year)  
- **Split**:  
  - Training: 12,064 images (74.5%)  
  - Testing: 4,121 images (25.5%)  
- **Resolution**: High (avg. 500×300 pixels)  
- **Challenges**: Fine-grained classification, variable lighting and orientation

---

## 🧠 Model Architectures

### 🛠 Custom CNN
- 12 convolutional layers
- 2 fully connected layers
- Dropout and batch normalization
- ~11.7 million parameters
- Trained from scratch

### 🛠 MobileNetV2
- Pretrained on ImageNet (1.2M images)
- Added new classification head
- Fine-tuned last 50 layers
- Lightweight and fast to train

### 🛠 SmolVLM (IDEFICS-3)
- Vision-language model with 2.8B parameters
- Fine-tuned using **QLoRA** (4-bit quantization + LoRA adapters)
- Only ~0.4% of parameters updated
- Best zero-shot and contextual performance

---

## 📊 Results Summary

| Model        | Accuracy | Notes                                        |
|--------------|----------|----------------------------------------------|
| Custom CNN   | 37.5%      | Low performance, underfit                    |
| MobileNetV2  | 69%      | Strong balance of speed and accuracy         |
| SmolVLM      | 96%      | Best performance using QLoRA fine-tuning     |

