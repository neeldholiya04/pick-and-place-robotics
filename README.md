
# Robotic Pick-and-Place System

This project focuses on developing an open-source robotic pick-and-place system utilizing the Braccio++ robotic arm, integrated with micro-ROS for precise object manipulation tasks.

## Features

- **Robotic Arm Control**: Utilizes the Braccio++ robotic arm for executing pick-and-place operations.
- **Micro-ROS Integration**: Employs micro-ROS for real-time communication and control.
- **Custom Arduino Firmware**: Includes tailored Arduino firmware to manage the robotic arm's movements.
- **Object Detection**: Incorporates YOLOv5 for object detection, enabling the system to identify and interact with various items.

## Repository Structure

The repository is organized as follows:

- **Arduino/**: Contains Arduino sketches and related code for controlling the Braccio++ arm.
- **pnp_ws/**: Houses the ROS workspace, including packages for object detection and system integration.
  - **src/ei_yolov5_detections/**: Features scripts for object detection using YOLOv5.

## Getting Started

To set up and run the Robotic Pick-and-Place System, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/neeldholiya04/pick-and-place-robotics.git
   ```

2. **Arduino Setup**:
   - Navigate to the `Arduino/` directory.
   - Open the Arduino IDE and load the provided sketch.
   - Upload the firmware to the Braccio++ robotic arm.

3. **ROS Workspace Setup**:
   - Ensure ROS 2 is installed on your system.
   - Navigate to the `pnp_ws/` directory.
   - Build the workspace:
     ```bash
     colcon build
     ```
   - Source the setup file:
     ```bash
     source install/setup.bash
     ```

4. **Running the System**:
   - Launch the ROS nodes:
     ```bash
     ros2 launch ei_yolov5_detections detection.launch.py
     ```
   - Ensure the Arduino firmware is running and connected to the ROS network.

## Dependencies

The project relies on the following dependencies:

- **Hardware**:
  - Braccio++ robotic arm
  - Arduino-compatible microcontroller

- **Software**:
  - Arduino IDE
  - ROS 2 (Foxy or later)
  - micro-ROS
  - YOLOv5
