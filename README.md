<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:ff6b6b,100:1e3a8a&height=220&section=header&text=4WD%20Arduino%20Robot%20Car&fontSize=64&fontAlign=50&fontAlignY=60&animation=fadeIn&fontColor=ffffff&desc=Bluetooth%20Controlled%20|%20Mobile%20Controlled&descAlign=50&descAlignY=88&descSize=26&descColor=f0f9ff&shadow=true" alt="Header" />
</div>

<h1 align="center">🚗 4WD Arduino Robot Car</h1>
<h3 align="center">Bluetooth Controlled Robotics Project</h3>

<div align="center">
  <img src="https://img.shields.io/badge/Platform-Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white" />
  <img src="https://img.shields.io/badge/Controller-Bluetooth-0082FC?style=for-the-badge&logo=bluetooth&logoColor=white" />
  <img src="https://img.shields.io/badge/Mobile-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Open--Source-Hardware-000000?style=for-the-badge&logo=open-source-initiative&logoColor=white" />
</div>




## Introduction:
Welcome to the **4WD Arduino Robot Car** project repository! This is a comprehensive, open-source robotics project that implements a fully functional 4-wheel drive robot car controlled wirelessly via Bluetooth from a mobile device. Designed for enthusiasts, students, and hobbyists, this project combines hardware assembly, Arduino programming, and wireless communication to create an interactive robotics platform.

### Project Overview:
This project transforms a standard 4WD robot chassis into a smart, wirelessly controlled vehicle using Arduino microcontroller, Bluetooth module, and motor driver circuitry.

### Learning Objectives:
Through this project, you'll gain hands-on experience with:
- Electronics circuit design and assembly
- Arduino programming in C++
- Wireless communication protocols
- Motor control principles
- Mobile-robot integration

## Features:

| Feature | Description |
|---------|-------------|
| **Wireless Control** | Bluetooth connectivity up to 10m range |
| **4WD System** | Four-wheel drive for superior traction |
| **Speed Control** | PWM-based variable speed adjustment |
| **Mobile Interface** | Custom Android/iOS control application |
| **Real-time Response** | Low latency control system |
| **Expandable** | Easy to add sensors and modules |
| **Open Source** | Complete code and documentation available |

##  Hardware Components:

###  Required Components:

| Component | Quantity | Specification | Approx. Price |
|-----------|----------|---------------|---------------|
| **Arduino Uno/Nano** | 1 | ATmega328P, 16MHz | $10-$20 |
| **L298N Motor Driver** | 1 | Dual H-Bridge, 2A per channel | $5-$8 |
| **HC-05 Bluetooth Module** | 1 | Bluetooth 2.0+EDR, 3.3V-5V | $4-$7 |
| **4WD Robot Chassis** | 1 | With 4 DC motors and wheels | $15-$25 |
| **18650 Battery Holder** | 1 | 2-cell with switch | $3-$5 |
| **18650 Batteries** | 2 | 3.7V, 2000mAh+ | $10-$15 |
| **Jumper Wires** | 20+ | Male-to-Male, Male-to-Female | $2-$4 |
| **Breadboard** | 1 | 400/800 points | $3-$5 |

### Additional Optional Components:

| Component | Purpose |
|-----------|---------|
| Ultrasonic Sensor (HC-SR04) | Obstacle detection |
| LED Strip | Lighting effects |
| Buzzer | Audio feedback |
| MPU6050 | Gyroscope/Accelerometer |
| OLED Display | Status monitoring |

## Circuit Diagram




### Connection Table

| Arduino Pin | L298N Pin | Bluetooth Module | Function |
|-------------|-----------|------------------|----------|
| **D5** | IN1 | - | Motor A Direction 1 |
| **D6** | IN2 | - | Motor A Direction 2 |
| **D9** | ENA | - | Motor A Speed (PWM) |
| **D7** | IN3 | - | Motor B Direction 1 |
| **D8** | IN4 | - | Motor B Direction 2 |
| **D10** | ENB | - | Motor B Speed (PWM) |
| **5V** | - | VCC | Bluetooth Power |
| **GND** | GND | GND | Common Ground |
| **TX (D1)** | - | RX | Serial Communication |
| **RX (D0)** | - | TX | Serial Communication |
| - | +12V | - | Motor Power (6-12V) |
| - | +5V | - | Logic Power (5V) |

### Power Connections

| Power Source | Connection Point | Voltage |
|--------------|------------------|---------|
| 18650 Battery Pack | L298N +12V | 7.4V |
| Arduino USB/5V | L298N +5V | 5V |
| Arduino 5V | HC-05 VCC | 5V |

## Installation

### Step-by-Step Setup

1. **Hardware Assembly**
   ```bash
   Step 1: Assemble the 4WD chassis with motors
   Step 2: Mount Arduino and L298N on chassis
   Step 3: Connect motors to L298N outputs
   Step 4: Wire power system and batteries
   Step 5: Connect all control wires as per circuit diagram
