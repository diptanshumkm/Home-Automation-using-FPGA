# Home Automation Using FPGA

## Overview

Home automation is the process of using technology to control various home features automatically and remotely. This project focuses on creating a **fire alarm system** using an FPGA (Field-Programmable Gate Array). The system is designed to detect fire through a sensor, process the data using an FPGA, and trigger an alarm via a buzzer. The system aims to improve safety, comfort, and energy efficiency within the home environment.

## Why FPGA?

FPGA, or Field-Programmable Gate Array, is an integrated circuit that can be programmed after manufacturing. It consists of an array of configurable logic blocks that can be connected to create custom hardware circuits. This flexibility allows for the development of a tailored hardware architecture specific to the needs of home automation, such as the fire alarm system in this project.

## Project Components

### Fire Alarm System

The core of this project is an FPGA-based fire alarm system that includes:

- **Fire Sensor:** Detects the presence of smoke or fire.
- **FPGA (ZedBoard):** Processes sensor data and controls the buzzer.
- **Buzzer:** Sounds an alarm when a fire is detected.

### Hardware Used

- **ZedBoard:** The FPGA development board used to execute the project.
- **Fire Sensor:** YG1006 Photo Transistor, used to detect fire by identifying infrared radiation emitted by flames.
- **Piezoelectric Buzzer:** Emits sound when activated by the FPGA upon detecting fire.
- **Breadboard and Jumper Wires:** Used for connecting various components.

### Software Used

- **Vivado Design Suite:** Xilinx's software environment used for developing electronic systems with FPGAs. It supports HDL editing, simulation, synthesis, and implementation.

## Hardware Setup

The hardware setup includes connecting the ZedBoard, fire sensor, and buzzer using a breadboard and jumper wires. The fire sensor detects fire and sends a digital signal to the ZedBoard. The ZedBoard processes this signal and sends a command to the buzzer to emit a sound if a fire is detected.

### Fire Sensor Specifications

- **Operating Voltage:** 3.3V to 5V
- **Operating Current:** 15 mA
- **Sensor Type:** YG1006 Photo Transistor
- **Comparator Chip:** LM393
- **Pins:** Digital output, GND, VCC

### How the Fire Sensor Works

1. **Detection Method:** The YG1006 photo transistor detects fire by identifying infrared radiation emitted by flames. In the absence of fire, reflected infrared does not hit the phototransistor.
2. **Digital Output:** The sensor has an internal comparator circuit that compares the phototransistor current to a threshold. If the current exceeds this threshold (indicating fire), the sensor outputs a high voltage level (Digital Logic 0).

### Buzzer Operation

The piezoelectric buzzer operates when it receives a digital logic ‘1’ from the FPGA, which occurs when the fire sensor detects a fire. The buzzer then emits a sound due to the piezoelectric effect.

### System Logic

1. The fire sensor sends a digital logic '0' to the ZedBoard when fire is detected.
2. The FPGA processes this signal and outputs a digital logic '1' to the buzzer.
3. The buzzer responds by emitting an alarm sound.

### Interfacing Components

The fire sensor and buzzer are connected to the PMOD interface of the ZedBoard, which standardizes the connection of sensors and other peripherals to the board.

## Execution

The project demonstrates the integration of FPGA technology with home automation systems, specifically focusing on fire detection and alarm. The use of an FPGA allows for custom logic design tailored to the application, making it a powerful tool for such safety-critical systems.

## Conclusion

This project showcases the application of FPGA in home automation, emphasizing the benefits of using configurable hardware for creating efficient and responsive systems. The fire alarm system is just one example of how FPGA can be utilized for enhancing home safety through automation.
