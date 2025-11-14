# Air Monitor System

**Course Project – Group of 2**

## Introduction
This is a course project carried out by a group of 2 students, aiming to build an **Air Quality Monitoring System**.  
The system collects environmental data from sensors and uploads it to a server for monitoring.

In this project, I am solely responsible for **hardware design** of both the **data collection Node** and the **Gateway**.  
All schematics, PCB layouts, energy-saving designs, and 3D models are part of my contribution. The software, dashboard, and Firebase integration are handled by the other team member.

---

## Main Features

### Node
- **Microcontroller Unit (MCU)**: STM32L151C8T6 – low-power series, optimized for energy efficiency  
- **Power supply**: Operates entirely on 3 18650 Li-ion batteries, no external power needed  
- **Energy-saving design**: Peripheral blocks are powered through transistors, allowing complete shutdown when not in use  
- **Sensors**:
  - PM2.5
  - Temperature & Humidity  
  - UV sensor  
- **Communication**: Sends collected data to the Gateway via LoRa

### Gateway
- **Power supply**: 220V AC input  
- **Voltage conversion**: Step-down through HiLink module on the board  
- **Functionality**:
  - Receives LoRa data from Node  
  - Converts LoRa data to Wi-Fi  
  - Uploads data to Firebase for storage and monitoring
