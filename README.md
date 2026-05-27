# Dual-Band Microstrip Rectenna for Wi-Fi Energy Harvesting

This repository contains the physical manufacturing files, schematic documentation, and Bill of Materials (BOM) for a dual-band radio frequency (RF) energy harvesting rectenna. 

The system is designed to passively capture ambient electromagnetic radiation from 2.45 GHz and 5 GHz Wi-Fi bands infrastructures and convert it into a sustainable Direct Current (DC) reservoir for ultra-low-energy IoT devices. 

## ⚙️ Hardware Specifications
* **Target Frequencies:** 2.45 GHz and 5.80 GHz
* **Measured Efficiency:** Peak 30% RF-to-DC conversion efficiency at 0 dBm input power.
* **DC Yield:** 1.0V DC (2.45 GHz) and 0.2V DC (5.20 GHz)
* **Substrate:** Commercial FR-4
* **Rectifier Topology:** Voltage doubler utilizing the SMS7630-006LF series pair Schottky diodes.

## 📂 Repository Contents
* `/Gerber_Files`: Contains the standard RS-274X Gerber packages and NC Drill files ready for immediate foundry handoff (e.g., JLCPCB, PCBWay).
* `/BOM`: Bill of Materials (`.csv`) detailing all high-Q passives and RF components. 
* `/Schematics`: High-resolution PDF of the system architecture and matching network.

## 🛠️ Layout & Design Notes
* **Impedance Matching:** The physical layout features strictly controlled-impedance microstrip routing. 
* **Parasitic Mitigation:** Because the SMS7630-006LF is a series pair of diodes rather than a single unit, the physical footprint and trace routing were specifically engineered to account for the internal parasitic capacitance of the dual-diode structure.
* **Fabrication Toolchain:** The RF geometries were validated via co-simulation in Keysight ADS and CST Studio Suite before being routed for manufacturing execution.

## ⚠️ Hardware Tolerance Notice
During physical validation via Vector Network Analyzer (VNA), minor frequency shifts may be observed compared to the simulated $S_{11}$ data. This is an expected artifact of the variable dielectric constant (ϵ_r)) inherent to commercial FR-4 substrates and standard fabrication etching tolerances. The rectifier network is designed with sufficient bandwidth to absorb these variations and maintain DC yield.

---
*Designed and engineered by Hamza Amr and the BUC graduation project team.*
