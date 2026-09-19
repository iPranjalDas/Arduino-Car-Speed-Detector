# Arduino-Car-Speed-Detector

[![Arduino](https://img.shields.io/badge/Arduino-Prototyping-00979D?style=for-the-badge&logo=arduino)](https://www.arduino.cc/)
[![Category](https://img.shields.io/badge/Category-Timing_&_Sensor_Physics-00e5ff?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](#)
[![Author](https://img.shields.io/badge/Author-Pranjal_Das-orange?style=for-the-badge)](https://github.com/iPranjalDas)

⏱️ Optical speed-trap radar calculating vehicle velocity via calibrated dual-IR photogate beam breaks.

---

## 🖥️ System Architecture & Visual Wiring Layout

### 🔌 Graphical Schematic & Pinout Diagrams

![Car Speed Detector using Arduino and IR Sensor](Car%20Speed%20Detector%20using%20Arduino%20and%20IR%20Sensor.png)



```
┌── DUAL-IR SPEED TRAP CALCULATION ARCHITECTURE ──────────────────────────┐
│                                                                         │
│           [Car Travel Direction: ═════════════════════>]                │
│                                                                         │
│      [IR Sensor 1: Entry]                [IR Sensor 2: Exit]            │
│         Digital Pin 2                       Digital Pin 3               │
│               │                                   │                     │
│               │<────── Calibrated Distance ──────>│                     │
│               │              (e.g., 20 cm)        │                     │
│               ▼                                   ▼                     │
│      micros() Timestamp T1               micros() Timestamp T2          │
│                                                                         │
│      Velocity = Distance / (T2 - T1) * 3.6  [Kilometers per Hour]       │
│      Displayed in real-time on 16x2 LCD with overspeed buzzer alert     │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Hardware Requirements & Components

- **Microcontroller / Core:** Arduino Uno / ESP32 / NodeMCU (Refer to `.ino` sketch)
- **Power Supply:** 5V / 12V external regulated battery pack
- **Sensors & Actuators:** Detailed in circuit diagram and sketch pinout headers

---

## 🚀 Installation & Upload

1. Clone this repository:
   ```bash
   git clone https://github.com/iPranjalDas/Arduino-Car-Speed-Detector.git
   ```
2. Open the primary `.ino` sketch in the [Arduino IDE](https://www.arduino.cc/en/software).
3. Install required libraries via the Arduino Library Manager.
4. If this sketch uses Wi-Fi, update `YOUR_WIFI_SSID` and `YOUR_WIFI_PASSWORD` with your local network settings.
5. Select your target board and COM port, then click **Upload**.

---

## 🔒 Security & Privacy Notice
All source sketches have been thoroughly sanitized. Generic placeholder strings are used for network credentials and API tokens.

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.  
Copyright (c) 2026 Pranjal Das. All Rights Reserved.

---

## 👤 Author & Architecture
**Pranjal Das**  
- **GitHub:** [@iPranjalDas](https://github.com/iPranjalDas)
- **Projects:** [https://iPranjalDas.github.io/Projects/](https://iPranjalDas.github.io/Projects/)
