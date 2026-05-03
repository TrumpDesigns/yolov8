YOLOv8 Weed Detection & Classification
An optimized deep learning model for real-time weed detection in agricultural fields

Overview
Weed infestation is one of the most significant threats to crop yields globally, yet most detection methods remain manual, slow, and imprecise. This project develops and optimizes a YOLOv8-based convolutional neural network capable of detecting and classifying 15 weed species in real-time from field imagery, enabling targeted herbicide application, reduced chemical usage, and lower operational costs for farmers.
This research was completed as an MSc Information Technology thesis at the National Open University of Nigeria (2024), supervised by Dr. James Kehinde Ayeni.

The Problem
Traditional weed management relies on uniform herbicide application across entire fields, wasteful, expensive, and environmentally damaging. Accurate automated detection would allow farmers to treat only affected areas. The challenge is building a model that is both accurate and lightweight enough to run on resource-constrained field hardware like drones and field robots.

Approach

Model: YOLOv8 (You Only Look Once, version 8), a state-of-the-art real-time object detection architecture
Dataset: 15 weed species commonly found in agricultural settings, sourced via Roboflow, curated across varied growth stages, lighting conditions, and field backgrounds
Technique: Transfer learning using pre-trained weights to accelerate training and improve generalization
Optimization: Confidence threshold analysis and cross-model benchmarking to balance accuracy and computational efficiency


Results
MetricScoremAP@0.591.7%mAP@0.5:0.9580.0%
The model outperformed existing benchmark models on both precision and recall, demonstrating strong generalizability across real-world field conditions.

Repository Structure
yolov8-weed-detection/
├── train.py              # Model training script
├── detect.py             # Run inference on new images
├── requirements.txt      # Dependencies
├── data/
│   └── dataset.yaml      # Dataset configuration
├── results/
│   └── metrics.csv       # Training and validation metrics
└── thesis/
    └── Komolafe_MSc_Thesis_2024.pdf

Getting Started
Install dependencies
bashpip install -r requirements.txt
Run detection on an image
bashpython detect.py --source your_image.jpg
Train from scratch
bashpython train.py --data data/dataset.yaml --epochs 100

Dataset
Dataset sourced from Roboflow. The dataset.yaml file contains the download configuration. A Roboflow account may be required to access the full dataset.

Broader Implications
Beyond yield improvement, this work raises questions relevant to AI governance in agricultural settings, particularly around model reliability and trust when AI systems are deployed in low-infrastructure, high-stakes environments. How do farmers verify that the model advising their decisions is performing as intended? These questions inform ongoing interest in technical AI governance and model authenticity guarantees.

Author
Michael Olorunfemi Komolafe
MSc Information Technology, National Open University of Nigeria
Agriculture Operations Manager | AgriTech Researcher
Lagos, Nigeria
mikel.komolafe@gmail.com
Portfolio

Citation
Komolafe, M.O. (2024). An Optimized Convolutional Neural Network for Detection
and Classification of Weeds. MSc Thesis, National Open University of Nigeria.
