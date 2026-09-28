# Obstacle Detection for Visually Impaired

An Arduino-based obstacle detection system designed to assist visually impaired users by detecting nearby obstacles using multiple ultrasonic sensors and providing an audio alert through a buzzer.

## 📌 Project Overview

This project uses an Arduino UNO and three HC-SR04 ultrasonic sensors to detect obstacles in different directions.

The ultrasonic sensors continuously measure the distance to nearby objects. The Arduino identifies the minimum detected distance and changes the buzzer's alert pattern according to the distance of the nearest obstacle.

This provides an intuitive audio-based indication of how close an obstacle is.

## 🎯 Objectives

- Detect obstacles using ultrasonic sensing.
- Monitor obstacles from multiple directions.
- Determine the nearest detected obstacle.
- Provide an audio warning through a buzzer.
- Develop a low-cost embedded system for assistive applications.

## 🛠️ Hardware

- Arduino UNO
- 3 × HC-SR04 Ultrasonic Sensors
- Buzzer
- Connecting wires
- Breadboard
- Power supply / USB connection

## 💻 Software

- Arduino IDE
- Embedded C / Arduino C++

## ⚙️ Pin Configuration

| Component | Arduino Pin |
|---|---|
| Ultrasonic Sensor 1 – TRIG | D4 |
| Ultrasonic Sensor 1 – ECHO | D5 |
| Ultrasonic Sensor 2 – TRIG | D2 |
| Ultrasonic Sensor 2 – ECHO | D3 |
| Ultrasonic Sensor 3 – TRIG | D6 |
| Ultrasonic Sensor 3 – ECHO | D7 |
| Buzzer | D9 |

## 🔄 System Workflow

1. The three HC-SR04 sensors transmit ultrasonic pulses.
2. Each sensor measures the distance to a nearby obstacle.
3. The Arduino calculates the distance from the echo time.
4. The three distance measurements are compared.
5. The minimum valid distance is selected.
6. The buzzer generates an alert according to the detected distance.
7. The closer the obstacle, the faster the alert pattern becomes.

## 🔔 Alert Logic

| Nearest Obstacle Distance | Buzzer Pattern |
|---|---|
| 0–5 cm | 600 Hz, 100 ms |
| >5–10 cm | 500 Hz, 300 ms |
| >10–15 cm | 400 Hz, 400 ms |
| >15–20 cm | 300 Hz, 500 ms |
| >20–25 cm | 250 Hz, 600 ms |
| >25–30 cm | 200 Hz, 700 ms |

No buzzer alert is generated when no valid obstacle is detected within the monitored range.

## 📂 Repository Structure

```text
Obstacle-Detection-Visually-Impaired/
│
├── README.md
│
├── Arduino_Code/
│   └── obstacle_detection.ino
│
└── Images/
    └── obstacle_detection_circuit.png
