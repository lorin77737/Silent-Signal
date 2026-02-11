# 🔔 Silent Signal  
### IoT-Based Early Infrastructure Failure Detection System

## 📌 Project Overview

Silent Signal is an IoT-based preventive monitoring system that detects hidden infrastructure failures by identifying abnormal vibration and temperature patterns before visible damage occurs.

The system continuously monitors physical assets like pipes, electrical lines, and machines, learns their normal behavior, and alerts users when unusual changes are detected.

---

## 🚀 Problem Statement

Infrastructure failures such as pipe leaks, cable overheating, or machine damage often occur silently before visible breakdown.

Current systems:
- React after failure
- Use fixed threshold alarms
- Do not learn behavior patterns

Silent Signal provides a preventive, behavior-based detection system.

---

## 💡 Solution

Silent Signal:
- Collects vibration and temperature data
- Learns baseline (normal behavior)
- Detects anomalies using deviation logic
- Sends real-time alerts through a web dashboard

---

## 🛠 Tech Stack

### Hardware
- ESP32 / NodeMCU
- Vibration Sensor
- Temperature Sensor (DHT11 / LM35)
- Jumper wires
- Breadboard

### Software
- Arduino IDE
- HTML, CSS, JavaScript (Dashboard)
- WiFi-based data transmission
- Basic anomaly detection logic

---

## ⚙️ How It Works

### 1️⃣ Data Collection
Sensors continuously measure:
- Vibration
- Temperature

### 2️⃣ Baseline Learning
System collects normal readings for initial few minutes and calculates average values.

### 3️⃣ Anomaly Detection
Live sensor values are compared with baseline.
If deviation exceeds threshold → anomaly detected.

### 4️⃣ Alert System
- Dashboard changes color
- Warning message displayed
- Early alert generated

---

## 🖥 Features (MVP - 24 Hour Hackathon)

✔ Real-time sensor monitoring  
✔ Baseline learning mechanism  
✔ Anomaly detection logic  
✔ Web dashboard  
✔ Alert notification system  

---

## 🌍 Real-World Applications

- Smart Buildings
- Hostels & Apartments
- Industrial Machines
- Smart Cities Infrastructure
- Manufacturing Plants

---

## 🎯 Theme Mapping

**Primary Theme:**
Connected Devices & Automation (IoT & Embedded Systems)

**Secondary Themes:**
- Smart Infrastructure & Urban Development
- Intelligent Systems & Data Technologies

---

## 🧠 Why It Is Unique

| Traditional Systems | Silent Signal |
|---------------------|--------------|
| Detect failure | Predict failure |
| Fixed thresholds | Behavior-based detection |
| Reactive | Preventive |

---

## 📷 Demonstration

1. Show normal readings  
2. Simulate vibration/heat fault  
3. Dashboard displays alert  

---

## 👥 Team Members

- Your Name
- Team Member 2
- Team Member 3

---

## 📌 One-Line Pitch

“Silent Signal is an IoT-based early warning system that detects silent infrastructure anomalies before visible damage occurs.”

---

## 📜 License

This project was developed for a 24-hour Hackathon.
