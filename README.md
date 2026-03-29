🚀 YOLO Performance Evaluation & Hyperparameter Optimization

This project provides a comprehensive framework for benchmarking and optimizing various versions of the YOLO (You Only Look Once) object detection architecture. It evaluates YOLOv5, YOLOv8, and YOLOv12 across a suite of performance and quality metrics to determine the most efficient model for real-time video processing.

📌 Overview

The codebase is structured into two primary modules:

1. Model Benchmarking (Task #1)

A comparative analysis of YOLOv5, YOLOv8, and YOLOv12 based on:

Inference speed
Hardware utilization
Detection accuracy
2. Hyperparameter Optimization (Task #2)

A series of sequential experiments designed to observe how varying:

Learning rates
Batch sizes
Thresholds

impact model performance.

📊 Key Metrics Tracked

To ensure a holistic evaluation, the project tracks the following:

Category	Metrics
Performance	FPS (Frames Per Second), Latency (ms)
Quality	mAP@0.5, mAP@0.95, Precision, Recall
Hardware	GPU Utilization (%), CPU Utilization (%)
Stability	Bounding-box Stability, Temporal Consistency
Physical	Model Size (MB)
🛠️ Project Structure
🔹 Task 1: Comparative Benchmarking

This module:

Loads the following model weights:
yolov5su.pt
yolov8n.pt
yolo12n.pt
Processes the target video file: check.mp4
Outputs Generated:
🎥 Annotated Videos
Visual proof of detection for each model
📄 Performance CSV
A detailed summary of all technical metrics
🔹 Task 2: Sequential Experiments

Four distinct experiments are conducted to determine the optimal configuration:

Exp-1 (YOLOv5)
Baseline with:
Learning Rate: 0.001
Batch Size: 16
Exp-2 (YOLOv8)
Reduced Learning Rate:
0.0005 (to test convergence stability)
Exp-3 (YOLOv12)
Speed optimization with:
Batch Size: 32
Image Size: 512
Exp-4 (YOLOv8)
Threshold tuning:
Confidence: 0.30
IoU: 0.55
💻 Technical Stack
Framework: Ultralytics YOLO
Deep Learning: PyTorch
Computer Vision: OpenCV
Data Analysis: Pandas, NumPy
Environment: Google Colab with Tesla T4 GPU support
📥 Setup & Usage
1. Mount Google Drive

Ensure your video file is located at:

/content/drive/MyDrive/check.mp4
2. Install Dependencies
pip install ultralytics pynvml psutil
3. Run the Notebook

Execute:

YOLO.ipynb
4. Outputs

Results will be generated in:

/YOLO_Outputs
👨‍💻 Author

Abdul Mateen
BS Artificial Intelligence Student
FAST University, Islamabad
