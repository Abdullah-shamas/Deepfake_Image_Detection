# DeepFake Image Detection using Transfer Learning (ResNet50)

A Deep Learning framework developed to distinguish between real images and AI-generated synthetic images (DeepFakes). This project utilizes the **CIFAKE dataset** and applies Transfer Learning via a pre-trained **ResNet50** architecture combined with advanced regularization techniques to ensure high evaluation precision.

## 🚀 Project Overview
With the rise of generative AI models (like GANs, Diffusion Models), synthetic image generation has become highly sophisticated. This project implements a binary classification pipeline using TensorFlow/Keras to perform accurate artifact detection in digital media.

### Key Features
- **Dataset:** CIFAKE (80,000 training images, 20,000 testing images) evenly split into `Real` and `FAKE`.
- **Core Architecture:** Pre-trained **ResNet50** (ImageNet weights) used as a frozen feature extractor.
- **Data Augmentation:** Real-time translation, horizontal flipping, and brightness adjustments to combat overfitting.
- **Regularization:** Batch Normalization and dynamic Dropout (0.5) layers.
- **Optimization:** Adam Optimizer with a controlled learning rate ($1e^{-4}$) and Binary Cross-Entropy loss.

---

## 📊 Model Architecture & Methodology


1. **Pre-processing:** Input images are resized to $32 \times 32 \times 3$ and normalized to $[0, 1]$.
2. **Feature Extraction:** Global Average Pooling 2D maps spatial features from ResNet50.
3. **Classification Head:** Dense layers with ReLU activation leading to a single Sigmoid neuron output.
4. **Early Stopping:** Monitored via validation loss with a patience parameter to ensure optimum generalization.

---

## 📈 Performance & Evaluation

The model evaluates metrics including Accuracy, Loss, Precision-Recall Curves, and a Confusion Matrix.

### Classification Report Summary
- **Precision:** Measures the accuracy of fake image predictions.
- **Recall:** Measures the ability to find all actual fake images.
- **F1-Score:** Harmonic mean of precision and recall.# Deepfake_Image_Detection
