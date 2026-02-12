Here is a professional **README.md** file tailored exactly to your ESP32 “Silent Signal” project code.

You can copy this into a `README.md` file in your GitHub repository.

---

# 🚨 Silent Signal

### Industrial Infrastructure Monitoring System (ESP32 + Web Dashboard)

Silent Signal is a real-time industrial monitoring system built using **ESP32**, designed to monitor:

* 🌡 Temperature (DHT11)
* 💧 Humidity (DHT11)
* ⚙️ Vibration Detection
* 🚨 Critical Alerts with Buzzer & LEDs
* 📊 Live Web Dashboard with Graphs

The system creates its own **WiFi Access Point** and hosts a futuristic monitoring dashboard accessible from any device.

---

## 📌 Features

✅ Real-time temperature monitoring
✅ Real-time humidity monitoring
✅ Vibration event detection
✅ Automatic critical alert system
✅ Manual siren test from dashboard
✅ Live updating nano-graphs
✅ Event logging terminal
✅ LED status indicators
✅ Buzzer alert system
✅ Captive portal (auto redirect using DNS server)

---

## 🛠 Hardware Requirements

| Component                          | Quantity    |
| ---------------------------------- | ----------- |
| ESP32                              | 1           |
| DHT11 Sensor                       | 1           |
| Vibration Sensor Module            | 1           |
| Buzzer                             | 1           |
| LEDs (Green, Blue, Yellow, Orange) | 4           |
| Resistors (220Ω recommended)       | 4           |
| Breadboard & Jumper Wires          | As required |

---

## 🔌 Pin Configuration

| Component        | ESP32 Pin |
| ---------------- | --------- |
| Vibration Sensor | GPIO 13   |
| DHT11 Data       | GPIO 14   |
| Buzzer           | GPIO 2    |
| Green LED        | GPIO 18   |
| Blue LED         | GPIO 19   |
| Yellow LED       | GPIO 21   |
| Orange LED       | GPIO 22   |

---

## 📡 WiFi Access Point

The ESP32 creates a WiFi network:

```
SSID: Sensor Syndicate
Password: Bjls@1234
```

### How to Connect:

1. Power the ESP32.
2. Connect to WiFi: **Sensor Syndicate**
3. Open browser.
4. Visit: `192.168.4.1`
5. Dashboard loads automatically (captive portal enabled).

---

## 📊 Dashboard Overview

The dashboard includes:

### 🔥 Power Core (Temperature)

* Live temperature value
* Status indicator:

  * NOMINAL (< 30°C)
  * WARNING (> 30°C)
  * CRITICAL (> 45°C)
* Live graph

### ⚙️ Turbine A1 (Vibration)

* Displays vibration state (0 or 1)
* Logs vibration spike events
* Turns red during failure
* Live graph

### 💧 Cooling System (Humidity)

* Live humidity %
* Status: Optimal / High
* Live graph

### 🚨 System Status

* Operational
* Critical Alert
* Manual siren test button

### 📢 Live Event Terminal

Logs:

* System initialization
* Manual siren events
* Vibration spike alerts

---

## 🚦 LED Behavior Logic

| Condition                                         | LED Behavior          |
| ------------------------------------------------- | --------------------- |
| Normal                                            | Green ON              |
| Temp > 30°C                                       | Green Blinking        |
| Humidity > 80%                                    | Blue Blinking         |
| Vibration Detected                                | Yellow Blinking       |
| Critical (Temp > 45°C / Vibration / Manual Alarm) | Orange ON + Buzzer ON |

---

## 🔊 Alert Logic

Critical Alert triggers when:

* Temperature > 45°C
* Vibration detected
* Manual siren test activated

Actions:

* Orange LED ON
* Buzzer ON
* Dashboard shows CRITICAL ALERT

---

## 🧠 Software Architecture

### Backend (ESP32)

* `WiFi.softAP()` → Creates WiFi network
* `WebServer` → Hosts dashboard
* `DNSServer` → Captive portal redirection
* `/data` → Sends JSON sensor data
* `/cmd` → Handles siren commands

### Frontend (Embedded HTML)

* Custom CSS futuristic UI
* NanoChart JavaScript graph engine
* Fetch API polling every 500ms
* Real-time status logic

---

## 📁 API Endpoints

### `GET /`

Returns dashboard HTML page.

### `GET /data`

Returns JSON:

```json
{
  "t": 32.5,
  "h": 68,
  "v": 0,
  "v_ev": false,
  "up": "00:05:23"
}
```

### `GET /cmd?s=1`

Activate manual siren.

### `GET /cmd?s=0`

Deactivate manual siren.

---

## ⚙️ Installation & Setup

1. Install Arduino IDE.
2. Install ESP32 board package.
3. Install required libraries:

   * WiFi
   * WebServer
   * DHT sensor library
   * DNSServer
4. Upload code to ESP32.
5. Power the device.

---

## 📈 System Workflow

1. ESP32 boots.
2. LEDs + buzzer startup sequence.
3. Creates WiFi Access Point.
4. Starts web server.
5. Continuously:

   * Reads DHT11
   * Reads vibration sensor
   * Updates LED states
   * Sends JSON data
   * Handles dashboard commands

---

## 🎯 Project Category

✔ Embedded Systems
✔ IoT
✔ Industrial Safety
✔ Smart Monitoring
✔ Hardware + Software Integrated System

---

## 🚀 Future Improvements

* MQTT cloud integration
* SMS alert system
* Mobile app version
* SD card logging
* Multiple sensor expansion
* AI-based anomaly detection

---

## 👨‍💻 Developed For

Hackathons, industrial monitoring demos, IoT prototypes, and safety system simulations.

---
