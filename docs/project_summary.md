# Project Summary

## Title
Real-Time Image-Based Detection and Targeted Pesticide 
Dispensing for Crop Leaf Diseases

## Institution
BMS Institute of Technology and Management, Bengaluru
Department of Electronics and Communication Engineering
VTU, 2025-26

## Guide
Dr. Shivarudraiah B, Assistant Professor, Dept. of ECE

## Problem Statement
Conventional pesticide spraying covers entire fields 
blindly, causing chemical overuse, soil degradation, 
and environmental contamination. Manual disease 
detection is slow, unreliable, and unscalable for 
large farms.

## Solution
An AI-powered autonomous robot that:
- Detects Late Blight disease in real time using YOLOv8n
- Sprays pesticide ONLY on infected leaf regions
- Navigates the field autonomously on a 4WD platform

## Key Results

| Model    | mAP@0.5 | mAP@0.95 | F1 Score |
|----------|---------|----------|----------|
| YOLOv8n ✅ | 0.707   | —        | 0.71     |
| YOLOv5n  | 0.703   | —        | 0.73     |

- Healthy_Leaf Average Precision: ~0.994 (both models)
- YOLOv8n selected for better real-time stability

## Hardware Components

| Component | Role |
|-----------|------|
| Raspberry Pi 4B | Image processing + YOLOv8n inference |
| Arduino Uno + L298N | 4WD robot movement control |
| ESP32 | Spraying system control |
| R385 Diaphragm Pump | Pesticide flow |
| Solenoid Valve | Electronic spray switch |
| 1.2 MPa Pressure Transducer | Pressure monitoring |
| Pi Camera Module | Live leaf image capture |

## Training Details
- Dataset: Kaggle PlantDisease + agricultural sources
- Annotation: LabelImg (Healthy_Leaf / Late_Blight)
- Platform: Google Colab, NVIDIA Tesla T4 GPU
- Epochs: 50 | Image size: 512×512
- Framework: Ultralytics YOLO

## Future Scope
- Expand dataset for multiple crop diseases
- Add GPS, soil moisture, and obstacle detection sensors
- Full autonomous navigation without remote control
- Night-time detection using infrared imaging
