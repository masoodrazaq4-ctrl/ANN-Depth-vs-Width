# ANN-Depth-vs-Width
Comparison of deep vs wide neural networks on tabular data, including class imbalance handling and SHAP-based model interpretation.
# Artificial Neural Networks: Depth vs Width Analysis

## 📌 Overview

This project investigates a fundamental question in neural network design:

**Is it better to increase network depth (more layers) or width (more neurons)?**

Using the Forest Cover Type dataset (581,012 samples, 54 features, 7 classes), we compare two architectures:

* **Deep Network**: 10 layers × 64 neurons (with Batch Normalization)
* **Wide Network**: 2 layers × 512 neurons

The goal is to evaluate performance, training behaviour, and interpretability in a real-world tabular classification problem.

---

## 📊 Key Results

| Metric      | Deep Network | Wide Network |
| ----------- | ------------ | ------------ |
| Accuracy    | 70.76%       | 87.53%       |
| Macro F1    | 0.60         | 0.81         |
| Weighted F1 | 0.72         | 0.88         |
| Latency     | 7.84s        | 6.05s        |

👉 **Conclusion:** Wide networks significantly outperform deep networks on tabular data.

---

## 🧠 Key Insights

* Depth is not always beneficial for structured/tabular data
* Batch Normalization is essential for deep networks
* Class weights effectively handle extreme imbalance (103:1)
* SHAP confirms that models learn ecologically meaningful patterns

