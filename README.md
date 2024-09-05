# Roadlane-detection-yolo8l
Detecting roadlanes in images and videos using YOLO8l

This project uses YOLOv8 for detecting road lanes in images and videos. It supports training on custom datasets and real-time inference.

## Installation

1. Clone the repository:
   bash
   git clone https://github.com/your-username/road-lane-detection.git
   cd road-lane-detection
   

2. Install dependencies:
   bash
   pip install ultralytics opencv-python-headless matplotlib
   

## Training

1. Prepare your dataset and update the data.yaml file.
2. Train the model:
   python
   from ultralytics import YOLO
   model = YOLO('yolov8l.yaml')
   model.train(data='data.yaml', epochs=45, imgsz=640)
   

## Inference

Run detection on images or videos:
python
# Image inference
results = model.predict('path/to/image.jpg')
results.show()

# Video inference
results = model.predict('path/to/video.mp4', save=True)


## Results

- *mAP@0.5:* X%
- *mAP@0.5:0.95:* Y%
