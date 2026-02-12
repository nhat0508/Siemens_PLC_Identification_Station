# Siemens_PLC_Identification_Station
"Automated Pick-and-Place &amp; Identification Station using Siemens PLC. Features Multi-sensor Classification, Shift Register Logic, and Advanced Alarm Handling."

# Identification & Pick-and-Place Station 🤖

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Platform](https://img.shields.io/badge/Platform-Siemens_TIA_Portal_V18-blue)

## 📖 Introduction
This project simulates an industrial Quality Control (QC) station. It utilizes a linear manipulator equipped with a vacuum gripper to identify, classify, and sort workpieces based on their material properties (Metal vs. Non-metal vs. Raw material).

The control logic is developed on **Siemens S7-1200 PLC** and visualized via **SIMATIC HMI**, demonstrating advanced sensor integration and error handling capabilities.

---

## ⚙️ Key Features
* **Multi-Sensor Fusion:** Integrates three different sensor types to classify incoming products:
    * **Inductive Sensor:** Detects metallic components.
    * **Capacitive Sensor:** Measures material density/thickness.
    * **Optical Sensor (Photocell):** Detects object presence.
* **Fault Detection & Alarms:**
    * **Actuator Timeout:** Triggers an alarm if the gripper cylinder takes >2 seconds to reach position (detecting jams or air leaks).
    * **Emergency Stop:** Immediate system halt and HMI notification upon E-Stop activation.
* **Modular Code Structure:** Logic is organized into reusable **Function Blocks (FBs)** (e.g., `Motor_Control`, `Sensor_Processing`) following IEC 61131-3 standards.

## 🛠️ Technology Stack
* **PLC:** Siemens S7-1200 CPU
* **HMI:** SIMATIC TP700 Comfort / KTP700 Basic
* **Software:** TIA Portal V18
* **Languages:** Function Block Diagram (FBD), Structured Control Language (SCL)
* **Hardware:** Vacuum Suction Cup, Pneumatic Cylinders, Linear Axis Motor

## 📂 Project Structure
* `/Identification Station`: Archived TIA Portal project file (`.ap18`).
* `/Docs`: I/O Lists and Functional Descriptions.
* `/HMI_Screens`: User interface designs for Manual/Auto modes.

## 🚀 How to Run
1.  Open **TIA Portal V18**.
2.  Retrieve the archived project file from the `Identification Station' folder.
3. Extract the"FB_library_AE23_IEPIP24.7z" and put it in the same folder with `Identification Station' folder.
4.  Simulate with **PLCSIM** or download to hardware.
4.  Use the HMI to perform the **Reference Run** (Home position) before starting **Auto Mode**.

---
*Created by Minh Nhat Nguyen - Automation Engineering Student @ SeAMK*
