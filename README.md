# Room Occupancy Detection System
ESP32-based intelligent occupancy detection using light sensor and machine learning

## Project Overview
Privacy-preserving room occupancy detection system using:
- ESP32 microcontroller
- Digital LDR light sensor
- Random Forest ML model (98.77% accuracy)
- ThingSpeak cloud integration

## Hardware Requirements
- ESP32 Development Board (ESP32-WROOM)
- Digital LDR Module (3-pin: VCC, GND, DO)
- Breadboard and jumper wires
- Micro-USB cable

## Wiring Connections
| LDR Module Pin | ESP32 Pin |
|----------------|-----------|
| VCC | 3.3V |
| GND | GND |
| DO | GPIO 34 |

## Software Setup

### Arduino IDE Configuration
1. Install Arduino IDE
2. Add ESP32 board support:
   - File → Preferences
   - Additional Board Manager URLs: 
```
     https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```
3. Tools → Board → Boards Manager → Search "ESP32" → Install

### WiFi and ThingSpeak Configuration
Update these lines in the code:
```cpp
const char* WIFI_SSID = "YOUR_WIFI_NAME";
const char* WIFI_PASSWORD = "YOUR_PASSWORD";
const char* THINGSPEAK_API_KEY = "YOUR_API_KEY";
```

### Upload to ESP32
1. Connect ESP32 via USB
2. Select: Tools → Board → ESP32 Dev Module
3. Select: Tools → Port → (your ESP32 port)
4. Click Upload
5. Open Serial Monitor (115200 baud)

## Features
- ✅ Real-time occupancy detection (98.77% accuracy)
- ✅ Edge ML inference (<100ms latency)
- ✅ Privacy-preserving (no cameras/biometrics)
- ✅ Cloud dashboard (ThingSpeak)
- ✅ Time-based threshold adaptation
- ✅ Low cost (£15 total hardware)

## ML Model
- **Algorithm:** Random Forest (50 trees, max_depth=5)
- **Training Dataset:** UCI Occupancy Detection (20,560 samples)
- **Features Used:** Light, Hour, Day_of_week, Is_weekend
- **Performance:** 98.77% accuracy, 0.9719 F1-score
- **Key Insight:** Light contributes 84.4% of predictions

## System Output Example
```
╔════════════════════════════════════╗
║      OCCUPANCY DETECTION           ║
╠════════════════════════════════════╣
║ 🕐 Time: 2026-01-14 14:30:45      ║
║ ⏰ Hour: 14h                       ║
║ 💡 Light: 85% (850 Lux)           ║
║ 🟢 ML PREDICTION: OCCUPIED        ║
║    Confidence: 92%                 ║
╚════════════════════════════════════╝
```

## Project Documentation
This project was developed as part of LD7182 - AI for IoT module at Northumbria University.

**Full Report:** Available in submission

**Author:** Basit Ogunlana (w24038619)

**Date:** January 2026

## License
MIT License - Free to use for educational purposes

## Acknowledgments
- UCI ML Repository for Occupancy Detection Dataset
- ThingSpeak platform for cloud integration
- Arduino and ESP32 communities
```

4. Scroll down and click **"Commit changes"**

---

### **STEP 5: Get Your Repository Link**

Your repository URL will be:
```
https://github.com/YOUR-USERNAME/room-occupancy-detection-esp32
```

**Copy this link!** You'll paste it in your report Appendix C.

---

## 📝 IN YOUR REPORT - APPENDIX C:

**Write:**

"## Appendix C: GitHub Repository

**Repository URL:** https://github.com/YOUR-USERNAME/room-occupancy-detection-esp32

The GitHub repository contains:
- Complete ESP32 firmware (.ino file) with inline documentation
- README.md with hardware setup and installation instructions
- Wiring diagram and pin connections
- Example Serial Monitor output
- System requirements and dependencies

**Repository Structure:**
```
room-occupancy-detection-esp32/
├── README.md                    (Setup instructions)
├── room_occupancy_esp32.ino     (Main firmware)
└── LICENSE                      (MIT License)
