
# Real-Time Crop Disease Detection & Targeted Pesticide Dispensing

Autonomous agricultural robot using YOLOv8n + Raspberry Pi for 
real-time Late Blight detection and targeted pesticide spraying — 
no chemicals wasted on healthy plants.

## Status
🔧 Phase 1 Complete — Model trained and evaluated.
   Physical hardware build in progress (Phase 2)


## Problem
Traditional pesticide spraying covers entire fields blindly, causing:
- Chemical overuse and soil degradation
- High cost for farmers
- Environmental contamination

This robot detects only infected leaves and sprays only those spots.

## Model Performance

| Model    | mAP@0.5 | F1 Score | Confidence |
|----------|---------|----------|------------|
| YOLOv8n ✅ | 0.707   | 0.71     | 0.308      |
| YOLOv5n  | 0.703   | 0.73     | 0.294      |

Both models achieved ~0.994 Average Precision on healthy leaf detection.
YOLOv8n selected for better real-time inference stability.

## Hardware

- **Raspberry Pi 4B** — image processing + YOLOv8n inference
- **Arduino Uno + L298N** — 4WD robotic platform control  
- **ESP32** — spraying system control
- **R385 Diaphragm Pump + Solenoid Valve + Nozzle** — precision dispensing
- **1.2 MPa Pressure Transducer** — pressure monitoring

## How It Works

1. Robot moves through the field on a 4WD platform
2. Camera continuously captures leaf images
3. YOLOv8n model running on Raspberry Pi detects Late Blight in real time
4. On detection, Raspberry Pi signals ESP32 to trigger the spray mechanism
5. Pesticide is sprayed only on the infected region

## Dataset & Training

- **Dataset**: Kaggle PlantDisease + agricultural sources
- **Annotation tool**: LabelImg (Healthy_Leaf / Late_Blight classes)
- **Training platform**: Google Colab with NVIDIA Tesla T4 GPU
- **Epochs**: 50 | **Image size**: 512×512
- **Framework**: Ultralytics YOLO

## Tech Stack

`Python` `YOLOv8` `YOLOv5` `Raspberry Pi` `Arduino` `ESP32` `OpenCV` `Google Colab`

## Academic Context

**B.E. Project — Electronics & Communication Engineering**  
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
