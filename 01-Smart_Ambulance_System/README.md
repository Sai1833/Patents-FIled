# 🚑 Smart Ambulance System
### **Integrated Emergency Response System (IERS)**
**Official Patent Portfolio | Innovation #01**

[![Patent-Pending](https://img.shields.io/badge/Status-Patent--Pending-blue?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Publication-No](https://img.shields.io/badge/Publication--No-IN202641011997_A1-success?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Tech-Stack](https://img.shields.io/badge/Tech-Embedded_C_|_IoT_|_DSP-orange?style=for-the-badge)]()

---

## 🌟 The Vision
Traditional emergency transit suffers from a **"Double Delay"**: physical traffic gridlock and a medical information blackout. [span_2](start_span)The **IERS** attacks both by integrating live health telemetry with automated traffic pre-emption[span_2](end_span).

## ⚡ Technical Core & Innovations

### 🩺 1. Real-Time Health Telemetry (HMM)
* **[span_3](start_span)[span_4](start_span)Digital Signal Processing:** Implements a **2nd order IIR bandpass filter** on-chip to strip 50Hz electrical hum and baseline drift from raw ECG signals[span_3](end_span)[span_4](end_span).
* **[span_5](start_span)[span_6](start_span)Multi-Sensor Array:** Synchronous monitoring of ECG (AD8232), SpO2 (MAX30100), Blood Pressure, and GSR (Stress Sensing)[span_5](end_span)[span_6](end_span).
* **[span_7](start_span)[span_8](start_span)Cloud Sync:** Formats data into **JSON packets** for live hospital-side visualization via Blynk/Cloud dashboards[span_7](end_span)[span_8](end_span).

### 🚦 2. Intelligent Traffic Override (TCM)
* **[span_9](start_span)[span_10](start_span)GPS-Based Geofencing:** Uses the **Haversine Formula** to calculate the precise great-circle distance between the ambulance and upcoming junctions[span_9](end_span)[span_10](end_span).
* **[span_11](start_span)[span_12](start_span)Independent RF Link:** Uses a dedicated **nRF24L01+ transceiver** (2.4 GHz) to trigger a "Green Corridor," bypassing unreliable cellular networks[span_11](end_span)[span_12](end_span).
* **[span_13](start_span)[span_14](start_span)Concurrent Operation:** The Health and Traffic modules work in parallel, powered by the vehicle's 12V battery through an LM2596 conditioning stage[span_13](end_span)[span_14](end_span).

---

## 🏗️ System Architecture & Logic Flow


```mermaid
graph TD
    A[Start: Emergency Run] --> B{Parallel Process}
    B --> H[Health Monitoring]
    B --> T[Traffic Pre-emption]
    H -->|JSON via WiFi| Cloud[Hospital ER Dashboard]
    T -->|Within 800m| Radio[nRF24L01 Priority Signal]
    Radio --> JCU[Junction Control Unit]
    JCU -->|Override| Light[Traffic Signal: GREEN]
    Goal((Saved Lives))
    Cloud --> Goal
    Light --> Goal
