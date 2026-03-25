# 🌾 Smart Agriculture Monitoring System (IoT)

![Banner](images/banner.png)

## 📌 Overview
The Smart Agriculture Monitoring System is an end-to-end Industrial IoT (IIoT) solution designed for precision farming. It collects real-time environmental data and enables remote monitoring, automation, and cloud-based analytics.

The system uses an ESP32 microcontroller to gather sensor data, transmit it via MQTT, and integrate with Node-RED, InfluxDB, and Grafana.

---

## 🎯 Key Features
- Real-time monitoring (Temperature, Humidity, Soil Moisture, Light)
- Remote pump control (ON/OFF)
- Cloud storage (InfluxDB)
- Visualization dashboards (Grafana)
- JSON-based scalable system

---

## 🧠 System Architecture
Sensors → ESP32 → MQTT → Node-RED → InfluxDB → Grafana  
                          ↓  
                     Pump Control  

---

## 🛠️ Hardware Components

| Component | Function | Interface |
|----------|--------|----------|
| ESP32 DevKit V1 | Controller | MCU |
| DHT11 | Temp & Humidity | GPIO 23 |
| LDR | Light | GPIO 35 |
| Soil Sensor | Moisture | GPIO 34 |
| Relay | Pump Control | GPIO 18 |
| Water Pump | Irrigation | External |

---

## ⚠️ Notes
- Use 10kΩ resistor with LDR
- Use external power for pump

---

## 💻 Software Stack
- Arduino (C++)
- MQTT (Mosquitto)
- Node-RED
- InfluxDB
- Grafana

---

## 🚀 Setup

### 1. Mosquitto
```
listener 1883
allow_anonymous true
```

### 2. ESP32
- Open firmware file
- Add WiFi + MQTT credentials
- Upload

### 3. Node-RED
```
npm install -g node-red
node-red
```

### 4. Cloud
- Setup InfluxDB
- Connect Grafana

---

## 📂 Structure
```
Smart-Agriculture-IoT/
├── README.md
├── firmware/
├── node-red/
├── images/
├── docs/
```

---

## 📜 License
MIT License
