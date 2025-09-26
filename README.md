# **_CropCare - Intelligent Pesticide Sprinkling System_**
**_Team:_ Spartan_**

**_Project for:_ Smart India Hackathon 2025_

CropCare is an Unmanned Guided Vehicle (UGV) designed for modern precision agriculture. It autonomously navigates farm terrains to detect crop diseases using a machine learning model and applies pesticides precisely to infected plants with a robotic arm. This targeted approach significantly reduces chemical usage, minimizes environmental impact, and improves crop yield.

**_Live Project Website:_** [https://sparton-sih-2025-9jpr.vercel.app/](https://sparton-sih-2025-9jpr.vercel.app/)

---

## **🎯 Key Features**

- **_Autonomous Navigation:_** UGV travels through rough farm terrains.
- **_AI-Powered Disease Detection:_** Uses TensorFlow and YOLO to identify infected plants from camera footage in real-time.
- **_Precision Spraying:_** Robotic arm sprays pesticide only on targeted infected areas, reducing waste and environmental harm.
- **_Web-Based Control:_** User-friendly web interface for remote monitoring and control.
- **_Real-Time Communication:_** WebSockets and MQTT enable seamless communication between UGV and server.
- **_Data Management:_** Operations data stored and managed with MongoDB and PostgreSQL.

---

## **⚙️ System Architecture**

The system operates through a coordinated flow of information between the web client, the server, and the UGV's hardware components.

1. **_Initiation:_** "Start" signal sent from web interface.
2. **_Movement:_** ESP32 controls Rover movement.
3. **_Image Capture:_** Robotic arm (Raspberry Pi Camera) captures plant images.
4. **_Analysis:_** Raspberry Pi runs disease detection model.
5. **_Action:_**
   - *No infection*: Rover moves forward.
   - *Infection detected*: Raspberry Pi signals ESP32 to activate arm and spray pesticide.
6. **_Data Sync:_** Images and actions sent to central server and stored for logging and analysis.

---

## **🛠️ Technology Stack**

### **_Hardware_**
- **Raspberry Pi & ESP32**
- **High-Resolution Camera Module**
- **DC Motors & Motor Drivers**
- **Ultrasonic Sensors**
- **Robotic Arm (Servo Motors)**
- **24V, 22,000 mAh Battery**

### **_Software & Frameworks_**
- **Frontend:** ReactJS
- **Backend:** FastAPI, ExpressJS
- **AI/ML:** TensorFlow, YOLO
- **Communication:** WebSockets, MQTT
- **Database:** MongoDB, PostgreSQL
- **Robotics:** ROS2
- **Platforms:** VS Code, Docker, GitHub
