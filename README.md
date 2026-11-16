Road Traffic Signs Detection using CV & DL

Detecting and classifying 21 types of road traffic signs with Computer Vision and Deep Learning, using YOLOv8s-OBB (oriented bounding boxes).

Introduction

Traffic signs keep vehicles and pedestrians moving safely and in order. As AI becomes part of transportation, especially in autonomous vehicles and driver-assistance systems, recognizing road signs automatically has become essential.

Aims and Objectives
Build an accurate and efficient system that detects and classifies 21 classes of road traffic signs.
Support intelligent transportation applications such as autonomous driving, road safety systems, and driver assistance.
Dataset
Step	Details
Source	Kaggle
Cleaning	Duplicates removed with imagededup (Perceptual Hashing / PHash), leaving 3,443 unique images
Annotation	Roboflow, 21 classes, exported in YOLOv8-OBB format
Preprocessing	Resized to 640×640 (stretch)
Augmentation	Blur (up to 2.5 px) to simulate camera motion, low resolution, fog, and glare
Final size	5,286 images after augmentation
Split	70% train / 15% validation / 15% test
Model and Training
Setting	Value
Model	yolov8s-obb.pt
Library	Ultralytics
Epochs	70
Image size	640×640

Why YOLOv8s-OBB?

Built-in support for detection, classification, and segmentation
Ready for real-time deployment
Pretrained weights allow transfer learning
Fast inference
Results

YOLOv8s-OBB outperformed Faster R-CNN and SSD in both accuracy and inference speed.

Metric	Score
mAP@50	97.7%
Precision	97.4%
Recall	96.9%

Sample test confidence: stop 95.0%, speed_limit_60 91.0%.

Challenges
Limited hardware resources (low GPU capability)
Limited time
Learning new tools and concepts
Adapting to realistic conditions
Project Files
ROAD_TRAFFIC_SIGNS_DETECTION___WITH_CV___DL.pptx: project presentation
Authors
Malek Alhaj &
Renad Omar

Supervised by Dr. Nancy Alajarmeh.
