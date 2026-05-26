<p align="center">
  <img src="https://capsule-render.vercel.app/render?type=waving&color=auto&height=220&section=header&text=Smart%20Ambulance%20System&fontSize=50&animation=fadeIn&fontAlignY=38" />
</p>

# 🚑 Integrated Emergency Response System (IERS)
### **Official Patent Portfolio | Innovation #01**

<p align="left">
  <img src="https://img.shields.io/badge/Status-Patent--Pending-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Publication--No-IN202641011997_A1-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Field-Bio--Medical_Engineering-orange?style=for-the-badge" />
</p>

---

## 🌟 The Vision
[cite_start]The **IERS** project attacks the **"Golden Hour"** delay from two fronts: eliminating traffic gridlocks and removing information blackouts between the ambulance and the ER [cite: 31-33, 41].

## ⚡ Technical Core & Innovations

### 🩺 1. Real-Time Health Telemetry (HMM)
* [cite_start]**Digital Signal Processing:** Implements a **2nd order IIR bandpass filter** on-chip to strip 50Hz electrical hum from raw ECG signals [cite: 71, 148-150].
* [cite_start]**Multi-Sensor Array:** Synchronous monitoring of ECG (AD8232), SpO2 (MAX30100), Blood Pressure, and GSR [cite: 70, 116, 126-128].
* [cite_start]**Cloud Sync:** Formats data into **JSON packets** for live hospital-side visualization via ESP8266 [cite: 79-81, 137-138, 167-168].

### 🚦 2. Intelligent Traffic Override (TCM)
* [cite_start]**GPS-Based Geofencing:** Uses the **Haversine Formula** to calculate the precise great-circle distance to upcoming junctions [cite: 146-147].
* [cite_start]**Independent RF Link:** Uses a dedicated **nRF24L01+ transceiver** (2.4 GHz) to trigger a "Green Corridor" when within 800m [cite: 104-106].
* [cite_start]**Concurrent Operation:** Health and Traffic modules work in parallel, powered by the vehicle's 12V battery [cite: 68-70, 119-121].

---

## 🛠️ Hardware Stack
| Component | Specifications | Role |
| :--- | :--- | :--- |
| **Main MCU** | Arduino Mega 2560 | [cite_start]Health Processing & Cloud Link [cite: 122-124] |
| **Sub MCU** | Arduino Nano | Navigation & Radio Broadcast |
| **Comms** | nRF24L01+ | 2.4GHz ISM Band Priority Link |
| **Sensors** | MAX30100, AD8232, NEO-6M | [cite_start]Vitals & Positioning [cite: 126-129] |

---

## 📸 Engineering Proof (Prototype)
[cite_start]The invention is backed by a fully functional physical prototype [cite: 158-164].
* **Vehicle Unit:** Compact design with OLED local display and external radio antenna.
* **Junction Unit:** Relay-controlled traffic light override system with authentication logic.

---

## 📁 Repository Contents
* [cite_start]**[📄 View Official Patent Publication](./01-PUBLICATION.pdf)** [cite: 7-8, 196]
* [cite_start]**[🖼️ View Technical Drawings & Circuitry](./01-DRAWINGS.pdf)** [cite: 86-95]

<p align="center">
  <img src="https://capsule-render.vercel.app/render?type=waving&color=auto&height=100&section=footer" />
</p>

<p align="center"> 
  ⭐ <b>Star this repo if you find it useful!</b> ⭐
</p>
