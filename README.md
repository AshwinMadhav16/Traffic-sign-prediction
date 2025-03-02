# Traffic-sign-prediction
# Traffic Sign Detection using YOLOv8

## Project Overview
This project implements real-time traffic sign detection using the YOLOv8 model. It captures video frames from a webcam and processes them using a trained YOLO model to detect and annotate traffic signs.

## Features
- Uses YOLOv8 for real-time traffic sign detection.
- Captures frames from a webcam.
- Annotates detected traffic signs in the video stream.
- Allows exiting the detection loop by pressing the 'q' key.

## Requirements
Ensure you have the following dependencies installed:

- Python 3.7+
- OpenCV (`cv2`)
- Ultralytics YOLO (`ultralytics`)
- Torch (`torch`)

Install dependencies using:
```bash
pip install ultralytics opencv-python torch
```

## File Structure
- `trafficsign.py`: Main script for real-time traffic sign detection.
- `trafficsign.pt`: Pre-trained YOLOv8 model file.
- `trafficlightdetection.ipynb`: Jupyter notebook for testing and experimentation.

## How to Run
1. Ensure the `trafficsign.pt` model file is present at the specified path in `trafficsign.py`.
2. Run the detection script:
   ```bash
   python trafficsign.py
   ```
3. If the webcam is accessible, the script will display real-time detection results.
4. Press 'q' to exit the detection window.

## Troubleshooting
- **Model file not found:** Verify the path to `trafficsign.pt` in `trafficsign.py`.
- **Webcam not accessible:** Ensure your webcam is properly connected and available.
- **Dependencies missing:** Run `pip install -r requirements.txt` if you have a `requirements.txt` file.

## Future Improvements
- Expand detection to different traffic sign types.
- Improve accuracy by training on a larger dataset.
- Deploy as a web-based application.

## License
This project is for educational purposes. Modify and use it as needed.




