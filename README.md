# 🍬 Candy Classification with YOLOv11

A deep learning project for detecting and classifying different types of candies using the **YOLOv8** object detection model. This repository contains the complete pipeline from dataset preparation to training, validation, testing, and inference.

---

## 📌 Project Overview

This project uses **Ultralytics YOLOv11** to train an object detection model on a custom candy dataset.  
The workflow includes:

- Dataset extraction and organization into `train`, `val`, and `test` sets (80/10/10 split)
- Automatic generation of the `data.yaml` configuration file
- Model training and hyperparameter tuning
- Evaluation and performance testing
- Running inference on custom images

---

## 📂 Dataset Setup

Your dataset should contain:
```
/images
   ├── image1.jpg
   ├── image2.jpg
/labels
   ├── image1.txt
   ├── image2.txt
classes.txt
```

- **`images/`** – All candy images (`.jpg`, `.png`, etc.)
- **`labels/`** – YOLO-format annotation files (`.txt`) for each image
- **`classes.txt`** – List of class names (one per line)

---

## ⚙️ Installation

```bash
# Clone this repository
git clone https://github.com/your-username/candy-classification.git
cd candy-classification

# Install YOLOv8
pip install ultralytics

# (Optional) Install other dependencies
pip install opencv-python pyyaml
```

---

## 🚀 Usage

### 1️⃣ Dataset Preparation
Unzip your dataset into a working directory:
```bash
unzip candy_data.zip -d custom_data
```
Run the notebook cells to:
- Create train/val/test directories
- Split data automatically
- Generate `data.yaml` from `classes.txt`

---

### 2️⃣ Training the Model
```python
from ultralytics import YOLO

model = YOLO('yolov8n.pt')  # or yolov8s.pt for better accuracy
model.train(data='data.yaml', epochs=50, imgsz=640)
```

---

### 3️⃣ Validation
```python
metrics = model.val()
print(metrics)
```

---

### 4️⃣ Testing
```python
results = model.predict(source='test_data/images', save=True)
```

---

### 5️⃣ Inference on Custom Images
```python
results = model.predict(source='path/to/your/image.jpg', save=True)
```
The predictions will be saved in the `runs/detect/` directory.

---

## 📁 Folder Structure
```
candy-classification/
│── custom_data/
│   ├── images/
│   ├── labels/
│── data/
│   ├── train_data/
│   ├── val_data/
│   ├── test_data/
│── data.yaml
│── Candy_Classification.ipynb
│── README.md
```

---

