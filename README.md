# Autonomous-Parcel-Sortation-For-Warehouse
A swarm robotics system for automated package sorting using computer vision and centralized navigation control
# Project Overview
This project implements an autonomous parcel sorting system using mobile robots with centralized monitoring and navigation. The system uses computer vision for robot tracking and package destination identification
# Features
* Centralized Navigation System: Overhead camera system for real-time robot tracking and control
* Computer Vision Integration: ArUco markers for robot orientation tracking and QR code scanning for package destinations
* MQTT Communication: Real-time command transmission between central system and robots
* Precision Control: Stepper motors for accurate movement and servo motors for package dropping
* Swarm Intelligence: Multiple robots working collaboratively to maximize throughput
* Real-time Performance: Average task completion time of 20-25 seconds per package
# Performance Metrics
| Metric | Value |
|--------|-------|
| Average Task Time | 20-25 seconds |
| Minimum Task Time | 5 seconds |
| Maximum Task Time | 25 seconds |
| Packages Delivered (10 min, 2 bots) | 55 packages |
| Package Drop Time | 1.5 seconds |
| Drop Accuracy | 90% |
## 🏗️ System Architecture

### Hardware Components
- **Robot Dimensions**: 6x6 inch constraint
- **Navigation**: Overhead camera system (no onboard sensors)
- **Tracking**: ArUco markers mounted on each robot
- **Package Scanning**: Two cameras at induct stations
- **Motors**: 
  - Stepper motors for movement control
  - MG90S Servo motor for dropping mechanism
- **Communication**: MQTT protocol

### Software Components
- Central monitoring and navigation system
- Computer vision processing for robot tracking
- QR code scanning for package destination identification
- Swarm coordination algorithms
- Real-time command distribution system

## 🎮 How It Works

1. **Package Input**: Operators load packages at two induct zones
2. **Destination Identification**: QR codes on packages are scanned to determine destination chutes
3. **Robot Assignment**: Central system assigns robots to packages based on availability and optimization
4. **Navigation**: Overhead camera tracks robots using ArUco markers and provides navigation commands
5. **Package Transport**: Robots pick up packages and navigate to designated chutes
6. **Package Delivery**: Servo-controlled dropping mechanism places packages in correct chutes
7. **Return Cycle**: Robots return to induct zones for next packages

## 📋 Competition Requirements

- **Package Loading**: Only one package per robot at a time
- **Color Coding**: Packages to same destination share the same color
- **Operator Requirement**: Two operators (one per induct zone)
- **Loading Constraint**: Packages loaded only when robots are within induct zones
- **Dynamic Mapping**: Robots autonomously decide destination-to-chute mappings

## 🛠️ Setup and Installation

### Prerequisites
- Python 3.x
- OpenCV for computer vision processing
- MQTT broker for communication
- Camera setup (1 overhead + 2 at induct stations)

### Hardware Setup
1. Install overhead camera system for arena monitoring
2. Position two cameras at induct stations for QR scanning
3. Set up robot charging/starting positions
4. Configure MQTT network for robot communication
5. Calibrate ArUco marker detection system

## 🎥 Demo

Watch our system in action: [Project Video](https://drive.google.com/drive/folders/1Xh0h8N9njuTw0Y-jtPcZ83GAZxs9W63K?usp=share_link)
