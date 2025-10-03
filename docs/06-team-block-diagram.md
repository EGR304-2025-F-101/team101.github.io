---
title: Team Block Diagram
---

# Block Diagram, Process Diagram, and Message Structure

## Introduction
Our team is developing a smart sprinkler controller designed for reliability, adaptability, and user transparency. The system builds on collaborative design ideation, where we clustered features into requirements like unshakable WiFi stability, graceful offline functionality, and seamless sensor integration. This block diagram shows how the boards communicate through a central hub using an 8-pin ribbon cable to manage connectivity, control, and data.

## Research Question
- How can we design a modular, reliable sprinkler system that functions both online and offline?
- What hardware and software strategies ensure self-healing, recovery, and transparency for the user?
- How can our design scale to different types of users (basic homeowner, tech-enthusiast, or sustainability-focused)?

## Block Diagram
The team block diagram illustrates the high-level architecture of our smart sprinkler controller. It uses a daisy-chain topology (as discussed in our team meeting) with three PIC18F57Q43 Curiosity Nano microcontroller boards: one for sensors (Isaiah), one for central processing and WiFi (Raj), and one for actuators (Liam). Interconnections are via 8-pin ribbon cables, with pins 1-7 mapped for shared communications (e.g., I2C for data exchange) and pin 8 reserved for ground. This minimizes interconnections while allowing modular expansion for additional zones or sensors.

### Key Features
- **Sensor Board (Isaiah):** Interfaces with soil moisture, rain, and temperature sensors to provide hyper-local data for weather skips and saturation detection.
- **Central Controller Board (Raj):** Handles scheduling, WiFi connectivity for cloud integration, offline storage (e.g., 30-day schedules), and user feedback via LEDs/buttons.
- **Actuator Board (Liam):** Controls zone valves and pump relays based on commands from the central board, supporting fault detection and modular scalability.

Each board meets minimum requirements with at least one sensor or actuator, and risks are de-risked by distributing functions (e.g., central fallback to offline mode if sensors fail).

![Block Diagram](path/to/block_diagram.png)  
*Note: Replace `path/to/block_diagram.png` with the actual path to your exported PNG.*

## Process Diagram
The process diagram outlines the system's operational flow, from data collection to watering execution. It ensures graceful offline functionality (e.g., using stored schedules during outages) and intelligent self-healing (e.g., auto-reconnect after power loss). We used a flowchart to visualize this, focusing on decision points for weather adjustments, sensor integration, and user overrides.

## Results
1. Identified 7 core requirement clusters from brainstorming.
2. Developed 3 product concepts, each targeting a different type of user.
3. Designed a modular block diagram architecture to support flexible expansion.

## Conclusions and Future Work
Our smart sprinkler system balances reliability, transparency, and sustainability. Next steps include refining hardware prototypes, testing offline resilience, and validating weather-based watering adjustments. Future iterations will focus on expanding integration with external sensors and refining the user app experience.

## External Links
- [ASU IdeaLab](https://idealab.asu.edu)

## References
*(Insert references from technical articles, standards, or course readings here.)*

