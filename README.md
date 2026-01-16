
# Lab Data System – LabVIEW Project

## Overview
**Lab Data System** is a LabVIEW-based application designed for **real-time monitoring, logging, and analysis** of laboratory sensor data.  
The system supports **Pressure, Temperature, Salinity, and Weight** measurements with live visualization, calibration, configurable settings, and automatic report generation.

---

## Features
- Real-time monitoring of multiple sensors
- Live graphs and current value display
- Sensor calibration using linear equations
- Data logging (**CSV / TDMS**)
- Configurable sampling rate and graph scaling
- RS-232 communication support
- NI cDAQ (4–20 mA) support
- Optional live measurement statistics

---

## Supported Sensors
| Sensor | Signal | Range |
|------|-------|-------|
| Pressure | 4–20 mA | 0–60 bar |
| Temperature | 4–20 mA | 0–200 °C |
| Salinity | 4–20 mA | 0–100,000 ppm |
| Weight | RS-232 | 0–220 g |

---

## Hardware Requirements
- Windows PC (Windows 10 / 11)
- NI cDAQ USB device (VISA compatible)
- Pressure, Temperature, Salinity sensors (4–20 mA)
- Weight balance device with RS-232 interface
- Power supply and required electrical components

---

## Software Requirements
- **LabVIEW 2024 or later**
- **NI-DAQmx**
- **NI-VISA**
- Windows OS

---

## System Architecture
### Inputs
- Pressure, Temperature, Salinity sensors via NI cDAQ
- Weight sensor via RS-232

### Outputs
- Real-time graphs
- CSV or TDMS log files
- Calibration parameters
- Optional statistics

### Communication
- **NI cDAQ (USB / VISA)**
  - RSE mode
  - Channels: 0, 1, 2
- **RS-232**
  - Baud rate: 9600
  - Data bits: 8
  - Parity: None
  - Stop bits: 1
  - Flow control: None

---

## Calibration Method
Each sensor uses the following equation:

```
Sensor Value = M × Sensor Output (mA) + C
```

Default values:
- Pressure: `M = 3`, `C = 0`
- Temperature: `M = 10`, `C = 0`
- Salinity: `M = 5000`, `C = 0`

Manual offset and two-point calibration are supported.

---

## How to Run
1. Open **LabVIEW**
2. Open the project file:
   ```
   Lab Data System.lvproj
   ```
3. Run the **Main UI VI**
4. Configure settings and start measurement

---

## Data Logging
- Supported formats:
  - CSV
  - TDMS
- Reports are generated automatically and saved under:
  ```
  C:\Program Files (x86)\Lab Data System\Reports
  ```

---

## Use Cases
- Laboratory testing
- Sensor validation
- Industrial data acquisition
- Research and development experiments

---

## Author
**Mohamed Abdelmageed Jaheen**  
📧 Mohamed.a.jaheen@gmail.com

---

## License
This project is provided for **educational and industrial demonstration purposes**.
