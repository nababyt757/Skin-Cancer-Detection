# EfficientNetV2-L Based Melanoma Detection from Skin Lesion Images  

## 📌 Project Overview  
This project focuses on the **automated detection of melanoma** (a severe type of skin cancer) from dermoscopic skin lesion images using **deep learning**.  

- Initially, a **custom CNN architecture** was implemented for binary classification (malignant vs benign).  
- While the CNN achieved reasonable accuracy, it lacked the generalization ability required for reliable medical diagnosis.  
- To improve performance, we adopted **EfficientNetV2-L** (a state-of-the-art convolutional neural network) with transfer learning, which significantly boosted **validation accuracy and robustness**.  

The objective is to build an **accurate, efficient, and scalable system** that can assist dermatologists in early melanoma screening.  

---

## 🚀 Features  
- Implementation of both **Custom CNN** and **EfficientNetV2-L** models.  
- **Binary classification**: Malignant (Melanoma) vs Benign.  
- **Data augmentation** for robustness (rotation, flipping, cropping).  
- **Mixed-precision training** with gradient scaling for faster performance.  
- **Early stopping & learning rate scheduling** to prevent overfitting.  
- **Performance visualization** with loss curves, accuracy plots, and confusion matrix.  

---

## 📂 Dataset  
Dataset used: **Melanoma Cancer Image Dataset** (Kaggle).  

- Total images: ~13,900  
- Classes:  
  - **Malignant (Melanoma)**  
  - **Benign (Non-Melanoma)**  
- Image resolution: 64×64 px  
- Data split: Training / Validation  

> 📎 Dataset link: [Kaggle – Melanoma Cancer Dataset](https://www.kaggle.com/)  

---

## 🏗️ Model Architectures  

### 1️⃣ Custom CNN (Baseline)  
- Convolutional + Pooling layers  
- Fully Connected Layers  
- Sigmoid output  

📉 Accuracy: ~91%  

---

### 2️⃣ EfficientNetV2-L (Final Model)  
- Pre-trained on **ImageNet**  
- Fine-tuned for binary classification  
- Final layer replaced with:  
  **Dropout → Linear → Sigmoid**  

📈 Accuracy: ~96%  

---

## ⚙️ Installation  

Clone the repository:  
```bash
git clone https://github.com/aishwaryashinde26/Skin-Cancer-Detection.git
```

## ⚙️ Installation dependencies:

- torch>=2.0.0
- torchvision>=0.15.0
- numpy>=1.23.0
- matplotlib>=3.7.0
- seaborn>=0.12.0
- scikit-learn>=1.2.0


## 🖥️ Usage
- Run CustomCNN.ipynb for CNN model
- Run EfficientNetV2L.ipynb for EfficientNet model

## 📊 Results
- **Custom CNN:** ~91% validation accuracy
- **EfficientNetV2-L:** ~96% validation accuracy
- Loss and accuracy plots show improved stability and generalization after switching to EfficientNetV2-L.

## 🔮 Future Scope
- Expand to **multi-class skin cancer classification** (different cancer types).
- Deploy as a **web / mobile application** for real-time screening.
