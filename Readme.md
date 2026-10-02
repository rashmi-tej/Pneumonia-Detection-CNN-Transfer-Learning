# Pneumonia Detection from Chest X-Ray Images

## 📌 Project Overview

This project uses **Deep Learning** to detect pneumonia from chest X-ray images.

Two different approaches are implemented separately:

1. **Custom Convolutional Neural Network (CNN)**
2. **Transfer Learning using MobileNetV2**

The models are trained and evaluated using the **Chest X-Ray Pneumonia dataset**. The goal is to classify an X-ray image into either:

- **NORMAL**
- **PNEUMONIA**

This project was developed using **Google Colab, Python, and TensorFlow/Keras**.

---

## 🎯 Objectives

- Detect pneumonia from chest X-ray images.
- Build a custom CNN model for image classification.
- Apply transfer learning using MobileNetV2.
- Train and validate the models.
- Evaluate model performance using accuracy, loss, classification report, and confusion matrix.
- Use the trained models to predict whether a new X-ray image is NORMAL or shows PNEUMONIA.

---

## 🗂️ Dataset

The project uses the **Chest X-Ray Images (Pneumonia)** dataset.

The dataset contains two classes:

```text
NORMAL
PNEUMONIA
```

The dataset is divided into:

```text
train/
├── NORMAL/
└── PNEUMONIA/

val/
├── NORMAL/
└── PNEUMONIA/

test/
├── NORMAL/
└── PNEUMONIA/
```

Dataset source:

**Chest X-Ray Images (Pneumonia) — Kaggle**

https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

---

## 🧠 Models Used

### 1. Custom CNN

A custom Convolutional Neural Network was developed using TensorFlow/Keras.

The architecture contains:

```text
Input Image
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Flatten
     ↓
Dense Layer
     ↓
Dropout
     ↓
Output Layer
```

The CNN takes grayscale chest X-ray images of size:

```text
224 × 224 × 1
```

The final layer uses a **sigmoid activation function** for binary classification.

---

### 2. Transfer Learning using MobileNetV2

The second approach uses **MobileNetV2**, a pretrained convolutional neural network.

The pretrained MobileNetV2 model uses ImageNet weights, while its original classification layer is replaced with a new classification head for pneumonia detection.

Architecture:

```text
Input Image
     ↓
MobileNetV2
     ↓
Global Average Pooling
     ↓
Dropout
     ↓
Output Layer
     ↓
NORMAL / PNEUMONIA
```

The input images are RGB images of size:

```text
224 × 224 × 3
```

---

## ⚙️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Kaggle API

---

## 📊 Model Evaluation

The models are evaluated using:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Test Accuracy
- Test Loss
- Classification Report
- Confusion Matrix

The training and validation accuracy/loss graphs are also generated to observe model performance during training.

---

## 🔍 Prediction

After training, the models can be used to classify a new chest X-ray image.

The prediction output is:

```text
NORMAL
```

or

```text
PNEUMONIA
```

The model also provides a prediction probability.

---

## 📁 Project Structure

```text
Pneumonia-Detection-CNN-Transfer-Learning/
│
├── Pneumonia_Detection.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

The dataset is not included in this repository because of its size. It can be downloaded from Kaggle.

---

## 🚀 How to Run the Project

### 1. Open the notebook

Open:

```text
Pneumonia_Detection.ipynb
```

using Google Colab or Jupyter Notebook.

### 2. Install the required libraries

Run:

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download the Chest X-Ray Pneumonia dataset from Kaggle.

### 4. Run the notebook

Run the notebook cells in order.

The notebook performs:

```text
Dataset Setup
      ↓
Data Loading
      ↓
Image Visualization
      ↓
CNN Model
      ↓
CNN Training
      ↓
CNN Evaluation
      ↓
MobileNetV2 Transfer Learning
      ↓
Transfer Learning Training
      ↓
Transfer Learning Evaluation
      ↓
New Image Prediction
```

---

## 📌 Results

The custom CNN and MobileNetV2 models are trained and evaluated separately.

The notebook contains the detailed:

- Accuracy results
- Loss results
- Confusion matrices
- Classification reports
- Prediction results

The results may vary depending on the training configuration and environment.

---

## ⚠️ Disclaimer

This project is developed for **educational and research purposes only**.

The predictions should not be considered a medical diagnosis. Medical decisions should always be made by qualified healthcare professionals.

---

## 👩‍💻 Author

**Rashmi T**

NMAM Institute of Technology
GitHub:  
https://github.com/rashmi-tej