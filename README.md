# Fire Detection System (Smoke & Heat)

A comprehensive fire safety solution designed to detect both smoke and fire using infrared technology and thermal sensing. This project was developed as an assignment for the **Electrical Electronic Circuits (CO2037)** course at **Ho Chi Minh City University of Technology (HCMUT)**.

## Highlights
* **Dual-Detection System**: Combines smoke detection (IR-T/R pair) with heat detection (thermistor) to minimize false alarms and ensure detection even for fires without smoke.
* **Integrated Power Supply**: Includes a dedicated power management circuit to provide stable 5V power to internal components and external devices.
* **Audible & Visual Alerts**: Triggers both a buzzer and triple-LED signaling for immediate notification.
* **Professional PCB Design**: Developed using **Altium Designer** with optimized component placement to prevent thermal damage to critical electronics.

## Overview
### 1. Principle of Operation
The system monitors two critical environmental factors to ensure early warning:
* **Smoke Detection**: Uses an Infrared Emitter (IR-T) and Receiver (IR-R) pair. When smoke reduces the infrared intensity between them, the change triggers the alarm.
* **Heat Detection**: Utilizes a thermal resistor (RT1) that activates khi nhiệt độ môi trường tăng cao, đảm bảo phát hiện được cả những đám cháy ít khói.



### 2. Key Specifications
* **Power Source**: 12V DC input connector (CON1), được điều chỉnh xuống mức 5V ổn định nhờ IC ổn áp 7805.
* **Processing Core**: Sử dụng IC OP-AMP LM358 để so sánh tín hiệu từ cảm biến và xử lý ngưỡng kích hoạt.
* **Safety Thresholds**: Được thiết lập để kích hoạt khi vượt qua các ngưỡng điện áp xác định (ví dụ: phần nhiệt độ được tính toán kích hoạt ở khoảng 316°C).

## Hardware Components
| Component Type | Label | Key Valuation |
| :--- | :--- | :--- |
| **IC OP-AMP** | U1A, U1B | LM358 (5V Input) |
| **Voltage Regulator**| U2 | 7805 (12V to 5V) |
| **Heat Sensor** | RT1 | 10kΩ Thermistor |
| **Notification** | Buzzer, D1-D3| 1.5V Speaker & 1N4007 Diodes |
| **Transistors** | Q1, Q2, Q3 | NPN & PNP for signal amplification |

## Getting Started

### 1. Requirements
* **Software**: Altium Designer (để xem/chỉnh sửa bản vẽ PCB).
* **Hardware**: Nguồn DC 12V 2A.

### 2. Implementation & Design Rules
* **Trace Constraints**: A track width of 10mil is applied to the entire design to ensure electrical isolation, prevent arcing, and maintain stable thermal management.
* **Component Placement**: The heat sensor is placed before the smoke detector to ensure high temperatures are detected before the flame can damage other components on the circuit board.
* **Calibration**: The sensitivity of the system can be adjusted through variable resistors **RV1** and **RV2**.

## ✍️ Author
* **Nguyen Hieu Trung** - MSSV: 2353244

---
© 2026 HCMUT - Faculty of Applied Science.
