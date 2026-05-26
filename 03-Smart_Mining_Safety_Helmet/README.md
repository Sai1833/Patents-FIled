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
* **[span_2](start_span)[span_3](start_span)UWB Precision Tracking:** Uses **Ultra-Wideband (UWB)** tags to enable centimeter-level indoor localization inside tunnels, bypassing the need for GPS[span_2](end_span)[span_3](end_span).
* **[span_4](start_span)[span_5](start_span)Long-Range Data Relay:** Employs a **LoRa Wireless Mesh** to transmit sensor data from deep tunnels to the surface control room via relay nodes[span_4](end_span)[span_5](end_span).
* **[span_6](start_span)[span_7](start_span)Intelligent Hazard Detection:** Continuous monitoring for Methane (CH4), Carbon Monoxide (CO), and abnormal temperature spikes with instant local and remote alerts[span_6](end_span)[span_7](end_span).
* **[span_8](start_span)[span_9](start_span)Emergency Panic Trigger:** A dedicated SOS push button that immediately broadcasts a high-priority distress signal to the dashboard[span_8](end_span)[span_9](end_span).

---

## 🏗️ System Architecture


### **1. The Smart Helmet (The Unit)**
* **[span_10](start_span)[span_11](start_span)Brain:** STM32 or ESP32 Microcontroller[span_10](end_span)[span_11](end_span).
* **[span_12](start_span)[span_13](start_span)Sensors:** Gas Sensor (MQ-4), Temperature sensor, and Flame sensor[span_12](end_span)[span_13](end_span).
* **[span_14](start_span)[span_15](start_span)Alerts:** Local buzzer and LED indicators for immediate worker feedback[span_14](end_span)[span_15](end_span).

### **2. Surface Monitoring (The Control Room)**
* **[span_16](start_span)[span_17](start_span)Dashboard:** A live map interface showing miner positions and real-time environmental status[span_16](end_span)[span_17](end_span).
* **[span_18](start_span)[span_19](start_span)Alert API:** Automated triggers for Alarms, SMS, and Voice Calls during critical incidents[span_18](end_span)[span_19](end_span).

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
