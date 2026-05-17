# COWGIRLS: Smart Farm Solution for Rural-Urban Synergy

![Event](https://img.shields.io/badge/Event-2026_Asian_Hackathon_for_Green_Future-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-Apache_2.0-blue?style=for-the-badge)

**Wind-Customized Ammonia Scrubbing for Sustainable Urban Air Quality.**

---

## 🌿 Project Overview

Large-scale rural livestock farms contribute significantly to urban fine dust (PM2.5) via ammonia emissions. However, these farms often lack the financial incentive to operate mitigation hardware due to high chemical costs.

**COWGIRLS** provides an integrated Hardware + Software solution that uses real-time weather data and a specialized livestock ammonia estimation algorithm. By only activating fence-based scrubbers when wind paths target urban areas, we reduce chemical waste by up to **70%**, convert harmful gas into solid fertilizer, and secure government eco-subsidies for farmers.

## ✨ Core Features

1.  **Dynamic Ammonia Calculation (JAES Formula)**: Real-time estimation of livestock ammonia production using empirical formulas (JAES, 2022).
2.  **Smart Valve & Direction Control**: Automated activation of directional fence zones (East, West, South, North) based on real-time wind azimuth (0-360°).
3.  **Eco-Subsidy Data Logging**: Visualized reports tracking operation minutes and chemical savings to assist farmers in applying for government subsidies.
4.  **Chemical Transformation**: Converts airborne ammonia into solid ammonium salt fertilizer, promoting resource recycling rather than simple odor masking.

## 🛠 Tech Stack

### Software
- **Mobile Frontend**: Native Android (Dashboard & Monitoring)
- **Web Frontend**: React + Vite + Tailwind CSS (Project Showcase)
- **Backend Server**: FastAPI (Python)
- **Database**: Farm Static Data & OpenWeatherMap API Integration

### Hardware & IoT
- **MCU**: ESP32 MCU Board
- **Protocol**: HTTPS REST API & MQTT
- **Actuators**: 4-Channel MOSFET Module, 5V DC Submersible Pumps, Fine Mist Nozzle Kits

## 🏗 System Architecture

The system adopts a **4-Layer Automated Control Architecture**:

1.  **Data Layer**: Collects real-time wind speed, direction, and temperature from OpenWeatherMap & local sensors.
2.  **Control Layer**: Backend processes data through the JAES formula and determines target blocking sectors.
3.  **Edge Layer**: ESP32 receives MQTT control packets (PWM: 0–255) for precision pressure scaling.
4.  **Actuator Layer**: MOSFET module triggers specific pumps and nozzles to neutralize urban-bound gas.

## 👥 The Team: COWGIRLS

| Member | Role | Major |
| :--- | :--- | :--- |
| **Yoojin Jang** | Product Manager | Food Science |
| **Arim Lee** | Lead Developer | Computer Science |

---

## 📖 References
- Park, S., et al. (2022). A study on ammonia emissions from weaned pig house. *Journal of Animal Environmental Science*.
- MAFRA (2024). *Guidelines for Livestock Odor Mitigation Project*.
- RDA (2019). *Reduction measures for fine dust and ammonia in agricultural sectors*.

---
Developed with ❤️ for the 2026 Asian Hackathon for Green Future.
