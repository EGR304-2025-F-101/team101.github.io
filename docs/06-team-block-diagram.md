---
title: Team Block Diagram
---
## Introduction
The system consists of Four interconnected subsystems—Control, Sensor, Speaker and Motor with each built using the PIC18F57Q43 Curiosity Nano. The Control unit processes sensor inputs and sends commands to the motor subsystem through 8-pin connectors, enabling modular and coordinated operation.

## Research Question
How can we design a modular, reliable sprinkler system ?
What hardware and software strategies ensure self-healing, recovery, and transparency for the user?
How can our design scale to different types of users (basic homeowner, tech-enthusiast, or sustainability-focused)?

## Block Diagram
This block diagram illustrates the architecture of the smart water saver system, which is divided into four interconnected modules.

The diagram illustrates the signal flow beginning from the central Hub module (Raj), which initiates communication by requesting sensor data from the Sensor module (Isaiah). The Sensor module measures soil moisture and transmits the corresponding analog data back to the Hub module for processing. The Hub also includes a light sensor to monitor sunlight levels, enabling more intelligent watering decisions based on ambient light conditions. The Speaker module (Myles) receives control signals from the Hub, driven by inputs from the potentiometer and push button, and produces audio feedback using a simple digital on/off control signal. After processing both soil moisture and light data, the Hub sends a digital control signal to the Motor module (Liam), which employs an H-Bridge circuit to activate the water pump. While each module operates with independent power, all share a common ground to maintain signal integrity, and standardized 8-pin connectors are used to interconnect the subsystems. This closed-loop architecture ensures efficient, responsive, and automated watering behavior based on real-time soil and light conditions.

<img width="2500" height="1000" alt="Screenshot 2025-12-09 192403" src="https://github.com/user-attachments/assets/143575cb-6bbb-4c0b-bcd9-70fd9235a3b7" />

*Figure 1: Showing Block Diagram of All Interconnect Subsystems*


| Pin | From        | To        | Type              | Description              |
|-----|-------------|-----------|-------------------|--------------------------|
| 1   | Myles (RB0) | Raj (RC7) | 0V / 5V Digital   | Trigger Pin For Speaker |
| 2   | –           | –         | –                 | not used                |
| 3   | –           | –         | –                 | not used                |
| 4   | –           | –         | –                 | not used                |
| 5   | –           | –         | –                 | not used                |
| 6   | –           | –         | –                 | not used                |
| 7   | –           | –         | –                 | not used                |
| 8   | Ground      | Ground    | Ground            | Ground                  |

*Figure 2: Showing Pin Connector Table for Myles and Raj*

| Pin | From          | To            | Type            | Description         |
|-----|---------------|---------------|-----------------|---------------------|
| 1   | –             | –             | –               | not used            |
| 2   | Raj (RD5)     | Isaiah (RB4)  | 0V / 5V Digital | Data Ready Signal   |
| 3   | –             | –             | –               | not used            |
| 4   | Isaiah (RC4)  | Raj (RC0)     | 0V / 5V PWM Digital | Sending Data        |
| 5   | –             | –             | –               | not used            |
| 6   | –             | –             | –               | not used            |
| 7   | –             | –             | –               | not used            |
| 8   | Ground        | Ground        | Ground          | Shared Ground       |

*Figure 3: Showing Pin Connector Table for Isaiah and Raj*

| Pin | From        | To         | Type            | Description            |
|-----|-------------|------------|-----------------|------------------------|
| 1   | Liam (RD0)  | Raj (RD6)  | 0V / 5V Digital | Button Pushed Signal   |
| 2   | Raj (RD7)   | Liam (RD1) | 0V / 5V Digital | Signal To Motor        |
| 3   | –           | –          | –               | not used               |
| 4   | –           | –          | –               | not used               |
| 5   | –           | –          | –               | not used               |
| 6   | –           | –          | –               | not used               |
| 7   | –           | –          | –               | not used               |
| 8   | Ground      | Ground     | Ground          | Shared Ground          |

*Figure 4: Showing Pin Connector Table for Liam and Raj*
