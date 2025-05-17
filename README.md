# 🚗 Automatic Number Plate Recognition (ANPR) System

## Overview
This repository presents an advanced Automatic Number Plate Recognition (ANPR) system designed to detect and extract license plate information from vehicle images. Leveraging cutting-edge technologies such as **Ultralytics YOLOv8** for object detection and **EasyOCR** for optical character recognition, this system offers high accuracy and efficiency in real-world applications.

---

## 🔧 Features
- **High-Accuracy Detection**: Utilizes Ultralytics YOLOv8, a state-of-the-art object detection model, to accurately identify license plates in various conditions.
- **Robust OCR Integration**: Employs EasyOCR to extract textual information from detected license plates, supporting multiple languages.
- **Flexible Input Handling**: Capable of processing images from various sources, including local files, URLs, and video streams.
- **Real-Time Processing**: Optimized for real-time performance, suitable for applications like traffic monitoring and surveillance.
- **Easy Deployment**: Designed with user-friendly configuration and deployment in mind.

---

## 🧠 How It Works

The ANPR system operates through a multi-stage pipeline:

1. **Object Detection**: YOLOv8 detects potential license plate regions within input images.
2. **Preprocessing**: Detected regions are cropped and preprocessed to enhance OCR accuracy.
3. **Optical Character Recognition**: EasyOCR extracts textual information from the preprocessed regions.
4. **Postprocessing**: Extracted text is cleaned and formatted for output.

This approach ensures high accuracy and robustness, even under challenging conditions such as varying lighting and occlusions.

---

## ⚙️ Installation

### Prerequisites
- Python 3.8+
- PyTorch 1.7+
- CUDA (for GPU acceleration)

### Setup

Clone the repository:
```bash
git clone https://github.com/yourusername/anpr-system.git
cd anpr-system
```
Install dependencies:
```bash
pip install -r requirements.txt
```
Download the YOLOv8 model weights:
```bash
python -c "from ultralytics import YOLO; YOLO('yolov8n.pt')"
```


