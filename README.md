# 🚗 Accident Detection and Alert System using ESP32, GPS & GSM

An intelligent real-time vehicle accident detection and emergency alert system developed using **ESP32**, **MPU6050 Accelerometer & Gyroscope**, **NEO-6M GPS Module**, and **SIM7670 GSM Module**. The system continuously monitors vehicle motion and detects sudden impacts or rollovers. Upon detecting an accident, it automatically retrieves the current GPS location and sends an emergency SMS with a Google Maps link to predefined emergency contacts, enabling faster emergency response.

---

## 📌 Project Overview

Road accidents often lead to delayed emergency assistance due to the inability of victims to communicate their location. This project addresses that issue by providing an automated accident detection and alert mechanism.

The ESP32 continuously reads acceleration and orientation data from the MPU6050 sensor. If the measured values exceed predefined thresholds, the system identifies it as an accident. It then obtains the live GPS coordinates from the NEO-6M GPS module and transmits an emergency SMS through the SIM7670 GSM module. The SMS contains the exact location along with a clickable Google Maps link.

---

## ✨ Features

- Real-time accident detection
- Sudden impact detection using MPU6050
- Vehicle rollover detection
- Live GPS location tracking
- Automatic emergency SMS notification
- Google Maps location sharing
- Local buzzer alert
- Manual reset functionality
- Low-power embedded system
- Modular and expandable architecture

---

## 🛠 Hardware Components

| Component | Description |
|-----------|-------------|
| ESP32 Dev Board | Main microcontroller |
| MPU6050 | Accelerometer & Gyroscope |
| NEO-6M GPS Module | Live GPS location |
| SIM7670 GSM Module | SMS communication |
| Active Buzzer | Local accident alert |
| Push Button | Manual reset |
| Buck Converter | Stable power supply |
| Vehicle Battery / Adapter | System power source |

---

## 💻 Software & Libraries

### Software
- Arduino IDE

### Programming Language
- Embedded C++

### Libraries
- Wire.h
- TinyGPS++.h
- HardwareSerial.h
- MPU6050.h

---

## ⚙ Working Principle

1. ESP32 continuously reads acceleration and gyroscope values from the MPU6050.
2. Sensor data is analyzed in real time.
3. If acceleration or tilt exceeds the predefined threshold, an accident is detected.
4. ESP32 requests the current location from the NEO-6M GPS module.
5. Latitude and longitude are converted into a Google Maps URL.
6. SIM7670 GSM module sends an emergency SMS to predefined phone numbers.
7. The buzzer is activated to indicate that an emergency alert has been generated.
8. The system remains active until manually reset.

---

## 🔄 System Flow

```text
Power ON
     │
     ▼
Initialize ESP32
     │
     ▼
Read MPU6050 Sensor
     │
     ▼
Accident Detected?
     │
 ┌───┴────┐
 │        │
No       Yes
 │        │
 ▼        ▼
Continue Read GPS
          │
          ▼
Generate Google Maps Link
          │
          ▼
Send Emergency SMS
          │
          ▼
Activate Buzzer
          │
          ▼
Wait for Manual Reset
```

---

## 📲 SMS Format

```text
🚨 Accident Detected!

A vehicle accident has been detected.

Location:
Latitude : 25.5941
Longitude: 85.1376

Google Maps:
https://maps.google.com/?q=25.5941,85.1376

Please provide immediate assistance.
```

---

## 🔌 Circuit Connections

### MPU6050

| MPU6050 | ESP32 |
|---------|-------|
| VCC | 3.3V |
| GND | GND |
| SDA | GPIO21 |
| SCL | GPIO22 |

### GPS Module

| GPS | ESP32 |
|------|-------|
| TX | GPIO16 |
| RX | GPIO17 |
| VCC | 5V |
| GND | GND |

### GSM Module

| SIM7670 | ESP32 |
|---------|-------|
| TX | GPIO26 |
| RX | GPIO27 |
| VCC | 5V |
| GND | GND |

### Buzzer

| Buzzer | ESP32 |
|---------|-------|
| Positive | GPIO18 |
| Negative | GND |

---

## 📁 Project Structure

```text
Accident-Detection-and-Alert-System/

│── README.md
│── LICENSE
│── .gitignore
│
├── Source_Code/
│     └── accident_detection.ino
│
├── Circuit_Diagram/
│     └── circuit_diagram.png
│
├── Images/
│     ├── prototype.jpg
│     ├── hardware_setup.jpg
│     └── working_demo.jpg
│
├── Documentation/
│     └── Project_Report.pdf
│
└── Libraries/
```

---

## 🚀 Applications

- Smart Vehicle Safety Systems
- Emergency Response Systems
- Fleet Management
- Public Transportation
- School Buses
- Ambulances
- Personal Vehicles
- Commercial Transportation

---

## 📈 Future Enhancements

- Mobile Application Integration
- Firebase Cloud Database
- IoT Dashboard
- Real-Time Vehicle Tracking
- Automatic Emergency Calling
- AI-Based Accident Classification
- Camera Integration
- Cloud Event Logging
- Ambulance Notification System
- MQTT-Based Remote Monitoring

---

## 🧠 Skills Demonstrated

- Embedded Systems
- ESP32 Programming
- Embedded C++
- Sensor Interfacing
- GPS Integration
- GSM Communication
- UART Communication
- I2C Communication
- Real-Time Embedded Systems
- Hardware Debugging
- Circuit Design
- IoT System Development

---

## 📚 Repository Contents

- Source Code
- Circuit Diagram
- Hardware Images
- Project Documentation
- README
- License

---

## 👨‍💻 Author

**Mohit Kumar**

Electronics & Communication Engineering (ECE)

Interested in **Embedded Systems, IoT, VLSI, and Semiconductor Design.
---

⭐ If you found this project useful, consider giving this repository a **Star**.
