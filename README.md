# 🌱 HelioPlant: Intelligent Bio-Sync Tracker

An automated plant-care pedestal that optimizes sunlight exposure based on specific botanical needs. Using real-time UV and luminosity tracking, HelioPlant ensures your plants get exactly the light they need—no more, no less.

## 🚀 Project Overview
Different plants have different "Light Budgets." While a cactus might thrive in 12 hours of direct sun, a fern might suffer from leaf scorch. **HelioPlant** solves this by:
1. **Tracking:** Following the sun's trajectory using a dual-LDR array.
2. **Measuring:** Calculating cumulative UV exposure using a dedicated UV Index sensor.
3. **Regulating:** Automatically rotating the plant into the shade (or away from the window) once its specific daily light requirement has been met.
4. **Connecting:** Allowing users to select plant profiles via a companion mobile app.

---

## 🛠️ System Components

### Hardware
* **Microcontroller:** Arduino Uno or ESP32 (Recommended for App connectivity).
* **Sensors:** * 2x LDR Photosensitive Modules (Directional Tracking).
    * 1x GUVA-S12SD UV Index Sensor (Intensity & Safety Measurement).
* **Actuator:** 360° High-Torque Servo or Stepper Motor (Rotating Pedestal).
* **Display:** 16x2 I2C LCD (To show current UV index and "Light %" filled).

### Software & App
* **Embedded Logic:** C++ (Arduino/PlatformIO).
* **Communication:** BLE (Bluetooth Low Energy) or Wi-Fi (via ESP32).
* **Companion App:** Developed in [MIT App Inventor / Flutter / React Native] to send plant profiles (e.g., "Succulent" vs "Fern") to the device.

---

## 📂 Project Structure
```text
├── firmware/
│   ├── HelioPlant.ino     # Main logic and BLE handler
│   ├── LightLogic.cpp      # UV integration and LDR differential math
│   └── MotorControl.cpp    # Pedestal rotation functions
├── mobile_app/             # App source code and UI assets
├── 3D_Models/              # STL files for the rotating base
└── README.md
