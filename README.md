# Candy Classification & Object Detection Project

This repository contains two computer vision tasks:

1. **Candy Classification using YOLOv11** – Detects and classifies different types of candies in images.
2. **Object Detection using SIFT** – Detects and matches keypoints between images using the Scale-Invariant Feature Transform (SIFT) algorithm.

---

## 📂 Project Structure

├── Candy_Classification.ipynb # YOLOv11-based candy classification code
├── candy_data/ # Dataset for candy classification
│ ├── images/ # Images for training/testing
│ ├── labels/ # YOLO annotation files
│ └── data.yaml # YOLO dataset configuration
├── Template/ # Dataset for SIFT object detection
│ ├── template.jpg # Template image for matching
│ ├── query_images/ # Query images for detection
├── sift_object_detection.py # SIFT object detection code
├── requirements.txt # Python dependencies
└── README.md # Project documentation

yaml
Copy
Edit

---

## 📌 1. Candy Classification (YOLOv11)

### **Overview**
This module uses YOLOv11, a state-of-the-art object detection model, to classify and locate different candy types in images.

### **Steps to Run**
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
Train YOLOv11 on the candy dataset:

bash
Copy
Edit
yolo task=detect mode=train model=yolov11.pt data=candy_data/data.yaml epochs=50 imgsz=640
Run inference on test images:

bash
Copy
Edit
yolo task=detect mode=predict model=runs/detect/train/weights/best.pt source=candy_data/images/test
📌 2. Object Detection (SIFT)
Overview
This module uses OpenCV's SIFT algorithm to detect and match keypoints between a template image and query images.

Steps to Run
Install OpenCV with extra features:

bash
Copy
Edit
pip install opencv-python opencv-contrib-python
Run the detection script:

bash
Copy
Edit
python sift_object_detection.py
The script will display matched features between the template and query images.

📊 Results
YOLOv11 Candy Classification
High accuracy in detecting multiple candy types in various lighting conditions.

Works in real-time on video streams.

SIFT Object Detection
Robust to scale and rotation changes.

Can be used for detecting objects in cluttered environments.

📦 Requirements
Python 3.8+

YOLOv11 (via Ultralytics)

OpenCV (with contrib modules)

NumPy

Matplotlib

Install all dependencies:

bash
Copy
Edit
pip install -r requirements.txt
🤝 Contribution
Feel free to fork this repo and submit pull requests to improve accuracy, add more candy classes, or integrate new detection algorithms.

