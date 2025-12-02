# CV_Project
🚁🔥 Edge-Enabled Real-Time Fire & Multi-Class Human/Animal Detection From UAV Aerial Imagery
Real_Time Environmental Monitoring & Rescue Intelligence Using NVIDIA Jetson Nano

Authors:
Nayab Nazar • Bushra Naeem • Ayesha Hussain • Arbaaz Alam
Department of Electrical Engineering and Computer Science, NUST

📌 Overview

Wildfires, remote accidents, and natural disasters pose increasing threats to human life, wildlife, and ecosystems. Rapid detection of fire and trapped beings in inaccessible regions is crucial for effective rescue operations.

This project presents an edge enabled UAV system capable of real-time detection of fire, humans, and animals using deep learning models optimized for the NVIDIA Jetson Nano.

The system performs onboard inference,no internet or cloud required allowing fast, autonomous situational awareness during emergency missions.

⭐ Key Features

Real-Time Multi-Class Detection
Fire 🔥, Humans 🧍, and Animals 🐕 detected simultaneously.

Jetson Nano Edge Computing
Local inference ensures low latency and eliminates dependence on cloud networks.

Optimized Deep Learning Models
Lightweight YOLOv5 / YOLOv8 / GhostNet / CNN-ViT hybrids reviewed and benchmarked.

UAV Deployment Ready
Designed for integration with drone camera feeds.

High Efficiency
Operates within 5–10 W power limits on Jetson Nano.

🎯 Project Objectives

✔ Develop a unified detection model combining fire, human, and animal recognition
✔ Deploy on NVIDIA Jetson Nano for real time inference
✔ Analyze feasible model architectures from 11 verified research studies
✔ Perform fire intensity assessment + object localization
✔ Provide a complete UAV-based real time rescue framework

📚 Literature Review Summary

A total of 11 peer reviewed research papers were evaluated covering:

UAV fire detection

Wildlife monitoring

Embedded deep learning

Edge computing optimizations

Real time transformer CNN hybrids

Key Insights

YOLOv5/YOLOv8 dominate real time UAV detection tasks

Lightweight, attention-enhanced YOLO variants show 30–40% parameter reduction

CNN–Transformer hybrids provide high accuracy with fewer than 1M parameters

Edge hardware (Jetson Nano, Xavier NX, Orin) can achieve 18–32 FPS

📊 Literature Comparison Table
Authors (Year)	Model	Dataset	Accuracy / mAP	Device	FPS	Contribution
Shamta & Demir (2024)	YOLOv5/8 + RCNN	UAV RGB	96% acc	Jetson Nano	25 FPS	Real-time UAV fire detection
Lu et al. (2025)	FCMI-YOLO	Fire	+1.5% mAP	Nano/Xavier	32 FPS	Efficient edge YOLO
Chaturvedi et al. (2024)	CNN–ViT	Smoke	93–99% acc	Edge GPU	18 FPS	Ultra-light hybrid model
Zhu et al. (2025)	Improved YOLOv8	Fire	93.6% P	Edge GPU	+14% FPS	Dual-attention design
Nguyen et al. (2025)	WildLive	Animal	94% MOT	Jetson Orin	17 FPS	UAV wildlife tracking
Yang et al. (2023)	Ghost YOLOv5	Smoke	95% acc	Jetson Nano	27 FPS	Low-power GhostNet
Muhammad et al. (2018)	CNN	Fire video	96% acc	Embedded HW	30 FPS	Foundational baseline
🔍 Research Gaps Identified

Single-Task Bias
9/11 studies focused on single-class detection only.

Limited Multi-Class Real-Time Inference
High accuracy models slow down under edge constraints.

No Integrated Rescue Intelligence
No prior system combines:

Fire detection

Human detection

Animal detection

Fire intensity estimation

🧠 Proposed System Contribution

This project proposes a unified edge-deployed wildfire and rescue vision framework that:

🔧 1. Performs Multi-Class Detection

Fire

Humans

Animals

🚁 2. Runs Entirely Onboard the UAV

Jetson Nano performs all inference

Zero dependence on cloud systems

⚡ 3. Achieves Real-Time Performance

Target: 15–25 FPS on Jetson Nano

Using TensorRT + FP16/INT8 quantization

🔥 4. Includes Fire Intensity Assessment

Bounding-box heat scoring

Multi-level severity classification

🏗 System Design
Pipeline Overview

UAV captures live aerial imagery

Jetson Nano processes frames using optimized YOLO-based model

Fire, human, and animal detection performed in real time

Alerts transmitted to ground control

UAV Camera → Jetson Nano → Onboard Deep Learning Model → Detection Output → Alert System

🤖 Model Options Evaluated for Deployment
Technique 1 — YOLOv8n (Quantized)

Best real-time performance

Highly optimized for TensorRT

Good accuracy across all classes

Technique 2 — FCMI-YOLO

Reduced feature maps

Improved inference on edge hardware

Parameter-efficient

Technique 3 — Ghost-Enhanced YOLOv5

Lowest computational load

Suitable for low-power embedded devices

💻 Hardware Requirements
Component	Specification
Jetson Nano	472 GFLOPs, Maxwell GPU
RAM	4GB LPDDR4
Storage	32GB microSD
Power	5–10W
Camera	USB/CSI compatible
Cooling	Active heatsink + fan recommended
