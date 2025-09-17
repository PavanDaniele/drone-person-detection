# drone-person-detection

## Drone-based Person Detection on Jetson Nano

**_Summary:_** All relevant data is provided by Kaggle and processed to clean and prepare it for model training.: Real-time person detection from UAV RGB imagery in natural terrains, optimized for Jetson Nano with lightweight detectors (YOLOv8n/YOLOv11n, EfficientDet, MobileNet-SSD) and a clean data pipeline.

This project targets search-and-rescue scenarios, detecting people from aerial images (top-down and oblique views, 20–120 m AGL) in non-crowded natural environments. We curate and merge aerial datasets (e.g., SARD, HERIDA) into a unified single-class “person” dataset, then fine-tune compact detectors in PyTorch and deploy them with TensorRT on Jetson Nano. The repository includes tools for dataset cleaning, VOC→YOLO/COCO conversion, letterbox resizing, training/evaluation, and on-device benchmarking.

---
**Key features**

- **Embedded-first models:** YOLOv8n / YOLOv11n.
- **Data pipeline:** merge & clean aerial datasets, unify labels to person, convert Pascal VOC → YOLO/COCO, letterbox resize.
- **Training in PyTorch:** reproducible scripts/notebooks, controlled augmentations for aerial viewpoints.
- **Deployment:** ONNX → TensorRT (.engine) with inference scripts for Jetson Nano.
- **Metrics:** mAP@0.5:0.95, Precision, Recall, F1, plus FPS, latency, throughput measured on-device.
- **Reproducibility:** the repo links to the original datasets; run the provided notebooks to regenerate the cleaned/merged set locally.

- **Use cases:** UAV search-and-rescue, wilderness monitoring, low-power edge CV.

---
## Datasets & Workspace

- Worked primarily with SARD and HERIDA (merged into the single-class AERALIS dataset).
- Data are stored on Google Drive and processed in Google Colab.

**Access (read-only):** [Google Drive folder](https://drive.google.com/drive/folders/1MlSMRVPPiz65_2jOrVj8LDbIcJ8NPclq?usp=drive_link)
