# 📘 NeuralNet-Engine-Cpp

A from-scratch neural network engine in C++ demonstrating core deep learning principles without external ML frameworks.

📌 Overview

NeuralNet-Engine-Cpp is a lightweight, educational neural network engine implemented entirely from scratch in C++.
The project focuses on clarity, correctness, and understanding, rather than using high-level libraries.

The engine implements:

Fully connected (dense) neural networks

Forward propagation

Backpropagation with gradient descent

Training and evaluation on the MNIST handwritten digit dataset

This project is designed to demonstrate how neural networks actually work internally, making it ideal for:

Learning ML fundamentals

Understanding backpropagation at code level

Showcasing strong C++ + ML foundations on a resume

## 🧠 Key Features

✅ Pure C++ implementation (no TensorFlow / PyTorch)

✅ Modular neural network components

✅ Forward & backward propagation

✅ Gradient descent optimization

✅ MNIST dataset support

✅ CMake build system

✅ Clean, readable, and extensible codebase

## 🏗️ Project Architecture

NeuralNet-Engine-Cpp/
│
├── CMakeLists.txt        # Build configuration
├── README.md             # Project documentation
│
├── src/
│   ├── main.cpp          # Entry point and training loop
│   ├── NeuralNetwork.cpp # Neural network logic
│   ├── NeuralNetwork.h
│   ├── Layer.cpp         # Layer abstraction
│   ├── Layer.h
│   ├── Utils.cpp         # Helper utilities
│   └── Utils.h
│
└── data/
    └── mnist/            # MNIST dataset files

Design philosophy:
Each component (network, layers, utilities) is kept separate to ensure maintainability and extensibility.

## ⚙️ How It Works (High-Level)

Input Layer

Reads pixel values from MNIST images

Normalizes input data

Hidden Layers

Fully connected layers

Activation functions applied

Output Layer

Produces probability scores for digits (0–9)

Training

Loss computed using prediction vs ground truth

Gradients calculated using backpropagation

Weights updated using gradient descent

## 🔁 Training Pipeline
Input → Forward Pass → Loss Calculation
      → Backpropagation → Weight Update
      → Repeat for Epochs

This explicit pipeline makes the learning process transparent and debuggable, unlike black-box frameworks.

## 📊 Dataset

MNIST Handwritten Digits

60,000 training images

10,000 test images

Each image: 28×28 grayscale

The dataset is widely used as a benchmark for classification models.

## 🧪 How to Build & Run
🔧 Prerequisites

C++17 compatible compiler

CMake (≥ 3.10)

🏗️ Build

```mkdir build
cd build
cmake ..
make ```

▶️ Run
```./NeuralNetEngine
```
## 📈 Results

The network successfully learns digit classification

Accuracy improves steadily across epochs

Demonstrates correct gradient flow and convergence behavior

Note: This engine prioritizes correctness and clarity over performance.

## 🎯 Learning Outcomes

By building this project, I gained:

Deep understanding of backpropagation

Hands-on experience with numerical stability

Stronger grasp of ML mathematics

Confidence in implementing complex systems in C++

## 🚀 Possible Extensions

Add configurable activation functions (ReLU, Tanh)

Support for different optimizers (Adam, RMSProp)

Modular loss functions

Batch normalization

GPU acceleration (future work)

Unit tests for layers and gradients