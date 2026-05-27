# Notebooks

## late_blight_yolov8n.ipynb

YOLOv8n training notebook for Late Blight crop disease detection.

### How to run
1. Open in Google Colab
2. Set runtime to GPU (Runtime → Change runtime type → T4 GPU)
3. Upload your dataset zip when prompted
4. Run cells in order top to bottom

### What it does
- Installs Ultralytics YOLO
- Uploads and extracts the annotated dataset
- Trains YOLOv8n for 50 epochs at 512×512
- Evaluates using Precision, Recall, mAP@0.5, mAP@0.95
- Downloads best.pt weights on completion

### Requirements
- Google account (for Colab)
- Dataset: Healthy_Leaf and Late_Blight annotated images in YOLO format
- GPU runtime (T4 recommended)

### Results achieved
| Metric | Value |
|--------|-------|
| mAP@0.5 | 0.707 |
| F1 Score | 0.71 |
| Healthy_Leaf AP | 0.994 |
