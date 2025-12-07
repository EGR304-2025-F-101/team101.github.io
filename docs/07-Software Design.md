---
title: Software Design
---

## Introduction

The system operates using a hub-and-spoke architecture designed to automate garden irrigation based on environmental conditions. The main hub continuously monitors sunlight intensity using an LDR sensor. When the light level falls below a defined threshold—indicating that it's an appropriate time to water, as evaporation will be minimal—the hub requests soil moisture data from the sensor board. The sensor board reads data from the soil moisture sensor, processes it, and sends the moisture percentage back to the hub. The hub then compares this value with a predefined moisture threshold. If the soil is sufficiently moist, the system waits and repeats the monitoring cycle. However, if the soil moisture is below the required level, the hub activates both the speaker subsystem and the sprinkler (motor) subsystem. The speaker emits a short beep to signal that watering has started, while the sprinkler runs for a fixed duration of 15 minutes, ensuring the soil receives adequate water. After watering, the system resets and resumes its continuous monitoring cycle, creating a fully automated and energy-efficient irrigation loop.

![Activity Diagram](https://github.com/EGR304-2025-F-101/team101.github.io/blob/main/docs/image/software-proposal.drawio%20.png?raw=true)

[Click here to download the XML file](https://github.com/EGR304-2025-F-101/team101.github.io/blob/main/docs/image/software-proposal.drawio.xml)


