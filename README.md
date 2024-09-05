# Roadlane-detection-yolo8l
Detecting roadlanes in images and videos using YOLO8l

This project uses YOLO8l for detecting road lanes in images and videos. It supports training on custom datasets and real-time inference.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/GayathriDeviRV/Roadlane-detection-yolo8l.git
   cd Roadlane-detection-yolo8l
   ```

2. Install dependencies:
   ```bash
   pip install ultralytics opencv-python-headless matplotlib
   ```

## Dataset
The ROAD MARK Dataset contains 2,892 annotated images and videos focused on detecting and classifying road markings and objects like lane lines, arrows, and traffic signs. It covers diverse road scenarios and is split into Train, Validation, and Test sets, ideal for road safety model development.
[ROAD MARK Dataset](https://www.kaggle.com/datasets/pkdarabi/road-mark-detection/data)


## Training

1. Prepare your dataset and update the data.yaml file.
2. Train the model:
   ```python
   from ultralytics import YOLO
   model = YOLO('yolov8l.yaml')
   model.train(data='data.yaml', epochs=45, imgsz=640)
   ```

## Inference

Run detection on images or videos:
```python
# Image inference
results = model.predict('path/to/image.jpg')
results.show()

# Video inference
results = model.predict('path/to/video.mp4', save=True)
```

## Results

- *mAP@0.5:* X%
- *mAP@0.5:0.95:* Y%
