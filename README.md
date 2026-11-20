# 🧠 Handwritten Digit Recognition (MNIST) with PyTorch & Gradio

[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-EE4C2C.svg?style=flat&logo=pytorch&logoColor=white)](https://pytorch.org)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg?style=flat&logo=python&logoColor=white)](https://python.org)
[![Gradio](https://img.shields.io/badge/Gradio-Web%20UI-FF7C00.svg?style=flat)](https://gradio.app)
[![Accuracy](https://img.shields.io/badge/Test%20Accuracy-99.18%25-brightgreen.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An end-to-end Computer Vision project implementing a Convolutional Neural Network (CNN) in PyTorch to classify handwritten digits (0–9) from the classic MNIST dataset, featuring an interactive real-time Gradio drawing canvas.

---

## 📌 Highlights & Performance

* **Test Accuracy:** **99.18%** on 10,000 unseen test samples.
* **Architecture:** 2D Convolutional layers with Batch Normalization, ReLU activation, Max Pooling, and Dropout for regularization.
* **Interactive Web Interface:** Real-time canvas where users can sketch digits with a mouse or touchscreen and receive instant model inference with confidence probability distributions.

---

## 🏗 Model Architecture

```text
Input (1x28x28)
  │
  ├──► Conv2D(1 -> 32, kernel=3, padding=1) + BatchNorm2d + ReLU
  ├──► Conv2D(32 -> 64, kernel=3, padding=1) + BatchNorm2d + ReLU
  ├──► MaxPool2d(2x2) + Dropout(0.25)
  │
  ├──► Conv2D(64 -> 128, kernel=3, padding=1) + BatchNorm2d + ReLU
  ├──► MaxPool2d(2x2) + Dropout(0.25)
  │
  ├──► Flatten (128 x 7 x 7 = 6272)
  ├──► Linear(6272 -> 256) + ReLU + Dropout(0.5)
  └──► Linear(256 -> 10) + LogSoftmax
```

---

## 🚀 Getting Started

```bash
# Clone repository
git clone https://github.com/quvonchbek212/mnist-digit-recognition.git
cd mnist-digit-recognition

# Install dependencies
pip install torch torchvision gradio numpy matplotlib

# Run interactive drawing app
python app.py
```

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
