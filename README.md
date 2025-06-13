# SAR Satellite Mission Design

Designing a Synthetic Aperture Radar (SAR) satellite mission involves many technical layers and trade-offs. Whether you’re building your first mission or refining a complex one, understanding the key components and their interplay is crucial. This repository contains a practical guide and resources based on real satellite mission design experience, including a sample SAR mission designed to detect drones.

---

## Guide Overview

### 1. General Requirements for Any Satellite Mission

Before diving into SAR specifics, every satellite mission requires a solid foundation covering:

| Subsystem                     | What’s Needed / Considered                           |
|------------------------------|-----------------------------------------------------|
| Payload                      | Define primary sensor(s), resolution, spectral range|
| Platform (Bus)               | Power, thermal control, attitude control, structure|
| Onboard Data Handling (OBDH) | Telemetry, software safety, data storage, processing|
| Telemetry, Tracking & Control (TTC) | Communications, encryption, command handling      |
| Power System                 | Solar arrays, batteries, power distribution          |
| Thermal Control              | Passive/active cooling, operating temperature ranges |
| Mechanical & Structural      | Mass budget, mounting, vibration tolerance           |
| Attitude Determination & Control (ADCS) | Stability, pointing accuracy, jitter limits      |
| Software                    | Fault detection, safe modes, uplink software updates  |

---

### 2. SAR Satellite Specific Considerations

SAR satellites have unique payload and system requirements due to radar’s nature:

| Parameter           | Typical Values / Considerations                      |
|---------------------|-----------------------------------------------------|
| Frequency Band      | X-band (8-12 GHz), C-band, or L-band depending on resolution/penetration |
| Spatial Resolution  | ~1m for high-res, up to 30m for wide-area surveillance|
| Swath Width         | 10 - 100 km depending on beamforming and orbit altitude|
| Payload Power       | High power needed (hundreds of Watts) for radar transmitters|
| Data Rate           | High data volumes, requiring fast onboard storage and downlink|
| Thermal Management  | Heat dissipation for high power radar electronics    |
| Attitude Control    | Precise pointing and stable orbit for coherent SAR imaging|
| Onboard Processing  | Image formation, data compression                     |

---

### 3. Example Mission: SAR Satellite for Drone Detection

**Mission Objective:**  
Detect and track unauthorized drones over urban areas using high-resolution SAR imaging.

| Subsystem           | Selected Option / Specification                    | Justification                           |
|---------------------|---------------------------------------------------|---------------------------------------|
| Payload Frequency    | X-band SAR (9.6 GHz)                              | High resolution for small target detection |
| Spatial Resolution   | 0.5 m                                             | To resolve small drone structures      |
| Swath Width         | 20 km                                             | Balance between coverage and resolution|
| Orbit               | Sun-synchronous, 500 km altitude                  | Consistent lighting, revisit time suitable for monitoring |
| Data Handling       | Onboard image processing & compression             | Reduce data volume before downlink     |
| Communication       | X-band downlink with encryption                     | Secure transmission of sensitive data |
| Power System        | Solar arrays capable of 1 kW output, Lithium-ion batteries | Support high power radar transmitter   |
| Thermal Control     | Active cooling via heat pipes and radiators         | Maintain radar electronics within operational limits |
| ADCS                | High precision reaction wheels & star trackers     | Required for accurate SAR imaging      |
| OBDH Software       | Safety mode, uplink command validation, fault recovery | Ensure mission reliability and remote updates |

---

## PDF Documentation

For a comprehensive overview, detailed explanations, and full design considerations, please refer to the PDF document:

**[SAR Mission Design Guide PDF](./SAR_Mission_Design.pdf)**

---

## Naming of Sketch and Design Files

Below are some key design sketches and info images related to the SAR mission:

| File Name                        | Description                                   |
|---------------------------------|-----------------------------------------------|
| SAR_Mission_Design_Sketch_2.png | Second version of the SAR mission concept sketch |
| design.png                      | General SAR satellite design overview          |
| SAR info.png                   | Infographic with SAR mission technical details |
| SAR_Mission_Design_Sketch.png  | Initial SAR mission design sketch               |

---

## Suggestions & Feedback

Your thoughts and ideas are valuable! If you have any suggestions, questions, or improvements related to SAR mission design or this repository, please feel free to share them here or submit a pull request. Together, we can make this resource even better for everyone interested in SAR satellite missions.

---

*Created by Meirah Alzyoudi*
