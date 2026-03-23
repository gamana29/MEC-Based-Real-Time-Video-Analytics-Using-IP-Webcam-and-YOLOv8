# 🚀 MEC-Based Real-Time Video Analytics using IP Webcam & YOLOv8  
### ⚡ Edge AI Object Detection with Laptop & Mobile Camera

[![Python](https://img.shields.io/badge/Python-3.x-blue)]()
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green)]()
[![YOLOv8](https://img.shields.io/badge/Model-YOLOv8-red)]()
[![Edge AI](https://img.shields.io/badge/Deployment-MEC-yellow)]()
[![Realtime](https://img.shields.io/badge/Mode-RealTime-orange)]()

---

## 📘 **Project Overview**

This project demonstrates a **Mobile Edge Computing (MEC)-based real-time video analytics system** using **YOLOv8 object detection**.

It enables real-time object detection using:
- 💻 Laptop Webcam  
- 📱 Mobile Camera via IP Webcam  

👉 All processing is done locally on the **edge device (laptop)** — ensuring **low latency, high speed, and privacy**.

---

## 📌 **What is MEC? (Simple Explanation)**

**MEC (Mobile Edge Computing)** means:
👉 Processing data **near the source (edge)** instead of sending it to the cloud.

### ✅ In This Project:
- 📱 Phone → Captures video  
- 💻 Laptop → Processes using YOLOv8  
- ☁️ No cloud → Faster + Secure  

👉 This is a real-world example of **Edge AI + MEC**

---

## 🌐 **System Flow**

### **1️⃣ Data Source Layer (Input)**
- 💻 Laptop Webcam  
- 📱 Mobile Camera (IP Webcam)  

👉 Video frames are generated here.

---

### **2️⃣ Edge Device (MEC Node)**
👉 Laptop acts as **MEC server**

- Runs Python script  
- Loads YOLOv8 model  
- Processes frames locally  

📌 No cloud → Low latency inference

---

### **3️⃣ Communication Layer (IP Webcam Mode)**

👉 Required only for mobile camera

- Phone & laptop must be on **same WiFi network**  
- Phone streams video  
- Laptop receives via URL  


---

### **4️⃣ Edge Processing (Core Logic)**

For each frame:
- Capture frame  
- Run YOLOv8 detection  
- Draw bounding boxes  
- Label detected objects  

👉 Fully local processing (Edge AI)

---

## 🖼️ **Project Demo**

### 📍 System Interface & Output

![Demo 1](https://github.com/user-attachments/assets/fca76f4a-ed04-4d22-aee6-902aaf092d99)
![Demo 2](https://github.com/user-attachments/assets/d8071cd6-8572-40a2-a252-ad9d6d6ab3be)
![Demo 3](https://github.com/user-attachments/assets/631ab9c9-08ab-4918-8435-160a795610a0)

---

## ⚙️ **Working Explanation**

### 🔹 Option 1: Laptop Webcam
- Select `1`
- Laptop camera opens  
- Real-time detection starts  

#### ✅ Example:
- Phone → `"phone"`  
- Person → `"person"`  
- Other objects detected instantly  

---

### 🔹 Option 2: IP Webcam (Mobile Camera)

#### 📡 Requirements:
- Same WiFi network  

#### 📲 Steps:
1. Open IP Webcam app  
2. Start server  
3. Copy IP address  
4. Enter in terminal  

#### ✅ Behavior:
- Live mobile feed on laptop  
- Move phone → video changes  
- Detection updates instantly  

---

## 🖥️ **System Workflow**

```bash
[ Camera (Laptop / Phone) ]
        ↓
[ Video Stream Capture ]
        ↓
[ MEC Edge Node (Laptop) ]
        ↓
[ YOLOv8 Processing ]
        ↓
[ Real-Time Detection Output ]
```

## Code Flow Logic
```python
1. Start program
2. Ask user → choose webcam or IP cam
3. Capture video stream
4. Load YOLO model

5. Loop:
    - Read frame
    - Run YOLO detection
    - Draw bounding boxes
    - Display output

6. Exit on key press
```
---

## 📊 **Performance & Advantages**

### ⚡ Key Benefits of MEC in This Project

- **Low Latency** → Processing happens locally, so no delay  
- **Real-Time Detection** → Instant object recognition  
- **No Cloud Dependency** → Works offline (except IP cam connection)  
- **Efficient Processing** → Lightweight YOLOv8 model ensures speed  
- **Privacy Preserving** → Data is not sent to external servers  

---

## 🧪 **Example Test Scenarios**

### **Test 1: Laptop Webcam**
- Start project → Choose `1`  
- Show different objects  

#### ✅ Expected Output:
- Detects:
  - Person  
  - Mobile phone  
  - Laptop  
  - Bottle  

---

### **Test 2: IP Webcam**
- Start project → Choose `2`  
- Enter IP address  

#### ✅ Expected Output:
- Live mobile camera feed  
- Move phone → video updates in real-time  
- Object detection updates instantly  

---

## 🛠️ **Code-Level Explanation**

### 🔹 Load YOLO Model
```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
```

### 🔹 Capture Video

#### Laptop Webcam:
```python
import cv2
cap = cv2.VideoCapture(0)
```
## IP Webcam:
```python
ip_url = "http://192.168.x.x:8080/video"
cap = cv2.VideoCapture(ip_url)
```
---
### 🤝 Contributing

Contributions are welcome! You can:

Report issues 🐛

Suggest new analysis features 💡

Submit pull requests 📬

---

### 📜 License

This project is licensed under the MIT License. See LICENSE for details.

Made with 💻 by Gamana
Explore more at https://github.com/gamana29


--- 
