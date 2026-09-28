# SAMUDRA-SCAN 🌊

### Low-Cost Deployable Seafloor Metal Anomaly Detection & Mapping System

SAMUDRA-SCAN is a 3D web-based simulation concept for a low-cost deployable seafloor sensor pod designed for early-stage ocean mineral-resource reconnaissance.

The project is aligned with **Smart India Hackathon Problem Statement 26064**:

> **Low-Cost Deployable Seafloor Metal Detection Sensor for Ocean Resource Exploration**

**Organization:** Ministry of Earth Sciences (MoES)  
**Department:** National Centre for Polar and Ocean Research (NCPOR)  
**Category:** Hardware  
**Theme:** Robotics and Drones

---

## 🌐 Live Demo

🚀 **[Launch SAMUDRA-SCAN 3D Live Demo](https://p3v-cyborg.github.io/samudra-scan-sim/)**

Explore the interactive 3D seafloor simulation, including:

- 🌊 3D underwater environment
- 🤖 SAMUDRA-SCAN sensor pod
- 📡 EM & magnetic sensing simulation
- 🎯 Anomaly detection
- 🔄 Adaptive rescanning
- 🗺️ Seafloor anomaly mapping
- 📊 Live sensor dashboard
- 📋 Mission report

> **Note:** This is a simulation/concept prototype. Sensor values and anomaly scores are simulated and are not real field measurements.

## 🚀 Project Idea

Existing deep-ocean exploration systems can involve expensive AUVs, ROVs, sonar systems and specialized research vessels.

SAMUDRA-SCAN proposes a different approach:

**Deploy → Detect → Locate → Rescan → Verify → Map**

A compact sensor pod is envisioned to be deployed from a research vessel and used to identify **geophysical anomalies associated with metal-rich seabed deposits**.

The system is intended as a reconnaissance tool. It does **not** claim to directly measure nickel, cobalt, copper or other metal grades.

---

## 🎯 Objectives

- Develop a low-cost deployable seafloor sensing concept.
- Combine multiple sensor measurements instead of relying on a single signal.
- Detect and locate potential seabed anomalies.
- Perform adaptive high-density rescanning around detected anomalies.
- Use visual/sonar verification only when required.
- Generate a georeferenced anomaly map.
- Prioritize locations for further investigation and physical sampling.

---

## 🧠 Core Concept

The proposed sensor-fusion architecture can combine:

- Electromagnetic/electric-field sensing
- 3-axis magnetometer
- Pressure/depth sensor
- IMU
- Temperature/salinity measurements
- Seabed-altitude sensing
- Optional camera/sonar
- Embedded controller
- Local data storage

The measurements can be converted into an **anomaly score** rather than presenting unsupported claims about exact mineral concentration.

### Example

```text
EM response        ──────── HIGH
Magnetic response  ──────   MEDIUM
Depth               ─────── 5200 m
Seabed altitude     ─────── 1 m

              ↓

        ANOMALY SCORE: 82

              ↓

        HIGH PRIORITY
          FOR RESCAN
```

---

## 🗺️ Adaptive Survey

Instead of performing a dense survey everywhere, the simulation demonstrates:

```text
                COARSE SURVEY
                      │
                      ▼
                ANOMALY FOUND
                      │
                      ▼
                LOCAL RESCAN
                      │
                      ▼
                 VERIFY
                      │
                      ▼
                 MAP TARGET
```

This is intended to reduce unnecessary high-resolution survey effort and focus measurements on potentially interesting areas.

---

## 🖥️ 3D Simulation

The repository includes a browser-based Three.js simulation.

The simulation contains:

- Research vessel
- Deployment environment
- Seafloor terrain
- Polymetallic-nodule-like seabed objects
- SAMUDRA-SCAN sensor pod
- Underwater particles
- Survey trajectory
- Anomaly heatmap
- Adaptive rescan zones
- Sensor telemetry dashboard
- Mission phases
- Mission report
- Camera controls

### Mission phases

1. **Descent**
2. **Coarse Survey**
3. **Detect + Locate**
4. **Adaptive Rescan**
5. **Camera Verify**
6. **Recovery**
7. **Mapping / Mission Report**

---

## 📊 Dashboard

The simulation dashboard displays:

- Current phase
- Estimated depth
- EM response
- Magnetic response
- Anomaly score
- Number of rescans
- Area covered
- Samples logged
- Low/Medium/High classifier
- Live sensor-response graph
- Mission progress
- Survey targets

The interface also provides:

- Restart
- Pause / Resume
- Simulation speed
- Camera mode
- Mission report
- "Why SAMUDRA-SCAN" comparison

---

## 🧪 Simulation Disclaimer

**This repository contains a simulation/concept prototype.**

The sensor values, anomaly scores and mineral distribution shown by the simulation are generated data and are **not field measurements**.

The simulation does not establish:

- Actual nickel concentration
- Actual cobalt concentration
- Actual copper concentration
- Exact mineral grade
- Commercial viability
- Real-world detection range

Real deployment would require laboratory calibration, pressure-rated underwater hardware, controlled experiments and validation using known seabed samples.

---

## 🏗️ Technology Stack

### Frontend / Simulation

- HTML5
- CSS3
- JavaScript
- Three.js
- WebGL

### Simulation components

- 3D scene rendering
- Procedural seabed
- Procedural anomaly field
- Sensor simulation
- Sensor-fusion scoring
- Adaptive path generation
- Heatmap generation
- Interactive camera
- Mission-state machine

The current prototype loads Three.js from a CDN, so an internet connection may be required when opening the HTML file unless the library is later bundled locally.

---

## 🎮 Controls

### Mouse

- **Drag:** Rotate the camera
- **Scroll:** Zoom
- **Touch:** Pinch to zoom

### Dashboard

- **Restart:** Restart the mission
- **Pause:** Pause/resume simulation
- **Speed:** 1× / 2× / 4×
- **Camera:** Free orbit / Follow pod / Top-down map
- **Why it wins:** Shows the concept comparison
- **Mission report:** Displays detected targets and simulated survey results

---

## 🔬 Proposed Real-World Hardware Architecture

The simulation represents a future hardware implementation.

```text
                 RESEARCH VESSEL
                       │
                 Deployment cable
                       │
                       ▼
              ┌─────────────────┐
              │  SENSOR POD     │
              │                 │
              │ EM Sensor       │
              │ Magnetometer    │
              │ IMU             │
              │ Pressure        │
              │ Temperature     │
              │ Seabed Sensor   │
              │ MCU             │
              │ SD Storage      │
              └────────┬────────┘
                       │
                       ▼
                    SEAFLOOR
             ○    ●     ○     ●
                ●    ○
```

---

## 💡 Proposed Innovation

SAMUDRA-SCAN focuses on combining several concepts into a single low-cost reconnaissance workflow:

### 1. Multi-sensor fusion

EM/electric, magnetic and environmental measurements can be combined to improve anomaly characterization.

### 2. Adaptive scanning

When an anomaly crosses a threshold, the system can perform a denser local survey.

### 3. Anomaly scoring

Instead of simply displaying "metal detected", the system produces a relative anomaly score.

### 4. Targeted verification

Camera/sonar verification can be triggered around selected anomalies instead of continuously operating at maximum resolution.

### 5. Seafloor anomaly mapping

Survey tracks and detected targets can be visualized on a spatial map.

### 6. Low-cost deployment concept

The proposed architecture is intended to complement expensive deep-ocean exploration platforms by providing a smaller reconnaissance-oriented sensing system.

---

## ⚠️ Engineering Challenges

A real deep-ocean version would need to address:

- Very high hydrostatic pressure
- Waterproof pressure housing
- Corrosion
- Seawater conductivity
- Electromagnetic interference
- Sensor calibration
- Precise underwater positioning
- Tether management
- Temperature effects
- Long-duration power
- Data storage
- Communication at depth
- Seabed contact/altitude control
- Recovery reliability

At approximately 5,000 m depth, pressure is roughly 500 bar, making the pressure housing one of the major hardware challenges.

---

## 📚 References

1. **National Institute of Ocean Technology (NIOT)** — Deep Sea Mining Technology  
   https://www.niot.res.in/niot_dsmtech_en.php

2. **Ministry of Earth Sciences (MoES)** — Deep Ocean Mission  
   https://www.moes.gov.in/

3. Szitkar, F. et al. (2021), research on deep-sea electric and magnetic surveys for hydrothermal/seafloor mineral exploration, *Journal of Geophysical Research: Solid Earth*.  
   https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2021JB022082

4. Gehrmann, M. et al. (2019), research on marine mineral exploration using controlled-source electromagnetics, *Geophysical Research Letters*.  
   https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2019GL082928

5. Research on marine self-potential measurements using an autonomous underwater vehicle, *Geophysical Journal International*.  
   https://academic.oup.com/gji/article/215/1/49/5047310

6. Research on joint interpretation of marine self-potential and transient electromagnetic surveys for seafloor massive sulphide deposits.  
   https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2022JB024496

---

## 🤝 Future Development

Possible next stages include:

- Real EM sensor integration
- Real magnetometer integration
- Pressure-rated electronics enclosure
- Underwater positioning
- Real-time surface dashboard
- Hardware-in-the-loop simulation
- Autonomous navigation
- Real seabed dataset integration
- Machine-learning anomaly classification
- Physical prototype testing
- Laboratory validation using known metal/mineral samples

---

## 👥 Project

**Project:** SAMUDRA-SCAN  
**Problem Statement:** 26064  
**Theme:** Robotics and Drones  
**Organization:** Ministry of Earth Sciences  
**Department:** National Centre for Polar and Ocean Research

---

## ⭐ Concept Summary

> **SAMUDRA-SCAN aims to provide a low-cost, deployable reconnaissance platform that detects, localizes, rescans and maps geophysical anomalies associated with metal-rich seafloor deposits, helping researchers identify locations for further detailed investigation.**

**Detect → Locate → Rescan → Verify → Map**
