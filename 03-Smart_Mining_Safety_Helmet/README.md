# ⛑️ Smart Safety Helmet for Underground Mining
### **IoT-Based Live Tracking & Multi-Sensor Hazard Detection**
**Official Patent Portfolio | Innovation #03**

[![Patent-Pending](https://img.shields.io/badge/Status-Patent--Pending-blue?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Publication-No](https://img.shields.io/badge/Publication--No-IN202641060636_A1-success?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Localization](https://img.shields.io/badge/Tech-UWB_|_LoRa_|_STM32-red?style=for-the-badge)]()

---

## ⛏️ The Underground Challenge
Underground coal mines are high-risk environments with zero GPS visibility, toxic gas leakages (Methane, CO), and extreme temperatures. Traditional communication often fails through thick rock layers.

## ⚡ The Solution: UWB + LoRa Hybrid Safety System
This smart helmet provides an integrated safety backbone, ensuring every miner is tracked with precision and protected from environmental hazards.

### 🛰️ Core Technical Innovations
* **UWB Precision Tracking:** Uses **Ultra-Wideband (UWB)** tags to enable centimeter-level indoor localization inside tunnels, bypassing the need for GPS.
* **Long-Range Data Relay:** Employs a **LoRa Wireless Mesh** to transmit sensor data from deep tunnels to the surface control room via relay nodes.
* **Intelligent Hazard Detection:** Continuous monitoring for Methane (CH4), Carbon Monoxide (CO), and abnormal temperature spikes with instant local and remote alerts.
* **Emergency Panic Trigger:** A dedicated SOS push button that immediately broadcasts a high-priority distress signal to the dashboard.

---

## 📁 Repository Contents
* [📄 View Official Publication](./03-PUBLICATION.pdf)
* [🖼️ Technical Block Diagrams](./03-DRAWINGS.pdf)

---

## 🏗️ System Architecture


### **1. The Smart Helmet (The Unit)**
* **Brain:** STM32 or ESP32 Microcontroller.
* **Sensors:** Gas Sensor (MQ-4), Temperature sensor, and Flame sensor.
* **Alerts:** Local buzzer and LED indicators for immediate worker feedback.

### **2. Surface Monitoring (The Control Room)**
* **Dashboard:** A live map interface showing miner positions and real-time environmental status.
* **Alert API:** Automated triggers for Alarms, SMS, and Voice Calls during critical incidents.

---

## 📐 Operation & Communication Flow


```mermaid
graph TD
    A[Miner in Tunnel] --> B[UWB Anchor Positioning]
    B --> C[Sensor Data Acquisition]
    C --> D{Emergency?}
    D -->|Yes| E[High-Priority SOS Alert]
    D -->|No| F[Periodic Status Update]
    E & F --> G[LoRa Relay Nodes]
    G --> H[Surface LoRa Gateway]
    H --> I[Cloud / Control Dashboard]
    I -->|Action| J((Rescue / Safety Protocol))
