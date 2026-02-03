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






<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" alt="Bottom Line" width="100%" />
</div>





## Introduction:
Welcome to the **4WD Arduino Robot Car**  project repository! This is a comprehensive, open-source robotics project that implements a fully functional 4-wheel drive robot car controlled wirelessly via Bluetooth from a mobile device. Designed for enthusiasts, students, and hobbyists, this  project  combines  hardware  assembly, Arduino programming, and wireless communication to create an interactive robotics platform.

### Project Overview:
This project transforms a standard 4WD robot chassis into a smart, wirelessly  controlled  vehicle  using the  Bluetooth module,Arduino microcontroller, and motor driver circuitry.



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


## Hardware Assembly
   ```bash

   Step 1: Assemble the 4WD chassis with motors
   Step 2: Mount Arduino and L298N on chassis
   Step 3: Connect motors to L298N outputs
   Step 4: Wire power system and batteries
   Step 5: Connect all control wires as per circuit diagram. Make these 10 connections:
   • Arduino 5V → L298N +5V  • Arduino GND → L298N GND
   • D5 → IN1, D6 → IN2, D9 → ENA, D7 → IN3, D8 → IN4, D10 → ENB
   • Battery + → L298N +12V.  Battery - → L298N GND
   • Arduino 5V → HC-05 VCC.  Arduino GND → HC-05 GND
   • Arduino TX → HC-05 RX.   Arduino RX → HC-05 TX
    Step 6. Upload the code. Pair Bluetooth (PIN: 1234). Test with mobile app.
```
## Software Setup:
```
Step:1. Go to https://www.arduino.cc/en/software   Download Arduino IDE for your operating system

Step 2: Upload Code to Arduino
   • Find the code in `src` folder. Connect Arduino to computer using USB cable
   • Go to Tools → Board → Select "Arduino Uno"
   • Go to Tools → Port → Select correct COM port
   • Open the file `src/4wd_robot_car.ino`. Or just paste the code.
   • Click Upload button (right arrow icon). Wait for "Done uploading" message

Step 3: Install any of these apps:
   • "Arduino Bluetooth Controller" • "Bluetooth Controller for Arduino" • "BT Control - RC Controller"

Step 4: Bluetooth Pairing
   • Turn ON the robot car power. Turn ON Bluetooth
   • Search for available devices. Find "HC-05" https in the list
   • Tap to pair. Enter PIN: 1234. Wait for "Paired" or "Connected" status

Step 5: App Settings
   • Open the Bluetooth control app. Go to Settings/Connection menu. Select "HC-05" from device list.
   • Configure these settings:
   • Baud Rate: 9600   • Data Bits: 8  • Stop Bits: 1   • Parity: None
   • Save settings and tap "Connect"
```


## 🔧 Testing & Troubleshooting

Connect battery to car. Check these lights:
   - **Arduino** - Green power LED = ON
   - **L298N** - Red power LED = ON
   - **HC-05** - LED blinking (searching) or solid (connected).



### Common Problems & Solutions:

| Problem | Solution |
|---------|----------|
| **Car doesn't move** | Check battery connection, motor wires |
| **Bluetooth not connecting** | Re-pair device, use PIN: 1234 |
| **Only one side moves** | Check motor connections on that side |
| **Car moves opposite direction** | Swap the two motor wires |
| **Slow movement** | Charge batteries, check speed setting |
| **App not working** | Try different Bluetooth app |




<br>


<div align="center">
  <h3>🌟 Enjoy Your Robot Car! 🚗</h3>
  
  <p>If this project helped you, please give it a ⭐ Star on GitHub!</p>
  
  <p>
    <strong>Built with ❤️ for the Robotics Community</strong><br>
    <em>Happy Building! 🛠️</em>
  </p>
</div>







<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" alt="Bottom Line" width="100%" />
</div>
