# Auto Rickshaw Fare Meter System

## Overview

This project is a **smart auto rickshaw fare meter** built using Arduino. It calculates fare based on distance traveled, adds waiting charges when the vehicle is idle, and detects obstacles using sensors. The system displays real-time data such as distance, speed, and fare on an LCD screen.

---

## Features

* Distance measurement using Hall sensor (wheel rotation)
* Automatic fare calculation
* Waiting charge calculation based on speed
* GPS-based speed monitoring
* Obstacle detection using Ultrasonic and IR sensors
* Real-time display on LCD
* Start, Stop, and Reset controls

---

## Components Used

* Arduino Uno
* 16x2 LCD (I2C)
* Hall Effect Sensor
* GPS Module (NEO-6M)
* Ultrasonic Sensor (HC-SR04)
* IR Sensor
* Push Buttons (Start, Stop, Reset)
* LED
* Breadboard and jumper wires
* Power supply

---

## Working Principle

1. The system starts when powered ON and initializes all components.
2. Pressing the **Start button** activates the ride.
3. Distance is calculated:

   * Using Hall sensor (real mode), or
   * Simulated increment (demo mode)
4. GPS module provides real-time speed.
5. Fare is calculated:

   * Base fare for initial distance
   * Additional charges for extra distance
6. If speed is low, waiting charges are added.
7. Ultrasonic sensor detects nearby obstacles and turns ON LED.
8. IR sensor detects object presence.
9. All data is displayed on the LCD and Serial Monitor.
10. **Stop button** ends the ride (data preserved).
11. **Reset button** clears all values for a new ride.

---

## Fare Calculation Logic

* Base Fare: ₹36 for first 0.5 meters
* Additional Fare: ₹1 per 0.4 meters
* Waiting Charge: ₹2 every 5 seconds when speed < 1 km/h

---

##  Pin Connections

| Component       | Arduino Pin |
| --------------- | ----------- |
| Hall Sensor     | D2          |
| Start Button    | D3          |
| Stop Button     | D4          |
| Reset Button    | D5          |
| IR Sensor       | D6          |
| GPS RX/TX       | D7, D8      |
| Ultrasonic Trig | D9          |
| Ultrasonic Echo | D10         |
| LED             | D13         |

---

## Output Display

### LCD:

* Distance (meters)
* Fare (₹)
* Speed (km/h)
* Ride status (ON/OFF)

### Serial Monitor:

* Ultrasonic distance
* IR detection status
* Distance traveled
* Speed
* Fare

---

## Demo Mode

For demonstration without moving the vehicle:

* Distance increases automatically every 2 seconds
* Speed increases gradually (limited to 5 km/h)

---

## Applications

* Auto rickshaw fare automation
* Smart transportation systems
* Low-cost fare meter solutions
* Embedded systems learning projects

---

## Future Improvements

* Mobile app integration
* Digital payment system
* GPS route tracking
* Cloud data storage

---

## Conclusion

This project demonstrates how embedded systems and sensors can be used to build an efficient and automated fare meter system. It is cost-effective, scalable, and suitable for real-world applications with further enhancements.

---
