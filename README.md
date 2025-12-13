# Venice Boat Classification – Deep Learning Workflow

## 📌 Project Overview

This project classifies **24 different types of boats in Venice** using deep learning. The goal is to automate visual recognition of boats and explore the benefits of **transfer learning** with MobileNetV2 compared to a CNN from scratch.

---

## 🎯 Objective

* Automatically classify boat images into categories (e.g., gondola, motorboat, ferry).
* Use supervised learning with labeled images.
* Evaluate performance with accuracy, validation loss, confusion matrix, and sample predictions.

**Why this matters:**

* Helps automate boat recognition for tourism, safety, and research.
* Provides insights into boat usage patterns.
* Serves as a benchmark for computer vision projects.

---

## 🗂 Dataset

* **Total images:** 4,774 (all in class-specific subfolders)
* Non-image files like `DBinfo.txt` are ignored.

### Dataset Split

| Split      | Images | %    |
| ---------- | ------ | ---- |
| Training   | 3,830  | ~80% |
| Validation | 944    | ~20% |
| **Total**  | 4,774  | 100% |

---

## 🧠 Models & Experiments

### 1️⃣ CNN From Scratch (Baseline)

* Training Accuracy: ~74%
* Validation Accuracy: ~67%
* Slight overfitting observed
* Serves as a baseline for comparison

### 2️⃣ CNN Hyperparameter Tuning Attempt

* Training Accuracy: 16–44%
* Validation Accuracy: <37%
* Unstable results, worse than baseline

### 3️⃣ Pretrained MobileNetV2

* Training Accuracy: ~74%
* Validation Accuracy: ~75%
* Lower loss and better generalization

### 4️⃣ Fine-Tuned MobileNetV2

* Training Accuracy: ~82%
* Validation Accuracy: ~78%
* Best overall performance

---

## 📊 Performance Summary

| Model                  | Training Acc | Validation Acc | Validation Loss | Stability  |
| ---------------------- | ------------ | -------------- | --------------- | ---------- |
| CNN Scratch            | ~74%         | ~67%           | 1.18 – 2.0+     | Fluctuated |
| CNN Tuning             | <45%         | <37%           | >2.5            | Poor       |
| MobileNetV2            | ~74%         | ~75%           | ↓0.82           | Good       |
| Fine-Tuned MobileNetV2 | 82%          | 78%            | ↓0.71           | Best       |

---

## ✅ Solution & Use Cases

* **Solution:** Fine-tuned MobileNetV2 accurately classifies boats about **8 out of 10 times**.
* **Why it matters:** Automates boat recognition, informs tourism and safety decisions, and supports research.
* **Use cases:**

  * Track boat traffic for urban planning and tourism.
  * Monitor maritime safety.
  * Analyze boat usage for environmental impact.
  * Develop apps that identify boat types in real-time.

---

## 🚀 Key Takeaway

> Transfer learning significantly improves performance and stability for multi-class image classification, especially when dealing with limited or visually similar datasets.
# venice-boat-classification
