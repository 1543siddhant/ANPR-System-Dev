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

# 🚀 Usage

## Command-Line Interface

Run the ANPR system on a single image:

```bash
python detect.py --source path/to/image.jpg
```

Run the system on a video stream:

```bash
python detect.py --source path/to/video.mp4
```

## Python API

Import and use the ANPR system in your Python scripts:

```python
from anpr_system import ANPR

anpr = ANPR(model_path='yolov8n.pt', ocr_lang='en')
result = anpr.process_image('path/to/image.jpg')
print(result)
```

# 📚 Theory Behind ANPR

## What Is ANPR?
Automatic Number Plate Recognition (ANPR) is a technology that uses optical character recognition (OCR) to read vehicle license plates. It captures images of vehicles and processes them to extract license plate numbers, enabling various applications such as traffic monitoring, law enforcement, and toll collection.

## Core Components
- **Image Acquisition**: Capturing high-quality images of vehicles using cameras.
- **License Plate Localization**: Identifying and isolating the license plate region within the image.
- **Character Segmentation**: Dividing the license plate region into individual characters.
- **Optical Character Recognition**: Recognizing the segmented characters to extract the license plate number.
- **Postprocessing**: Refining the extracted information for accuracy and usability.

## Challenges
- **Environmental Factors**: Variations in lighting, weather conditions, and occlusions can affect detection accuracy.
- **Plate Variations**: Differences in plate designs, fonts, and sizes across regions pose challenges for recognition.
- **Real-Time Processing**: Achieving high accuracy while maintaining real-time performance is computationally demanding.

## Applications
- **Law Enforcement**: Monitoring and enforcing traffic laws, identifying stolen vehicles, and tracking suspect movements.
- **Toll Collection**: Automating toll collection processes on highways and bridges.
- **Parking Management**: Managing access control and monitoring parking facilities.
- **Surveillance**: Enhancing security through vehicle tracking and monitoring.

## 🛠️ Customization
The system is designed to be easily customizable:

- **Model Selection**: Choose from various YOLOv8 models (e.g., `yolov8n.pt`, `yolov8s.pt`) based on performance and accuracy requirements.
- **OCR Configuration**: Specify the language for OCR using EasyOCR's supported languages.
- **Input Sources**: Process images or videos from local files, URLs, or camera streams.


## 📞 Contact
For support or inquiries, please contact:

- **Email**: siddhantpatil1543.com  
