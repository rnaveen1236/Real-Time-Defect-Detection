# 🔍 Real-Time Defect Detection System using YOLO

## 📌 Project Overview

This project implements a **Real-Time Industrial Defect Detection System** using YOLO and OpenCV.

The system can:

* Train a custom defect detection model
* Perform real-time detection using a live camera
* Detect defects from input images

This project follows a **minimal and clean architecture** with a single Python file (`src.py`) for simplicity and easy deployment.

---

## 🏗️ Project Structure

```bash
real_time_defect_detection/
│
├── dataset/
│   ├── images/
│   │   ├── train/
│   │   ├── val/
│   │   └── test/
│   │
│   ├── labels/
│   │   ├── train/
│   │   ├── val/
│   │   └── test/
│   │
│   └── data.yaml
│
├── models/
│   ├── yolov8n.pt
│   └── best.pt
│
├── src.py
├── requirements.txt
└── README.md
```

---

## 📂 Dataset Format (YOLO Format)

Each image must have a corresponding `.txt` label file with the same name.

Example:

```
images/train/metal_01.jpg
labels/train/metal_01.txt
```

### 📄 Label File Format

```
class_id x_center y_center width height
```

All values must be **normalized between 0 and 1**.

Example:

```
0 0.512 0.423 0.210 0.180
1 0.324 0.651 0.120 0.090
```

---

## 📄 data.yaml Configuration

Located inside `dataset/data.yaml`

```yaml
path: dataset
train: images/train
val: images/val
test: images/test

nc: 2
names:
  0: scratch
  1: crack
```

---

## ⚙️ Technologies Used

* Python 3.9+
* YOLO (Ultralytics – v8 / v11 compatible)
* OpenCV
* PyTorch
* NumPy

---

## 📦 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/real_time_defect_detection.git
cd real_time_defect_detection
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3️⃣ Install Requirements

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

Run the main file:

```bash
python src.py
```

You will see:

```
1 - Train Model
2 - Real-Time Detection
3 - Detect Image
```

### 🔹 Option 1 – Train Model

Trains YOLO using dataset in `dataset/`

### 🔹 Option 2 – Real-Time Detection

Uses webcam to detect defects live.

Press **Q** to quit.

### 🔹 Option 3 – Image Detection

Detects defects from a given image path.

---

## 🎯 Key Features

* Real-time defect detection
* Custom dataset training
* YOLO-based object detection
* Clean minimal structure
* GPU acceleration support
* Easy to deploy and modify

---

## 🏭 Applications

* Surface defect inspection
* Manufacturing quality control
* Metal sheet defect detection
* PCB inspection
* Industrial automation systems

---

## 👨‍💻 Author

**Naveen Kumar R**
Computer Vision & Real-Time Automation Developer

---

## 📜 License

This project is licensed under the MIT License.

---

⭐ If you find this project useful, consider giving it a star!
