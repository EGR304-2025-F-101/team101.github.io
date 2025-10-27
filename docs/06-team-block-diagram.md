---
title: Team Block Diagram
---
## Introduction
The system consists of three interconnected subsystems—Control, Sensor, and Motor—each built using the PIC18F57Q43 Curiosity Nano. The Control unit processes sensor inputs and sends commands to the motor subsystem through 8-pin connectors, enabling modular and coordinated operation.

## Research Question
How can we design a modular, reliable sprinkler system that functions both online and offline?
What hardware and software strategies ensure self-healing, recovery, and transparency for the user?
How can our design scale to different types of users (basic homeowner, tech-enthusiast, or sustainability-focused)?

## Block Diagram
This block diagram illustrates the architecture of the smart water saver system, which is divided into three interconnected modules.

The diagram shows the signal flow starting from the Sensor module (Isaiah), which measures soil moisture and sends analog data to the central Control module (Ragul Raj). The Speaker module (Myles) will recive control signals from the Control Module(Ragul Raj), speciffically the button and potentiometer and generate audio feedback through a PWM driven circuit. The Control unit processes this information and sends a digital signal to the Motor module (Liam), which uses an H-Bridge circuit to activate the water pump. While independently powered, all modules share a common ground for signal integrity, and standardized 8-pin connectors link the subsystems. This closed-loop design ensures efficient and automated watering.  


<img width="2729" height="1028" alt="team-block-diagram-hub drawio" src="https://github.com/user-attachments/assets/ed30117f-d3ea-4303-bd23-efbd9e282cd0" />


