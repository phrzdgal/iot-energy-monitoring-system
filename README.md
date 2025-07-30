# IoT Energy Monitoring System

## Project Overview
The **IoT Energy Monitoring System** is a full-stack project designed to measure, transmit, and visualize household or small-scale energy usage in real time.  

Using an **ESP32 microcontroller** and a **non-invasive current sensor (SCT-013)**, the system captures electricity consumption data, sends it wirelessly to a backend server, stores it in a database, and visualizes it through a web dashboard.  

This project demonstrates skills in **embedded C++**, **IoT protocols**, **backend APIs**, **databases**, and **frontend dashboards** — bridging software and hardware for energy technology applications.  

---

## System Architecture
```plaintext
[SCT-013 Current Sensor]
           │
           ▼
       [ESP32 MCU] ---- WiFi (MQTT/HTTP) ----> [FastAPI Backend + PostgreSQL]
                                                   │
                                                   ▼
                                          [React Dashboard]
```

### System Architecure Version II -- Utilizing Raspberry Pi
```plaintext
[SCT-013 Current Sensor] 
          │
          ▼
       [ESP32 MCU] ----WiFi/MQTT----> [Raspberry Pi Hub]
                                            │
                        ┌───────────────────┴────────────────────┐
                        │                                        │
                [FastAPI Backend + PostgreSQL]          [React Dashboard Server]
```

---

## Specifications & Features
The system is meant to measure real-time AC current using an SCT-013 current sensor with ESP32. It calculates power (Watts) and energy consumption (kWh), tasmits readings from ESP32 to a backend server via MQTT/HTTp, stores sensor data in PostgreSQL with timestamps, and provides visualizations to live and historical energy usage on a React dashboard. In the near future, the system should have the added capability of sending alerts when power usage exceeds a designated threshold. 

### Core Delivarables: 
1. ESP32 Firmware
   - Reads current using a SCT-013 sensor.
   - Calculates power usage in real-time.
   - Sends readings to backend in JSON format.
2. FastAPI Backend
   - Endpoint /api/data receives ESP32 readings.
   - Stores readings in PostgreSQL with timestamps.
   - Endpoint /api/usage povides usage history. 
3. PostgreSQL Database
   - Stores time-series data: timestamp, current, power, kWh.
4. React Dashboard
   - Displays real-time power usage.
   - Provides daily/weekly/monthly summaries.
   - Interactive charts using Recharts or Chart.js
5. (Future) Raspberry Pi
   - Linux System Administration
   - Local Server Hosting
   - MQTT Broker & Edge IoT Networking
   - Edge Computing Concepts
   - Ful-Stack Deployment Skills
   - Hardware Interfacing Beyond ESP32

--- 

## Project Structure
iot-energy-monitoring-system/
│
├── esp32_firmware/        # Arduino C++ code for ESP32
├── backend/               # FastAPI backend
│   ├── models/            # Database models
│   └── routes/            # API endpoints
├── dashboard/             # React frontend
└── docs/                  # Diagrams, notes, and setup guides

--- 

## Skills
- Embedded Systems: Writing firmware in C++ for ESP32, using ADC.
- IoT Communication: Implementing MQTT/HTTP for device-to-server data transfer.
- Backend Development: Designing FastAPI endpoints, handling JSON, SQLAlchemy integration.
- Databases: Managing time-series energy data in PostgreSQL.
- Frontend Development: React dashboard with real-time charts.
- Systems Integration: Debugging across hardware, networking, and software layers.
- Energy Domain Knowledge: Basics of current measurement, power calculation, and energy analytics.
- (Future) Raspberry Pi Setup: Linux system administration; Local FastAPI server; MQTT broker coordinating many ESP32 nodes; Offline-capable dashboard; Deployable product for field/humanitarian use 


