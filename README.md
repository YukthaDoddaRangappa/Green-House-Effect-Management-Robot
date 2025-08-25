# Greenhouse Effect management robo
Features

Environmental Monitoring:

Temperature & Humidity → DHT11 Sensor

CO₂ levels → MQ135 Gas Sensor

Soil Moisture → Resistive Soil Sensor

Automation:

Fan Control: Automatically turns ON when temperature > 30°C

Pump Control: Activates when soil moisture is below threshold

Robot Mobility: Moves using motor drivers and wheels

IoT Integration:

ESP32 Wi-Fi module sends sensor data to ThingSpeak Cloud

Remote monitoring of temperature, humidity, CO₂, and soil data

🖥User Interface:

LCD Display for local real-time readings

ThingSpeak Dashboard for cloud visualization

Tech Stack & Hardware

Microcontrollers

Arduino Nano

ESP32 Wi-Fi Module

Programming

Embedded C

Arduino IDE

Sensors

DHT11 (Temperature & Humidity)

MQ135 (CO₂ Gas Sensor)

Soil Moisture Sensor

Actuators

Relay Modules (Fan & Pump control)

Motor Drivers (L298N / L293D)

DC Motors + Wheels

Display

16x2 LCD with I2C Module

Cloud

ThingSpeak IoT Platform

Circuit Overview

DHT11 → Arduino Nano digital pin

MQ135 → Analog pin A0

Soil Moisture → Analog pin A1

Relays (Fan & Pump) → Digital pins D5, D6

Motors → Controlled via motor driver (pins D9–D12)

ESP32 → Connected via UART (Wi-Fi data transmission)

LCD (I2C) → Connected via SDA/SCL


Install Arduino IDE

Install Libraries:

DHT.h

LiquidCrystal_I2C.h

WiFi.h

HTTPClient.h

 Clone Repository
git clone https://github.com/YukthaDoddaRangappa/Green-House-Effect-Management-Robot
cd IoT-Greenhouse-Robot/code


Upload Code

Connect Arduino Nano & ESP32 to your PC.

Open greenhouse_robot.ino in Arduino IDE.

Select correct Board & COM Port.

Upload the code.

ThingSpeak Setup

Create a free account at ThingSpeak
.

Create a New Channel with fields:

Field 1 → Temperature

Field 2 → Humidity

Field 3 → CO₂ Level

Field 4 → Soil Moisture

Copy your Write API Key and paste it in the Arduino code.

After uploading, go to your channel → "Private View" → see live sensor graphs.

Example Working

Temperature rises above 30°C → Fan turns ON

Soil moisture drops below threshold → Pump turns ON

CO₂ levels rise → System can trigger ventilation (fans/motors)

Robot Mobility → Moves forward/backward periodically for ventilation & irrigation coverage

ThingSpeak Dashboard → Displays live environmental data in graphs

Future Enhancements

Add mobile app for control (Blynk/Firebase).

 Store long-term data in Google Firebase / AWS IoT.

 Add AI/ML models for predictive irrigation.

Use solar panels for energy sustainability.

👨‍💻 Author

Developed by Yuktha D
