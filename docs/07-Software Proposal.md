---
title: Software Proposal
---

## Introduction

This system comprises four subsystems: Main Hub, Sensor Board, Motor Board (sprinkler actuator), and Speaker Board. The Main Hub periodically requests soil‑moisture data from the Sensor Board. After receiving the reading, it compares it against a user-set threshold from the potentiometer. If the soil is drier than the threshold (i.e., needs to be more moist), the Main Hub commands the Motor Board to run the sprinkler for the programmed duration and simultaneously signals the Speaker Board to announce the status. This poll–compare–act loop repeats to maintain the desired soil moisture.


![Activity Diagram](https://raw.githubusercontent.com/EGR304-2025-F-101/team101.github.io/refs/heads/main/docs/image/software-proposal-img.png)


