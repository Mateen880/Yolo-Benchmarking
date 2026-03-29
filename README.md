🚀 YOLO Performance Evaluation & Hyperparameter Optimization










A comprehensive framework for benchmarking and optimizing multiple YOLO (You Only Look Once) object detection models. This project evaluates YOLOv5, YOLOv8, and YOLOv12 across performance, accuracy, and efficiency metrics to identify the best model for real-time video processing.

📌 Table of Contents
Overview
Key Metrics
Project Structure
Experiments
Tech Stack
Setup & Usage
Outputs
Author
📖 Overview

This project is divided into two major components:

🔹 Model Benchmarking (Task #1)

Compares YOLO models based on:

⚡ Inference Speed
🧠 Detection Accuracy
💻 Hardware Utilization
🔹 Hyperparameter Optimization (Task #2)

Analyzes how changes in:

Learning Rate
Batch Size
Confidence & IoU Thresholds

affect model performance and stability.

📊 Key Metrics Tracked
Category	Metrics
⚡ Performance	FPS (Frames Per Second), Latency (ms)
🎯 Quality	mAP@0.5, mAP@0.95, Precision, Recall
💻 Hardware	GPU Utilization (%), CPU Utilization (%)
🔄 Stability	Bounding-box Stability, Temporal Consistency
📦 Physical	Model Size (MB)
🛠️ Project Structure
YOLO-Performance-Evaluation/
│
├── YOLO.ipynb                # Main notebook
├── /YOLO_Outputs             # Generated outputs
│   ├── videos/               # Annotated videos
│   ├── metrics.csv           # Performance results
│
├── /weights                  # Model weights
│   ├── yolov5su.pt
│   ├── yolov8n.pt
│   ├── yolo12n.pt
│
└── README.md
🧪 Sequential Experiments
Experiment	Model	Configuration	Purpose
Exp-1	YOLOv5	LR: 0.001, Batch: 16	Baseline
Exp-2	YOLOv8	LR: 0.0005	Convergence Stability
Exp-3	YOLOv12	Batch: 32, Img Size: 512	Speed Optimization
Exp-4	YOLOv8	Conf: 0.30, IoU: 0.55	Threshold Tuning
💻 Technical Stack
Framework: Ultralytics YOLO
Deep Learning: PyTorch
Computer Vision: OpenCV
Data Analysis: Pandas, NumPy
Environment: Google Colab (Tesla T4 GPU)
⚙️ Setup & Usage
1️⃣ Mount Google Drive
/content/drive/MyDrive/check.mp4
2️⃣ Install Dependencies
pip install ultralytics pynvml psutil
3️⃣ Run Notebook
YOLO.ipynb
📂 Outputs

All results are saved in:

/YOLO_Outputs/
Includes:
🎥 Annotated detection videos
📄 CSV file with full performance metrics
🌟 Key Highlights
Multi-model benchmarking (YOLOv5 vs YOLOv8 vs YOLOv12)
Real-time performance evaluation on video data
Hardware-aware analysis (GPU/CPU tracking)
Structured hyperparameter experimentation
Scalable and reproducible pipeline
👨‍💻 Author

Abdul Mateen
BS Artificial Intelligence Student
FAST University, Islamabad

⭐ Support

If you find this project useful, consider giving it a ⭐ on GitHub to support the work.
