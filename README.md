# IoT-Based Environmental Monitoring System

This project demonstrates the design, implementation, and evaluation of an IoT-based environmental monitoring system using an ESP32 microcontroller, MQTT protocol, and Node-RED. The system monitors temperature and humidity and allows remote control of an RGB LED through a web-based dashboard.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [Project Demonstration](#project-demonstration)
- [References](#references)

## Overview

This IoT system leverages the AZ-Delivery ESP32 microcontroller and DHT11 temperature and humidity sensors to collect environmental data, which is transmitted to a cloud platform using the MQTT protocol. The data is then visualized on a Node-RED dashboard, providing a user-friendly interface for real-time monitoring and control.

## Features

- **Real-time Environmental Monitoring**: Measures temperature and humidity using the DHT11 sensor.
- **MQTT-based Communication**: Sends data to the cloud and subscribes to control messages.
- **Remote LED Control**: RGB LED displays temperature status (blue: cold, green: normal, red: hot).
- **Historical Data Storage**: MongoDB integration for long-term data storage and analysis.

## Architecture

The architecture includes the following components:

- **ESP32 Microcontroller**: Captures sensor data and communicates over Wi-Fi.
- **MQTT Broker**: Facilitates data transfer between the ESP32 and the cloud.
- **Node-RED Dashboard**: Visualizes real-time and historical data and enables remote control of devices.
- **MongoDB**: Stores data for historical analysis.

## Hardware Requirements

- AZ-Delivery ESP32 NodeMCU Development Board
- DHT11 Temperature and Humidity Sensor
- RGB LED
- Power Supply (USB or battery pack)

## Software Requirements

- Arduino IDE (for ESP32 programming)
- Node-RED (for dashboard and data flow management)
- MongoDB (for data storage)

## Installation and Setup

1. **ESP32 Programming**: Use Arduino IDE to program the ESP32 with libraries like `WiFi.h` and `PubSubClient` for Wi-Fi and MQTT functionalities.
2. **Node-RED Setup**:
   - Install Node-RED: `npm install -g node-red`
   - Run Node-RED: `node-red`
3. **MQTT Configuration**:
   - Set up the MQTT broker at `broker.mqtt.cool` or your preferred MQTT broker.
4. **MongoDB Setup**:
   - Configure MongoDB for data storage, ensuring integration with Node-RED for storing sensor data.

## Usage

- Connect the ESP32 to Wi-Fi, and it will start publishing temperature and humidity data via MQTT.
- Access the Node-RED dashboard to view real-time data, retrieve historical data from MongoDB, and control the RGB LED based on environmental conditions.

## Future Enhancements

- **Improved Sensor Accuracy**: Replace DHT11 with DHT22 for better precision.
- **Expanded Sensor Network**: Add additional sensors for air quality and light monitoring.
- **Enhanced Connectivity**: Integrate LoRaWAN or 5G for stable remote monitoring.
- **Advanced Analytics**: Implement machine learning models for predictive analytics and anomaly detection.

## Project Demonstration

[Project Video Link](IoT_Assignment/IoT_Project_Video (1).mp4)

## References

- Rattanapoka, C., et al., "An MQTT-based IoT Cloud Platform with Flow Design by Node-RED," 2019 IEEE.
- D’Ortona, C., et al., "Open-Source MQTT-Based End-to-End IoT System," 2022 Future Internet.
