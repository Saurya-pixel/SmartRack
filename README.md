# ☀️ SmartSun Drying Rack

A high-school CS project: An intelligent, automated laundry drying system that tracks the sun for maximum efficiency and protects clothes from rain.

## 🚀 Project Overview
The **SmartSun Drying Rack** is an integrated hardware and software solution designed to reduce laundry drying time. Using a dual-axis light-sensing array, the rack rotates to follow the sun's position throughout the day. Additionally, the system features an automated "Rain Guard" that deploys a protective shed over the clothes when moisture is detected.

### Key Features
* **Active Sun Tracking:** Uses two LDRs (Light Dependent Resistors) and a PID-style logic loop to keep the rack angled toward the strongest light source.
* **Rain Protection:** Instant-response rain sensor triggers a motorized awning to cover the rack.
* **Safety Overrides:** Physical limit switches prevent motor over-rotation and cable tangling.
* **Automated Night Reset:** Logic to return the rack to the "East" position after sunset.

---

## 🛠️ System Components

### Hardware
* **Microcontroller:** Arduino Uno (The "Brain")
* **Primary Motor:** NEMA 17 Stepper Motor + A4988 Driver (Rack Rotation)
* **Secondary Motor:** SG90 Servo (Shed Deployment)
* **Sensors:** 2x Photoresistors (LDRs), 1x Raindrop Sensor Module
* **Safety:** 2x Mechanical Limit Switches
* **Power:** 12V 2A DC Power Supply (for motors) + USB 5V (for Arduino)

### Software
* **Language:** C++ / Arduino Wire
* **Environment:** Arduino IDE / VS Code with PlatformIO
* **Libraries:** `Stepper.h`, `Servo.h`

---

## 📂 Project Structure
```text
├── src/
│   ├── main.cpp          # Core logic loop and state machine
│   ├── sensors.cpp       # LDR and Rain sensor reading functions
│   └── movement.cpp      # Motor control and calibration functions
├── docs/
│   ├── wiring_diagram.png
│   └── flow_chart.png
├── README.md             # This file
└── LICENSE
