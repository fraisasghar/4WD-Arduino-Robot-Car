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

<br>



## Introduction:
Welcome to the **4WD Arduino Robot Car** project repository! This is a comprehensive, open-source robotics project that implements a fully functional 4-wheel drive robot car controlled wirelessly via Bluetooth from a mobile device. Designed for enthusiasts, students, and hobbyists, this project combines hardware assembly, Arduino programming, and wireless communication to create an interactive robotics platform.

### Project Overview:
This project transforms a standard 4WD robot chassis into a smart, wirelessly controlled vehicle using Arduino microcontroller, Bluetooth module, and motor driver circuitry.



![Image](https://github.com/user-attachments/assets/ee4ec3c8-16d7-49fc-9884-78d5903e9864)





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
| **Arduino Uno/Nano** | 1 | ATmega328P, 16MHz | 1000-1500 PKR |
| **L298N Motor Driver** | 1 | Dual H-Bridge, 2A per channel | 500-700 PKR |
| **HC-05 Bluetooth Module** | 1 | Bluetooth 2.0+EDR, 3.3V-5V | 700-900PKR |
| **4WD Robot Chassis** | 1 | With 4 DC motors and wheels | 1800-2200 PKR |
| **18650 Battery Holder** | 1 | 3-cell with switch | 200-300 |
| **18650 Batteries** | 2 | 3.7V, 2000mAh+ | 600-800 |
| **Jumper Wires** | 20+ | Male-to-Male, Male-to-Female | 100-200 |
| **Breadboard** | 1 | 400/800 points | 400-500 |

### Additional Optional Components:

| Component | Purpose |
|-----------|---------|
| Ultrasonic Sensor (HC-SR04) | Obstacle detection |
| LED Strip | Lighting effects |
| Buzzer | Audio feedback |
| MPU6050 | Gyroscope/Accelerometer |
| OLED Display | Status monitoring |

## Circuit Diagram


<img width="912" height="720" alt="Image" src="https://github.com/user-attachments/assets/75fc23a3-481d-4da5-9e5d-5f29707ecf53" />
<img width="1200" height="700" alt="Image" src="https://github.com/user-attachments/assets/4865ce66-9331-477b-a108-7dafa4fec372" />




## Installation

### Step-by-Step Setup

1. **Hardware Assembly**
   ```bash
   Step 1: Assemble the 4WD chassis with motors
   Step 2: Mount Arduino and L298N on chassis
   Step 3: Connect motors to L298N outputs
   Step 4: Wire power system and batteries
   Step 5: Connect all control wires as per circuit diagram. Make these 10 connections:
   • Arduino 5V → L298N +5V
   • Arduino GND → L298N GND
   • D5 → IN1, D6 → IN2, D9 → ENA
   • D7 → IN3, D8 → IN4, D10 → ENB
   • Battery + → L298N +12V.  Battery - → L298N GND
   • Arduino 5V → HC-05 VCC.  Arduino GND → HC-05 GND
   • Arduino TX → HC-05 RX.   Arduino RX → HC-05 TX
    Step 6. Upload the code. Pair Bluetooth (PIN: 1234). Test with mobile app





## 💻 Software Setup
```bash

       **Step 1: Install Arduino IDE**
1. Go to https://www.arduino.cc/en/software
2. Download Arduino IDE for your operating system
3. Install the software following on-screen instructions

       **Step 2: Get the Code**
1. Download this project as ZIP file
2. Extract the ZIP file to your computer
3. Open the folder and find the `src` folder

### Step 3: Upload Code to Arduino
1. Connect Arduino to computer using USB cable
2. Open Arduino IDE
3. Go to Tools → Board → Select "Arduino Uno"
4. Go to Tools → Port → Select correct COM port
5. Open the file `src/4wd_robot_car.ino`
6. Click Upload button (right arrow icon)
7. Wait for "Done uploading" message

## 📱 Mobile App Configuration

### Step 1: Install Bluetooth App
       For Android:
1. Open Google Play Store
2. Search for "Bluetooth RC Controller"
3. Install any of these apps:
   • "Arduino Bluetooth Controller"
   • "Bluetooth Controller for Arduino"
   • "BT Control - RC Controller"

### Step 2: Bluetooth Pairing
1. Turn ON the robot car power
2. Go to your phone's Settings → Bluetooth
3. Turn ON Bluetooth
4. Search for available devices
5. Find "HC-05" https in the list
6. Tap to pair
7. Enter PIN: 1234
8. Wait for "Paired" or "Connected" status

### Step 3: App Settings
1. Open the Bluetooth control app
2. Go to Settings or Connection menu
3. Select "HC-05" from device list
4. Configure these settings:

• Baud Rate: 9600
• Data Bits: 8
• Stop Bits: 1
• Parity: None

5. Save settings and tap "Connect"

```
### 📱 Mobile App Button Controls

| Button | Action | What Happens |
|--------|--------|--------------|
| ▲ Forward | Sends 'F' | Car moves forward |
| ▼ Backward | Sends 'B' | Car moves backward |
| ◀ Left | Sends 'L' | Car turns left |
| ▶ Right | Sends 'R' | Car turns right |
| ⏹ Stop | Sends 'S' | Car stops |
| 0-9 | Sends '0' to '9' | Changes speed (0=slow, 9=fast) |

## 🔧 Testing & Troubleshooting

### Initial Power Test:
1. Connect battery to car
2. Check these lights:
   - **Arduino** - Green power LED = ON
   - **L298N** - Red power LED = ON
   - **HC-05** - LED blinking (searching) or solid (connected)



### Common Problems & Solutions:

| Problem | Solution |
|---------|----------|
| **Car doesn't move** | Check battery connection, motor wires |
| **Bluetooth not connecting** | Re-pair device, use PIN: 1234 |
| **Only one side moves** | Check motor connections on that side |
| **Car moves opposite direction** | Swap the two motor wires |
| **Slow movement** | Charge batteries, check speed setting |
| **App not working** | Try different Bluetooth app |








<div align="center">
  <h3>🌟 Enjoy Your Robot Car! 🚗</h3>
  
  <p>If this project helped you, please give it a ⭐ Star on GitHub!</p>
  
  <p>
    <strong>Built with ❤️ for the Robotics Community</strong><br>
    <em>Happy Building! 🛠️</em>
  </p>
</div>


























---
</div>

<div align="center" style="background: linear-gradient(135deg, #00979d 0%, #ffd343 100%); padding: 20px; border-radius: 10px; margin: 30px 0;">

### 🏁 Final Note
**Your journey in robotics has just begun!**  
This car is not just a project—it's a platform for innovation, learning, and discovery.

**Keep Building • Keep Learning • Keep Innovating**

[![Made with Arduino](https://img.shields.io/badge/Made%20with-Arduino-00979D?style=for-the-badge&logo=arduino)](https://arduino.cc)
[![Open Source](https://img.shields.io/badge/Open%20Source-❤-red?style=for-the-badge)](https://opensource.org)

</div>

<div align="center">

---
**© 2023 AWD Arduino Robot Car Project**  
*All designs, code, and documentation open for innovation*

**📧 Contact:** project@example.com  
**🐦 Twitter:** @ArduinoRobotCar  
**📱 Instagram:** @arduino_robot_car

---
</div>

<div align="center">
<sub>🚗 Drive into the future of robotics! 🚀</sub>
</div>

