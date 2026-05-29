# Real-Time Crop Disease Detection & Targeted Pesticide Dispensing

Autonomous agricultural robot using YOLOv8n + Raspberry Pi for
real-time Late Blight detection and targeted pesticide spraying,
no chemicals wasted on healthy plants.

## Status
🔧 Phase 1 Complete - Model trained and evaluated.
   Physical hardware build in progress (Phase 2).

## Training Notebook
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Arindam111123/intelligent-agro-tronic-weeder/blob/main/notebooks/YOLOv8n_training_notebook.ipynb)

Full training pipeline, evaluation results, and visualizations:
notebooks/YOLOv8n_training_notebook.ipynb

## Problem
Traditional pesticide spraying covers entire fields blindly, causing:
- Chemical overuse and soil degradation
- High cost for farmers
- Environmental contamination

This robot detects only infected leaves and sprays only those spots.

## Model Performance (YOLOv8n)

| Metric | Value |
|--------|-------|
| mAP@0.5 | 0.710 |
| mAP@0.5-95 | 0.570 |
| Precision | 0.807 |
| Recall | 0.675 |
| Training images | 3,505 |
| Validation images | 528 |
| Epochs | 50 |
| Image size | 512×512 |

## How It Works

1. Robot moves through the field on a 4WD platform
2. Camera continuously captures leaf images
3. YOLOv8n model on Raspberry Pi detects Late Blight in real time
4. On detection, Raspberry Pi signals ESP32 to trigger spray mechanism
5. Pesticide is sprayed only on the infected region

## Hardware

| Component | Role |
|-----------|------|
| Raspberry Pi 4B | Image processing + YOLOv8n inference |
| Arduino Uno + L298N | 4WD robot movement control |
| ESP32 | Spraying system control |
| R385 Diaphragm Pump | Pesticide flow |
| Solenoid Valve | Electronic spray switch |
| 1.2 MPa Pressure Transducer | Pressure monitoring |
| Pi Camera Module | Live leaf image capture |

## Dataset & Training

- **Dataset**: Kaggle PlantDisease + agricultural sources
- **Classes**: Healthy_Leaf, Late_Blight
- **Annotation tool**: LabelImg
- **Platform**: Google Colab, NVIDIA Tesla T4 GPU
- **Framework**: Ultralytics YOLOv8

## Tech Stack

`Python` `YOLOv8` `Raspberry Pi` `Arduino` `ESP32` `OpenCV` `Google Colab`

## Academic Context

**B.E. Project : Electronics & Communication Engineering**
BMS Institute of Technology and Management, Bengaluru
Visvesvaraya Technological University | 2025–26
Guide: Dr. Shivarudraiah B

## Team

| Name | USN |
|------|-----|
| Ananya Gladys | 1BY23EC001 |
| Amogha T Maiya | 1BY23EC013 |
| Arindam Kashyap | 1BY23EC021 |
| Kushagra Sinha | 1BY23EC060 |
