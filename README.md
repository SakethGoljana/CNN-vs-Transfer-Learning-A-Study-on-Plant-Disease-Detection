
# 🌿 CNN vs Transfer Learning for Plant Disease Detection

### Comparative Analysis of Custom CNN and Pretrained Transfer Learning Models

---

## 📘 Overview

This project presents a **comparative analysis** between a **custom Convolutional Neural Network (CNN)** and three popular **pretrained transfer learning models** — **VGG16**, **ResNet50**, and **MobileNetV2** — for plant disease detection using leaf images.

The goal is to evaluate **accuracy, efficiency, and generalization** while promoting **sustainable AI solutions** for agricultural diagnostics.

All experiments were conducted using the **PlantVillage Dataset** and implemented in **TensorFlow/Keras**.

---

## 📊 Models Compared

| Model         | Accuracy | F1-Score | Parameters (M) | Notes |
|----------------|-----------|-----------|----------------|--------|
| **Custom CNN** | 0.87 | 0.84 | 3.2 | Lightweight, efficient for edge devices |
| **VGG16** | 0.91 | 0.89 | 14.7 | High accuracy, large model |
| **ResNet50** | **0.93** | **0.91** | 23.5 | Best performing overall |
| **MobileNetV2** | 0.90 | 0.87 | 3.4 | Best balance of speed and accuracy |

---

## 🌱 Dataset

**Dataset Used:** [PlantVillage Dataset – Kaggle](https://www.kaggle.com/datasets/emmarex/plantdisease)

- 📸 Contains **54,000+ leaf images**
- 🌿 Covers **38 classes** (including healthy leaves)
- 🌤️ High-resolution images of crops like tomato, potato, and apple
- 🧠 Used for **multi-class classification** of plant diseases

---

## 🧠 Methodology

### 🔹 Custom CNN
- 4 convolutional blocks (32 → 64 → 128 → 256 filters)
- Batch Normalization + MaxPooling + Dropout
- Fully connected dense layers with L2 regularization
- Optimized for lightweight performance

### 🔹 Transfer Learning Models
- **VGG16**, **ResNet50**, and **MobileNetV2** pretrained on ImageNet
- Fine-tuned for plant disease classification
- Global Average Pooling + Dense layers + Softmax output

### 🔹 Training Configuration
- **Optimizer:** Adam (lr = 0.0005)  
- **Batch Size:** 32  
- **Epochs:** 20 (EarlyStopping used)  
- **Regularization:** Dropout (0.3–0.5), L2 (0.001)  
- **Data Augmentation:** Rotation, zoom, shift, shear, flip  
- **Framework:** TensorFlow 2.x  
- **Platform:** Google Colab (NVIDIA Tesla T4 GPU)

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/PlantDiseaseDetection-CNN-vs-TransferLearning.git
cd PlantDiseaseDetection-CNN-vs-TransferLearning
````

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

Typical requirements:

```txt
tensorflow>=2.10
numpy
matplotlib
seaborn
scikit-learn
pandas
pillow
```

### 3️⃣ Download Dataset

Download from Kaggle and extract to a folder named `dataset/`.

```bash
kaggle datasets download -d emmarex/plantdisease
unzip plantdisease.zip -d dataset/
```

---

## 🚀 Running the Notebook

Open and execute the Jupyter notebook:

```bash
jupyter notebook "dl (1).ipynb"
```

or run directly in Google Colab:

1. Upload `dl (1).ipynb`
2. Mount your dataset folder
3. Run all cells sequentially

---

## 📈 Results & Visualizations

* Accuracy and Loss Curves for all models
* Confusion Matrices (Custom CNN, VGG16, ResNet50, MobileNetV2)
* Grad-CAM Heatmaps for interpretability
* Parameter vs Accuracy Comparison

**Example Visuals (to include later):**

* 📊 `training_accuracy_loss.png`
* 🔲 `confusion_matrix_resnet50.png`
* 🌾 `gradcam_visualization.png`

---

## 🧩 Key Findings

* **ResNet50** achieved the highest validation accuracy (93%).
* **Custom CNN** offered competitive performance with minimal parameters — ideal for **edge deployment**.
* **MobileNetV2** balanced speed and accuracy efficiently.
* **Transfer learning** models outperform in accuracy but require more computational resources.

---

## 🧭 Future Work

* Extend to **field-captured datasets** with natural conditions
* Deploy optimized models on **mobile/IoT edge devices**
* Explore **ensemble** and **model pruning** techniques
* Build a **real-time web or Android app** for live disease detection

---

## 🧾 Citation

If you use this work, please cite:

```
Goljana Sree Ratna Saketh, Ponnana Sri Sai Manikantha, Kuppili Hemanth, and Gaurav Sharan,
“Comparative Analysis of Custom CNN and Pretrained Transfer Learning Models for Plant Disease Detection,”
Lovely Professional University, 2025.
```

---

## 🙏 Acknowledgments

* **PlantVillage Dataset** – Open source dataset for plant disease classification
* **Google Colab** – GPU computation resources
* **TensorFlow/Keras** – Deep learning framework

---

## 📚 References

1. [PlantVillage Dataset on Kaggle](https://www.kaggle.com/datasets/emmarex/plantdisease)
2. Kumar et al., *IEEE, 2024* – Transfer Learning Architectures for Plant Disease Detection
3. Singh et al., *The Bioscan, 2024* – Comparative Study of Pre-trained Models
4. Fan et al., *Computers and Electronics in Agriculture, 2022*

---
