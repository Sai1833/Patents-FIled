# 🔥 Autonomous Wireless Mesh Network
### **Wildfire Detection & Early Warning System**
**Official Patent Portfolio | Innovation #02**

[![Patent-Pending](https://img.shields.io/badge/Status-Patent--Pending-blue?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Publication-No](https://img.shields.io/badge/Publication--No-IN202641057752_A1-success?style=for-the-badge)](https://iprsearch.ipindia.gov.in)
[![Connectivity](https://img.shields.io/badge/Tech-LoRa_|_Mesh_|_P2P-green?style=for-the-badge)]()

---

## 🌲 The Challenge
Remote forests lack cellular coverage (No 4G/5G) and power grids. Traditional monitoring fails in deep woods due to signal attenuation and line-of-sight issues.

## ⚡ The Solution: Self-Healing LoRa Mesh
This system uses solar-powered autonomous nodes that form a **Peer-to-Peer (P2P) Relay Chain**. Alerts "hop" from node to node until they reach the forest edge gateway.

### 🛰️ Core Technical Innovations
* **Multi-Sensor Validation:** Prevents false alarms by requiring a positive Flame signal **AND** an elevated Smoke or Heat reading (Threshold: >45°C or >1200 ADC smoke units) [cite: 2617, 2753-2755].
* [cite_start]**Energy Autonomy:** Each node is powered by a **6V 10W Solar Panel** and an MPPT charge controller, managing a 18650 Li-ion cell for 24/7 operation [cite: 2615, 2724-2726].
* [cite_start]**Mesh Relay Protocol:** Implements a "Hear-Check-Forward" rule—nodes listen for neighbor packets and automatically retransmit new alerts to extend range indefinitely.

---

## 📁 Repository Contents
* [📄 View Official Publication](./fire_w2.pdf)
* [🖼️ Technical Schematics](./fire_D.pdf)

---
## 🏗️ System Architecture

### **1. Sensor Node (The Watchman)**
* **Brain:** Arduino Nano.
* **Sensors:** IR Flame Detector, MQ-2 Smoke/Gas, and DHT22 [cite: 2616, 2731-2733].
* [cite_start]**Radio:** **SX1262 LoRa module** optimized for tree penetration (866 MHz, SF10) [cite: 2738-2739].

### **2. Receiver Station (The Gateway)**
* [cite_start]**MCU:** ESP32 with built-in Wi-Fi.
* **Function:** Collects LoRa packets, formats them into **JSON**, and POSTs to a cloud dashboard.

---

## 📐 Operational Logic
```mermaid
graph TD
    A[Sleep Mode: Low Power] -->|Timer Wake| B[Acquire Sensor Data]
    B --> C{Fire Condition?}
    C -->|Flame + Smoke/Heat| D[Broadcast FIRE ALERT]
    C -->|Normal| E[Send Status Update]
    D --> F[Neighbor Node Relays]
    F --> G[Gateway Reaches Cloud]
    G --> Alert[Authorities Notified < 30s]
