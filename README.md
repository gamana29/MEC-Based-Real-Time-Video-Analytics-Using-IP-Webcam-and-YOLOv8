# 🚀 5G Standalone (SA) MEC-Based Real-Time Video Analytics using IP Webcam & YOLOv8
### ⚡ Edge AI Object Detection with 5G SA, MEC Server, Laptop & Mobile Camera

[![Python](https://img.shields.io/badge/Python-3.x-blue)]()
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green)]()
[![YOLOv8](https://img.shields.io/badge/Model-YOLOv8-red)]()
[![5G SA](https://img.shields.io/badge/Network-5G%20Standalone-blueviolet)]()
[![MEC](https://img.shields.io/badge/Deployment-MEC-yellow)]()
[![Edge AI](https://img.shields.io/badge/AI-Edge%20Computing-success)]()
[![Realtime](https://img.shields.io/badge/Mode-RealTime-orange)]()



---

# 📘 Project Overview

This project demonstrates a **5G Standalone (SA) Mobile Edge Computing (MEC)-based Real-Time Video Analytics System** powered by **YOLOv8** for high-speed object detection.

The application performs real-time object detection using either:

- 💻 Laptop Webcam
- 📱 Mobile Camera via IP Webcam

The captured video is processed locally on an **MEC Server (Laptop)**, enabling intelligent edge inference without relying on cloud computing.

By combining **5G Standalone architecture**, **Multi-access Edge Computing (MEC)**, and **Edge AI**, the project demonstrates how next-generation wireless networks can support latency-sensitive applications through local processing, reduced response times, and enhanced privacy.

---

# 📌 What is 5G Standalone (SA)?

**5G Standalone (SA)** is a complete 5G network architecture built on a dedicated 5G Core instead of depending on existing 4G infrastructure.

Key advantages include:

- Ultra-Low Latency
- Higher Network Reliability
- Massive Device Connectivity
- Network Slicing
- Native Support for Edge Computing (MEC)
- Better Performance for AI and IoT Applications

5G SA enables applications that require real-time communication, such as autonomous vehicles, smart factories, industrial automation, AR/VR, healthcare, and intelligent surveillance.

---

# 📌 What is MEC?

**Multi-access Edge Computing (MEC)** brings cloud computing capabilities closer to end users by processing data at the network edge instead of sending everything to centralized cloud servers.

### In this project:

- 📱 Camera captures live video
- 📡 Video is transmitted through a **5G Standalone (SA) enabled edge network** (or local test network)
- 💻 MEC Server receives the stream
- 🤖 YOLOv8 performs object detection locally
- ☁️ No cloud processing is required

This architecture minimizes latency while improving speed, efficiency, and data privacy.

---

# 🌐 System Architecture

```
          Camera Device
       (Laptop / Mobile)
                │
                │
        5G Standalone (SA)
           Communication
                │
                ▼
      ┌───────────────────┐
      │    MEC Server      │
      │     (Laptop)       │
      └───────────────────┘
                │
                ▼
      YOLOv8 Edge AI Inference
                │
                ▼
      Real-Time Object Detection
```

---

# 📌 System Flow

## 1️⃣ Data Source Layer

Input devices:

- 💻 Laptop Webcam
- 📱 Mobile Camera (IP Webcam)

Video frames are continuously generated.

---

## 2️⃣ Communication Layer

The camera stream is transmitted through a **5G Standalone (SA) network** or a local testing network.

For mobile streaming:

- Phone and MEC server remain connected through the same network
- IP Webcam streams live video
- MEC server receives the stream

---

## 3️⃣ MEC Layer

The laptop acts as the **MEC Server**.

Responsibilities:

- Receive video frames
- Execute YOLOv8 inference
- Process frames locally
- Generate detection results
- Display output in real time

Since computation happens at the network edge, cloud dependency is eliminated.

---

## 4️⃣ Edge AI Processing

Each incoming frame undergoes:

- Image acquisition
- Object detection
- Bounding box generation
- Confidence score prediction
- Object classification
- Result visualization

All inference is performed locally on the MEC server.

---

# 🖼 Project Demonstration

## System Interface

![Demo 1](https://github.com/user-attachments/assets/fca76f4a-ed04-4d22-aee6-902aaf092d99)

![Demo 2](https://github.com/user-attachments/assets/d8071cd6-8572-40a2-a252-ad9d6d6ab3be)

![Demo 3](https://github.com/user-attachments/assets/631ab9c9-08ab-4918-8435-160a795610a0)

---

# ⚙ Working Process

## Option 1: Laptop Webcam

- Start application
- Select option `1`
- Laptop webcam opens
- Live video captured
- YOLOv8 performs object detection
- Results displayed instantly

Example detected objects:

- Person
- Mobile Phone
- Bottle
- Laptop
- Chair
- Keyboard

---

## Option 2: Mobile Camera (IP Webcam)

Requirements:

- Phone and MEC server connected through the same network
- IP Webcam installed

Steps:

1. Launch IP Webcam
2. Start streaming
3. Copy stream URL
4. Enter URL in the application
5. Live video received by MEC server
6. YOLOv8 detects objects in real time

---

# 🖥 Overall Workflow

```
Camera
(Laptop / Mobile)
        │
        ▼
5G Standalone Network
        │
        ▼
MEC Edge Server
(Laptop)
        │
        ▼
YOLOv8 Inference Engine
        │
        ▼
Bounding Boxes + Labels
        │
        ▼
Real-Time Detection Output
```

---

# 💻 Code Flow

```python
1. Start Application

2. Load YOLOv8 Model

3. Ask User:
      Laptop Webcam
      or
      Mobile IP Webcam

4. Capture Video Stream

5. For Every Frame:

      Read Frame

      Run YOLOv8 Detection

      Draw Bounding Boxes

      Display Output

6. Exit Program
```

---

# ⚡ Performance Benefits

## Benefits of 5G SA + MEC

- Ultra-low latency processing
- Real-time AI inference
- High-speed communication
- Reduced network congestion
- Efficient bandwidth utilization
- Local data processing
- Enhanced privacy
- Cloud-independent operation
- Better scalability
- Faster response time

---

# 📊 MEC Advantages

Instead of:

```
Camera
      ↓
Cloud
      ↓
Detection
      ↓
User
```

The project follows:

```
Camera
      ↓
MEC Server
      ↓
Detection
      ↓
User
```

This significantly reduces inference latency.

---

# 🧪 Test Scenario 1

Input:

Laptop Webcam

Expected Output:

- Person
- Bottle
- Laptop
- Mobile Phone
- Keyboard
- Chair

---

# 🧪 Test Scenario 2

Input:

Mobile Camera using IP Webcam

Expected Output:

- Live mobile feed
- Continuous video
- Real-time object detection
- Dynamic bounding boxes
- Low latency inference

---

# 🛠 Technologies Used

- Python
- OpenCV
- YOLOv8
- Ultralytics
- Mobile Edge Computing (MEC)
- 5G Standalone (SA)
- Edge AI
- Computer Vision
- IP Webcam
- Linux / Windows
- Real-Time Video Analytics

---

# 📂 Code Snippets

## Load YOLO Model

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
```

---

## Laptop Webcam

```python
import cv2

cap = cv2.VideoCapture(0)
```

---

## Mobile Camera

```python
ip_url = "http://192.168.x.x:8080/video"

cap = cv2.VideoCapture(ip_url)
```

---

# 🚀 Future Enhancements

- Deploy on a real 5G Standalone Core Network
- Kubernetes-based MEC orchestration
- Docker container deployment
- Multi-camera analytics
- AI model optimization using TensorRT
- Network slicing support
- Edge-to-Cloud collaboration
- Remote MEC deployment
- Smart City surveillance integration
- Industrial IoT monitoring
- Vehicle detection and traffic analytics

---

# 🤝 Contributing

Contributions are welcome!

You can:

- Report Issues
- Suggest Features
- Improve Documentation
- Submit Pull Requests

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Made with ❤️ by Gamana**

**GitHub:** https://github.com/gamana29
