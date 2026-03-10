# SonarBased_AlertSystem

🚀 Overview
This project is a low-cost, contactless safety solution designed to detect nearby obstacles using ultrasonic pulses. The system uses a servo motor to rotate the sensor, allowing for a wider scanning field than a stationary sensor.

🛠 Hardware Components
Arduino UNO: The main microcontroller "brain" of the system.

Ultrasonic Sensor: Detects objects via sound wave reflection.

Servo Motor: Rotates the sensor for 180-degree scanning.

LCD Interface: Displays real-time scanning status and distance.

Buzzer/LED: Provides audio and visual warnings upon detection.

⚙️ Methodology
INIT: System initializes, LCD shows "Scanning...", and servo moves to the start position.

SCAN: Servo rotates the ultrasonic sensor while it emits pulses.

DETECT: Arduino calculates distance. If an object is within the threshold, an alert triggers.

ALERT: LCD displays "WARNING FOREIGN BODY!" and the buzzer/LED turn ON.

CLEAR: If no object is detected, LCD shows "AREA IS EMPTY."

💻 Simulation
This repository includes a web-based simulation (see sonar_alert_system.html) that provides a top-down view of the robot's obstacle avoidance logic, including adjustable sensor ranges and robot speeds.
