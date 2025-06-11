# End-to-End-Logo-Recognition-System


## Overview

This project is a complete pipeline for detecting brand logos from images using a state-of-the-art object detection model. The goal is to create a **Logo-Recognition-System** capable of generalizing to logos even outside its training set. We used the **FlickrLogos-27** dataset and **YOLOv8** to build this system.

This repository contains:
- Model Training Code, Pretrained Weights, Inference Pipeline
- UI for Live Demo
- Setup Instructions

---

## Why YOLOv8 + FlickrLogos-27?

### Dataset: FlickrLogos-27
- Contains real-world images of 27 different logos.
- Logos are annotated with bounding boxes.
- The dataset has a diverse background, making it suitable for generalization.
- Well-suited for transfer learning in detection models.

### ⚙️ Model: YOLOv8
- Chosen for its balance between **speed** and **accuracy**.
- Supports export to ONNX/TFLite for real-time applications.
- Easy integration with Ultralytics’ training API.

---

## Training & Results

We trained YOLOv8 using transfer learning:
- **Base Model**: `yolov8n.pt`
- **Epochs**: 100
- **Batch Size**: 16
- **Optimizer**: SGD
- **Validation mAP**: ~0.72 on held-out validation set

The model performs well on unseen logos and cluttered scenes.

---

##  Running on
 public URL: https://acc24cfe2072740cc0.gradio.live

### ✅ Requirements

```bash
pip install -r requirements.txt
