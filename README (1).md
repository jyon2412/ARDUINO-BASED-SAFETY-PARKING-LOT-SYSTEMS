# Arduino-Based Safety Parking Lot System 

## 📌 Overview
This project demonstrates a **smart parking safety system** using an Arduino Uno, ultrasonic distance sensing, and a servo motor barrier.  
It prevents low-speed collisions in parking structures by actively monitoring clearance distance and deploying a barrier when vehicles approach too close to walls or boundaries.

---

## 🎯 Problem Statement
Drivers often misjudge the clearance distance between their vehicle and structural walls in parking bays, leading to minor but cumulative collisions.  
Traditional passive measures (painted lines, bumpers) fail to actively prevent impact.  
This system introduces **real-time monitoring and automated intervention** to eliminate such damage.

---

## 🛠️ Objectives
- Real-Time Distance Monitoring using ultrasonic sensor  
- Automated Barrier Deployment with servo motor  
- Collision Mitigation by enforcing a minimum buffer distance  
- Low-Cost Prototype built with accessible microcontroller hardware  

---

## ⚙️ Components
| Component | Specification | Purpose |
|-----------|---------------|---------|
| Arduino Uno (Rev 3) | Microcontroller | Runs embedded logic, processes sensor data, controls servo |
| HC-SR04 Ultrasonic Sensor | 40 kHz | Measures vehicle distance in real time |
| TowerPro SG90 Micro Servo | 9g, 1.8 kg·cm torque | Deploys barrier arm between open (0°) and block (90°) |
| Breadboard | Solderless | Circuit prototyping hub |
| Jumper Wires | Flexible | Connects modules |
| USB Cable | 5V Power | Powers Arduino and peripherals |
| Cardboard Base | Parking bay model | Simulates parking layout |

---

## 🔬 Working Principle
1. **Ultrasonic Sensing**  
   - Arduino sends a 10 µs pulse to TRIG pin  
   - Sensor emits 40 kHz bursts, measures echo duration  
   - Distance calculated:  
     

\[
     \text{Distance (cm)} = \frac{t \times 0.0343}{2}
     \]



2. **Decision Control**  
   - Safe Zone: \(d > d_{threshold}\) → Servo at 0° (Barrier Open)  
   - Collision Zone: \(d \le d_{threshold}\) → Servo at 90° (Barrier Deployed)  

---

## 🖥️ System Flow
1. Power Initialization  
2. Trigger Pulse Generation  
3. Echo Time Measurement  
4. Distance Calculation  
5. Threshold Evaluation  
6. Barrier Deployment / Retraction  

---

## ✅ Advantages
- Automated, non-contact sensing  
- Active barrier intervention  
- Low power, cost-effective  
- Modular deployment across multiple bays  

---

## ⚠️ Limitations
- Limited torque of SG90 servo (prototype scale only)  
- Sensor angle (~15°) may miss curved bumpers  
- Environmental sensitivity (temperature, dust, reflections)  
- Voltage sag during motor stall  

---

## 🚀 Future Scope
- Industrial-grade actuators (boom gates, hydraulic stoppers)  
- LCD + LED + buzzer warnings  
- IoT integration with ESP32 for cloud analytics  
- Sensor fusion with IR/LiDAR  

---

## 📂 Repository Structure
