🚗 #Comparative Analysis of CNN, MobileNetV2, and SmolVLM on the Stanford Cars Dataset
A machine learning study exploring how different deep learning architectures perform on fine-grained image classification using the Stanford Cars Dataset.

📌 Overview
This project investigates and compares three deep learning models:

A custom-built Convolutional Neural Network (CNN)

MobileNetV2 with transfer learning and fine-tuning

SmolVLM, a compact Vision-Language Model using QLoRA

The models are evaluated on their:

Classification accuracy

Convergence speed

Computational efficiency

🎯 Objectives
Primary Goal: Determine how different model architectures perform on a fine-grained classification task.

Secondary Goals:

Assess the value of fine-tuning pre-trained models

Evaluate trade-offs between performance and compute cost

📚 Dataset
Stanford Cars Dataset

16,185 high-resolution images

196 car classes (make, model, year)

Resplit into:

Training: 12,064 images (74.5%)

Testing: 4,121 images (25.5%)

Rich visual diversity: lighting, backgrounds, orientations

🛠️ Methodology
🔧 1. Custom CNN
Built from scratch

4 convolutional layers

2 fully connected layers

Batch normalization and dropout

~2.28M parameters

🔧 2. MobileNetV2
Pretrained on ImageNet (1.2M images)

New classification head added

Fine-tuning last 50 layers

Fast convergence and efficient performance

🔧 3. SmolVLM (IDEFICS-3 architecture)
2.8B parameter vision-language model

Fine-tuned using QLoRA (4-bit quantization + LoRA adapters)

Only ~0.4% of parameters are updated

Strong contextual reasoning and zero-shot potential

⚙️ Implementation
Framework: TensorFlow / Keras

Preprocessing:

Normalization

Data augmentation: rotation, flipping, shifting

Training:

Early stopping (patience=10)

Batch size: 32

Epochs: 70 (with early stop)

📈 Results
Model	Accuracy	Notes
Custom CNN	12%	Poor convergence, underfits data
MobileNetV2	78%	Good performance with fine-tuning
SmolVLM	92%	Best accuracy with QLoRA

