# Road Lane Detection using YOLOv8

## Overview
This project focuses on detecting road lanes using the YOLOv8 model. Road lane detection is a critical task in autonomous driving and traffic management, where detecting lane lines accurately can help improve road safety and navigation.

The dataset includes annotated images capturing various road scenarios such as highways, urban streets, and rural areas. The goal is to detect objects like lane lines, crosswalks, and other relevant road markings.

## Dataset
- **Samples**: 2,892 annotated images
- **Classes**: Lane lines, crosswalks, arrows, etc.
- **Split**: Train, Validation, Test
- **Link**: [ROAD LANE Dataset](https://www.kaggle.com/datasets/pkdarabi/road-mark-detection)

The dataset is divided into three parts—Train, Validation, and Test—ensuring a balanced distribution for effective training and evaluation.

## Model
We employed **YOLOv8** to detect road lanes and markings. The model was trained for 45 epochs with an image size of 640x640, resulting in strong detection performance:

- **mAP@0.5**: 0.90
- **mAP@0.5:0.95**: 0.71

## Installation and Setup
To run the project locally, follow these steps:

1. Install dependencies:
    ```bash
    pip install ultralytics opencv-python-headless
    ```

2. Train the YOLOv8 model:
    ```python
    from ultralytics import YOLO
    model = YOLO('yolov8l.yaml')
    model.train(data='data.yaml', epochs=45, imgsz=640)
    ```

## Results
The model effectively detects road lanes across various conditions, providing accurate predictions for lane lines, crosswalks, and directional arrows. Example results from the validation set show promising performance with high precision in both urban and highway environments.
