# Traffic Sign Detection using YOLOv8 

![Screenshot (2)](https://github.com/user-attachments/assets/2abd2fdd-36c6-48f1-9ff8-e5968aa00d5e)

## Overview
This project implements real-time traffic sign detection using the YOLOv8 object detection model. The model is trained on a custom dataset and deployed for live webcam detection.

## Features
- Train a YOLOv8 model on a custom traffic sign dataset
- Perform real-time traffic sign detection using a webcam
- Save and export the trained model for further use

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/traffic-sign-detection.git
cd traffic-sign-detection
```

### 2. Install Dependencies
Ensure you have Python installed, then install the required libraries:
```bash
pip install ultralytics roboflow opencv-python
```

## Training the Model
### Download the dataset using Roboflow:
```python
from roboflow import Roboflow
rf = Roboflow(api_key="your_api_key")
project = rf.workspace("my-jvrqh").project("traffic_sign-gv5rp-t0k2e-4y3sn")
version = project.version(2)
dataset = version.download("yolov8")
```

### Train YOLOv8:
```bash
yolo task=detect mode=train model=yolov8n.pt data=Traffic_Sign-2/data.yaml epochs=25 imgsz=640 batch=8
```

## Running Real-Time Detection
Ensure you have a trained model (`trafficsign.pt`) stored in the correct path, then run the detection script:
```bash
python trafficsign.py
```

### Expected Output
The script will open the webcam and detect traffic signs in real time.
- Press `q` to exit the application.

## Model Export
To save and zip the trained model:
```bash
cp /content/runs/detect/train/weights/best.pt /content/my_model/trafficsign.pt
zip -r my_model.zip my_model
```

## Troubleshooting
- **Model file not found:** Ensure `trafficsign.pt` is in the correct directory.
- **Webcam access error:** Check if another application is using the webcam.
- **Python dependencies issue:** Run `pip install -r requirements.txt` to reinstall dependencies.

## License
This project is open-source and available under the MIT License.

## Author
**Ashwin Madhav A**

## Acknowledgments
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- [Roboflow](https://roboflow.com) for dataset management.





