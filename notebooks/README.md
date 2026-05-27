# Notebooks

## YOLOv8n_training_notebook.ipynb

YOLOv8n training notebook for Late Blight crop disease detection.

### How to run
1. Open in Google Colab
2. Set runtime to GPU (Runtime → Change runtime type → T4 GPU)
3. Upload your dataset zip when prompted
4. Run cells in order top to bottom

### What it does
- Installs Ultralytics YOLOv8
- Uploads and extracts the annotated dataset
- Trains YOLOv8n for 50 epochs at 512×512
- Evaluates using Precision, Recall, mAP@0.5, mAP@0.5-95
- Downloads best.pt weights on completion

### Results achieved

| Metric | Value |
|--------|-------|
| mAP@0.5 | 0.710 |
| mAP@0.5-95 | 0.570 |
| Precision | 0.807 |
| Recall | 0.675 |

### Requirements
- Google account (for Colab)
- Dataset: Healthy_Leaf and Late_Blight annotated images in YOLO format
- GPU runtime (T4 recommended)
