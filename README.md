# Portable Heart Rate Monitor

This repository contains the documentation and development details for the **Portable Heart Rate Monitor** project developed as part of the **EEP3020 Digital Systems Lab** course at IIT Jodhpur.

## Table of Contents

- [Project Overview](#project-overview)
- [Objective](#objective)
- [Components Used](#components-used)
- [System Overview](#system-overview)
- [Features](#features)
- [Working Principle](#working-principle)
- [How to Use](#how-to-use)
- [Future Improvements](#future-improvements)

## Project Overview

This project aims to develop a **Portable Heart Rate Monitoring System** that can measure and display heart rate data in real-time using a low-cost embedded setup.

## Objective

To design a compact, real-time heart rate monitor capable of measuring a user's pulse through a sensor and displaying the result, making it suitable for wearable or mobile healthcare systems.

## Components Used

- MAX30100 Heart Rate Sensor
- ESP8266
- Battery Power Supply
- Supporting passive components and interconnects

## System Overview

The MAX30100 sensor detects pulse rate through optical reflectance and transmits data to ESP8266, which processes the signal and displays the heart rate on the dashboard.

## Features

- Real-time heart rate measurement
- Compact and low-power design
- Portable form factor
- Embedded signal processing using STM32

## Working Principle

The system uses photoplethysmography (PPG) to detect blood volume changes in the fingertip using infrared light. ESP8266 board processes the analog waveform, detects peaks, and computes beats per minute (BPM).

## How to Use

1. Power on the device.
2. Place your finger on the MAX30100 sensor.
3. Wait for a few seconds while the device calculates your heart rate.
4. Read the BPM value displayed on the Blynk Cloud dashboard.

## Circuit Connections

The following table shows the connections between the MAX30100 sensor and the ESP8266 module:

| MAX30100 Pin | ESP8266 Pin   |
|--------------|---------------|
| VCC          | 3.3V          |
| GND          | GND           |
| SDA          | D2 (GPIO 4)   |
| SCL          | D1 (GPIO 5)   |

*Table 1: Circuit Connections*


## Future Improvements

- Add SpO₂ measurement feature
- Integrate Bluetooth for wireless data transmission
- Improve power management for longer battery life
- Use machine learning for artifact detection

---

> This project was submitted as part of the coursework for *EEP3020 Digital Systems Lab*.
