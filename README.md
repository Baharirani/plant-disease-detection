# plant-disease-detection
# 🌿 Advanced Image Classification for Automated Plant Disease Detection
![Python](https://img.shields.io/badge/Python-3.8+-blue) ![PyTorch](https://img.shields.io/badge/Framework-PyTorch-orange) ![Computer Vision](https://img.shields.io/badge/Field-Computer%20Vision%20%7C%20Deep%20Learning-green)
## 📌 Project Overview

This project develops and evaluates a deep learning system for **automated plant disease detection** using image classification. Two convolutional neural network architectures are compared — a custom-built SimpleCNN trained from scratch and a **ResNet50 transfer learning model** — using the PlantVillage dataset. The goal is to support smart agricultural applications through early and accurate disease identification.

---

## 🎯 Objectives

- Build and train a custom CNN (SimpleCNN) as a baseline model
- Apply transfer learning using a pre-trained ResNet50 architecture
- Compare both models on accuracy, precision, recall, F1-score, and scalability
- Evaluate real-world performance on field images beyond the controlled dataset

---

## 📂 Dataset

| Dataset | Description |
|---|---|
| PlantVillage | Labelled leaf images across multiple plant disease categories |
| Split Ratio | 70% Training / 20% Validation / 10% Test |

---

## 🛠️ Methods & Tools

| Category | Tools / Methods |
|---|---|
| Language | Python |
| Framework | PyTorch |
| Models | SimpleCNN (from scratch), ResNet50 (Transfer Learning) |
| Preprocessing | Image resizing, normalization, data augmentation |
| Optimizer | Adam |
| Loss Function | Categorical Cross-Entropy |
| Evaluation | Accuracy, Precision, Recall, F1-Score, Confusion Matrix |

---

## 📊 Key Results

| Model | Validation Accuracy | Trainable Parameters | Macro F1-Score |
|---|---|---|---|
| SimpleCNN | 88.25% | 51,400,000 | 0.87 |
| ResNet50 | 98.91% | 23,500,000 | 0.99 |

- ✅ ResNet50 outperformed SimpleCNN by over 10 percentage points
- ✅ ResNet50 achieved this with **fewer parameters**, making it more efficient and scalable
- ✅ Strong precision, recall and F1-scores across all disease classes with ResNet50
- ⚠️ Both models struggled with complex real-world field backgrounds outside the training data

---

## 💡 Key Findings

- Transfer learning with ResNet50 is significantly more effective than training from scratch for plant disease classification
- A deeper architecture does not always mean more parameters — ResNet50 is both more accurate and more efficient than SimpleCNN
- Real-world deployment requires training data from actual field conditions, not just controlled laboratory images
- The domain gap between lab images and field images remains the main challenge for practical use

---

## 🗂️ Project Structure

```
plant-disease-detection/
│
├── data/                  # Dataset loading and preprocessing scripts
├── models/
│   ├── simple_cnn.py      # Custom CNN architecture
│   └── resnet50.py        # ResNet50 transfer learning model
├── training/              # Training loop and learning configuration
├── evaluation/            # Metrics, confusion matrix, scalability analysis
├── notebooks/             # Jupyter notebooks for experiments and visualisation
├── results/               # Accuracy charts, confusion matrices, sample predictions
└── README.md
```

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/baharirani/plant-disease-detection.git
cd plant-disease-detection

# Install dependencies
pip install -r requirements.txt

# Train SimpleCNN
python models/simple_cnn.py

# Train ResNet50
python models/resnet50.py

# Evaluate models
python evaluation/evaluate.py
```

---

## 📚 Context

This project was completed as part of an **MSc in Data Analytics** (Computer Vision and Artificial Intelligence module) at the Berlin School of Business and Innovation (BSBI), Berlin (2026).

---

## 👩‍💻 Author

**Bahar Irani**
MSc Data Analytics | Data Analyst
📧 iranibahhar@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/bahar-irani-1740952b0)
