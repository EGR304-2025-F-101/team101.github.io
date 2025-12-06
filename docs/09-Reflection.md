---
title: Reflection
---

# Reflection

## Lessons Learned  

1. **Lesson 1:** We learned that defining user needs early and grounding those needs in real research—such as Amazon reviews, benchmarking, and project requirements—kept our design focused on solving real problems like water waste, installation difficulty, and reliability.
2. **Lesson 2:** We discovered that having a modular system architecture with four separate subsystems made debugging much easier, because isolating issues in the Sensor, Motor, Speaker, or Control module helped us quickly narrow down hardware faults and communication problems.
3. **Lesson 3:** From our design review, we learned that clear documentation and justification of decisions are just as important as the hardware itself, since reviewers rely on our clarity to understand why the design is structured the way it is.
4. **Lesson 4:** We realized the importance of consistent team communication, especially because each subsystem was built by a different team member and required coordination through shared connectors, shared ground, and timing of signals.
5. **Lesson 5:** We learned that early testing of sensors—especially the soil moisture sensor and light sensor—was crucial because raw analog values often behaved differently than expected and required smoothing, calibration, and interpretation.
6. **Lesson 6:** We discovered that power distribution and grounding across multiple boards requires careful planning, as independent power supplies can only function correctly when a stable common ground is maintained across all subsystems.
7. **Lesson 7:** We learned the value of iterative improvement, because every time we refined a subsystem—such as adjusting the H-Bridge motor circuit, tuning speaker outputs, or reorganizing the block diagram—the overall system became more reliable and aligned with our product goals.
8. **Lesson 8:** Through building and testing, we learned how real-world hardware limitations like noise, connection instability, and outdoor environmental expectations shape the final design more than theoretical ideas do.
9. **Lesson 9:** We learned how important strong version control and organized documentation are, especially when handling multiple codebases, multiple boards, and separate subsystem responsibilities across the team.
10. **Lesson 10:** Most importantly, we gained experience designing a complete embedded system—from brainstorming and requirements gathering to modular hardware, communication protocols, and final integration—which strengthened our engineering judgment and teamwork skills moving forward.

## Recommendations for Future Students  

1. **Recommendation 1:** Learn how to break a project into modular subsystems early, because having defined roles and clear interfaces between boards will save a huge amount of time during debugging and integration.
2. **Recommendation 2:** Get comfortable with basic microcontroller skills—ADC reading, digital I/O, PWM, interrupts, and simple communication—because nearly every part of this class depends on applying those fundamentals quickly.
3. **Recommendation 3:** Start documentation from day one and keep everything organized, since writing things clearly as you go makes design reviews, status reports, and final deliverables far less stressful.
4. **Recommendation 4:** Communicate with your team consistently and check alignment often, because even small misunderstandings about connectors, pinouts, or power setups can cause major delays later in the project.
5. **Recommendation 5:** Adopt a mindset of testing early and iterating often, because hardware rarely works perfectly on the first try and steady, small improvements will make the final system far more reliable.
