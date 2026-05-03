# YOLOv8 Weed Detection & Classification

> An optimized deep learning model for real-time weed detection in agricultural fields

![Python](https://img.shields.io/badge/Python-3.10-blue) ![YOLOv8](https://img.shields.io/badge/Model-YOLOv8-brightgreen) ![mAP](https://img.shields.io/badge/mAP@0.5-91.7%25-success) ![License](https://img.shields.io/badge/Dataset%20License-CC%20BY%204.0-lightgrey)

---

## Overview

Weed infestation is one of the most significant threats to crop yields globally, yet most detection methods remain manual, slow, and imprecise. This project develops and optimizes a YOLOv8-based convolutional neural network capable of detecting and classifying 15 weed species in real-time from field imagery, enabling targeted herbicide application, reduced chemical usage, and lower operational costs for farmers.

This research was completed as an MSc Information Technology thesis at the National Open University of Nigeria (2024), supervised by Dr. James Kehinde Ayeni.

---

## The Problem

Traditional weed management relies on uniform herbicide application across entire fields, wasteful, expensive, and environmentally damaging. Accurate automated detection would allow farmers to treat only affected areas. The challenge is building a model that is both accurate and lightweight enough to run on resource-constrained field hardware like drones and field robots.

---

## Approach

| Component | Detail |
|---|---|
| Model | YOLOv8n (You Only Look Once, version 8) |
| Dataset | 15 weed species via Roboflow (CC BY 4.0) |
| Training | 100 epochs, batch size 16, image size 640px |
| Technique | Transfer learning with pre-trained weights |
| Optimizer | Auto (SGD-based), lr0=0.01 |
| Platform | Google Colab |

---

## Results

| Metric | Score |
|---|---|
| mAP@0.5 | **91.7%** |
| mAP@0.5:0.95 | **80.0%** |

The model outperformed existing benchmark models on both precision and recall across all 15 weed classes.

![Results](https://raw.githubusercontent.com/TrumpDesigns/yolov8/main/results/results.png)
![PR Curve](https://raw.githubusercontent.com/TrumpDesigns/yolov8/main/results/PR_curve.png)
![Confusion Matrix](https://raw.githubusercontent.com/TrumpDesigns/yolov8/main/results/confusion_matrix_normalized.png)

---

## Weed Classes

`carpetweeds` `crabgrass` `eclipta` `goosegrass` `morningglory` `nutsedge` `palmeramaranth` `pricklysida` `purslane` `ragweed` `sicklepod` `spottedspurge` `spurredanoda` `swinecress` `waterhemp`

---

## Repository Structure
yolov8-weed-detection/
├── Weed_detection.ipynb      # Training and inference notebook
├── requirements.txt          # Dependencies
├── data/
│   └── dataset.yaml          # Dataset configuration
├── results/
│   ├── results.csv
│   ├── results.png
│   ├── PR_curve.png
│   └── confusion_matrix_normalized.png
├── thesis/
│   └── Komolafe_MSc_Thesis_2024.pdf
└── README.md

---

## Getting Started

**1. Clone the repository**
```bash
git clone https://github.com/trumpdesigns/yolov8-weed-detection.git
cd yolov8-weed-detection
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Open the notebook**

Recommended: open `Weed_detection.ipynb` directly in [Google Colab](https://colab.research.google.com/) — no local GPU required.

```bash
jupyter notebook Weed_detection.ipynb
```

---

## Dataset

Dataset sourced from [Roboflow Universe](https://universe.roboflow.com/dronepag/weed_detection-rrlf8-xxodx/dataset/1), licensed under CC BY 4.0. The `data/dataset.yaml` file contains the full configuration. A free Roboflow account may be required to download the full dataset.

---

## Broader Implications

Beyond yield improvement, this work raises questions relevant to AI governance in agricultural settings, particularly around model reliability and trust when AI systems are deployed in low-infrastructure, high-stakes environments. How do farmers verify that the model advising their decisions is performing as intended? These questions inform ongoing interest in technical AI governance and model authenticity guarantees.

---

## Author

**Michael Olorunfemi Komolafe**
MSc Information Technology, National Open University of Nigeria
Agriculture Operations Manager | AgriTech Researcher | Lagos, Nigeria

[![Email](https://img.shields.io/badge/Email-mikel.komolafe%40gmail.com-red)](mailto:mikel.komolafe@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-trumpdesigns-black)](https://github.com/trumpdesigns)

---

## Citation

```bibtex
@mastersthesis{komolafe2024weed,
  author    = {Komolafe, Michael Olorunfemi},
  title     = {An Optimized Convolutional Neural Network for Detection and Classification of Weeds},
  school    = {National Open University of Nigeria},
  year      = {2024},
  month     = {October}
}
```
