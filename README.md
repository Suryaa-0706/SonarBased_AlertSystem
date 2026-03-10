# 📡 Sonar-Based Alert System | Autonomous Obstacle Avoidance

An interactive, web-based simulation and documentation of a Sonar-Based Alert System. This project demonstrates how an autonomous mobile robot uses ultrasonic pulses and servo-assisted scanning to detect and navigate around obstacles in real-time.

---

## 🚀 Overview
This project was developed by **Group 8** to showcase a low-cost, contactless safety solution. By mounting an ultrasonic sensor on a rotating servo motor, the system achieves a wide-angle "sonar" sweep, mimicking radar technology to identify objects within its path.

### Key Features:
* **180° Radar Sweep:** Uses a servo motor to scan the environment.
* **Real-time HUD:** Interactive heads-up display showing distance, angle, and robot status.
* **Object Tracking:** Visual representation of detected "foreign bodies."
* **Autonomous Logic:** Decision-making algorithms for "Scanning," "Forward," and "Avoidance" (Backing/Turning) modes.

---

## 🛠 Hardware Architecture
The logic showcased in this webpage is designed to be implemented with the following hardware:

| Component | Function |
| :--- | :--- |
| **Arduino UNO** | The central processing unit for sensor logic and motor control. |
| **HC-SR04 Sensor** | Emits ultrasonic waves to calculate distance to the nearest object. |
| **Servo Motor** | Rotates the sensor to provide a wide-angle field of view. |
| **LCD 16x2 (I2C)** | Displays system status: `SCANNING`, `WARNING`, or `AREA CLEAR`. |
| **Buzzer & LEDs** | Provides immediate audio-visual alerts when an object is too close. |

---

## 🎮 How to Use the Simulation
1.  **Open the Webpage:** Open `sonar_alert_system (1).html` in any modern web browser.
2.  **Toggle Simulation:** Use the "START/STOP" button to engage the robot.
3.  **Interact:** * Click anywhere on the map to **Place Obstacles**.
    * Use the **Control Panel** to adjust movement speed and sensor sensitivity.
    * Monitor the **Live Radar** at the bottom left for angle-specific detections.

---

## 📂 Project Structure
* `sonar_alert_system (1).html` — The complete interactive simulation, logic, and GUI.
* `assets/` — (Optional) Folder for images or diagrams.
* `arduino_code/` — (Optional) Folder for your `.ino` source files.

---

## 📝 Methodology
The system follows a specific operational loop:
1.  **Initialize:** Calibrate sensors and set the servo to the center position.
2.  **Sweep:** The servo moves from 0° to 180°, triggering the ultrasonic sensor at every step.
3.  **Evaluate:** If an object is detected within the threshold (e.g., < 15cm), the system enters `ALERT` mode.
4.  **React:** The robot stops, reverses, and turns to find a clear path before resuming forward motion.

---

## 👥 Contributors (Group 8)
1. M Mahendra - CB.SC.U4AIE24033
2. K Siva Kumar - CB.SC.U4AIE24027
3. K Usman Shareef - CB.SC.U4AIE24024
4. G Chaitanya Varma - CB.SC.U4AIE24017

---
*Developed for the Robotics and Autonomous Systems Project.*
