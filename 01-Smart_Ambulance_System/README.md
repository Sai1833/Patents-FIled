# 🚑 Smart Ambulance System
### **Patent-Filed | IoT & Bio-Medical Engineering**

[![Patent-Status](https://img.shields.io/badge/Status-Patent--Pending-blue?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Publication-No](https://img.shields.io/badge/Publication--No-IN202641011997_A1-success?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Tech-Stack](https://img.shields.io/badge/Stack-Embedded_C_|_IoT_|_JSON-orange?style=for-the-badge)]()

---

## 🌟 Vision
[span_2](start_span)The IERS project attacks the **"Golden Hour"** delay from two fronts: eliminating traffic gridlocks and removing information blackouts between the ambulance and the ER[span_2](end_span).

## ⚡ Key Technical Features
* **[span_3](start_span)Concurrent Operation:** The Health (HMM) and Traffic (TCM) modules run independently and simultaneously to maximize efficiency[span_3](end_span).
* **[span_4](start_span)[span_5](start_span)Intelligent Geofencing:** Uses the **Haversine Formula** to detect upcoming traffic junctions within 800m[span_4](end_span)[span_5](end_span).
* **[span_6](start_span)[span_7](start_span)Digital Signal Processing:** Real-time **2nd order IIR bandpass filters** clean raw ECG data from powerline noise[span_6](end_span)[span_7](end_span).
* **[span_8](start_span)[span_9](start_span)Reliable Data Link:** Independent **nRF24L01+ radio link** for traffic overrides, bypassing unreliable cellular networks[span_8](end_span)[span_9](end_span).

---

## 🛠️ System Architecture


### **1. Health Monitoring Module (HMM)**
* **[span_10](start_span)MCU:** Arduino Mega 2560[span_10](end_span).
* **[span_11](start_span)Sensors:** * ECG (AD8232)[span_11](end_span).
    * [span_12](start_span)Pulse Oximeter (MAX30100)[span_12](end_span).
    * [span_13](start_span)[span_14](start_span)Blood Pressure & GSR (Stress Sensing)[span_13](end_span)[span_14](end_span).
* **[span_15](start_span)Cloud:** Data formatted as **JSON** and pushed via ESP8266 to a live dashboard[span_15](end_span).

### **2. Traffic Clearance Module (TCM)**
* **[span_16](start_span)MCU:** Arduino Nano[span_16](end_span).
* **[span_17](start_span)[span_18](start_span)Hardware:** NEO-6M GPS & nRF24L01+ Transceiver[span_17](end_span)[span_18](end_span).
* **[span_19](start_span)[span_20](start_span)Logic:** Automatically triggers "Green Corridor" sequences at upcoming junctions based on approach direction[span_19](end_span)[span_20](end_span).

---

## 📐 Methodological Flow
```mermaid
graph TD
    Start[Ambulance Starts] --> H[Health Vitals Monitoring]
    Start --> T[GPS Geofencing Active]
    H -->|JSON Packets| Cloud[Live Hospital Dashboard]
    T -->|Within 800m| Radio[nRF24L01+ Priority Command]
    Radio --> JCU[Junction Control Unit]
    JCU -->|Override| Green[Signal Turned Green]
    Green --> Goal((Saved Lives))
    Cloud --> Goal
