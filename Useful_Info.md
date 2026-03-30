<div align="center">

# 🚀 ABLATOR: HIGH-FIDELITY ROCKET ENGINE DIGITAL TWIN
### *Nozzle Heat Transfer & Erosive Ablation Transient Simulator*

[![Version](https://img.shields.io/badge/Version-1.0.0--Stable-blue?style=for-the-badge)](https://github.com/andrescd11/Ablator/releases)
[![License](https://img.shields.io/badge/License-AGPL--3.0-orange?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows)](https://github.com/andrescd11/Ablator/releases)

---

[📥 **DOWNLOAD STANDALONE INSTALLER (.exe)**](https://github.com/andrescd11/Ablator/releases/download/v1.0/Ablator_Installer.exe)
*True Standalone: No MATLAB or Python installation required.*

---
</div>

## 📝 1. Executive Summary
**Ablator** is a specialized Digital Twin developed to simulate the non-linear thermal degradation of rocket engine liners. Unlike static thermal models, Ablator couples a **1D radial heat conduction solver** with a **real-time core gas aerodynamics engine**.

The software predicts **"Erosive Ablation"**—the material loss occurring when the liner's surface reaches its phase-change temperature ($T_{abl}$). This provides critical data for:
* Engine life-cycle analysis.
* Throat erosion rates.
* Thermal structural integrity for LPL’s liquid rocket programs (**Nova** & **Theseus**).

---

## 📂 2. Comprehensive Directory Inventory
This package is structured to provide both the execution environment and the theoretical foundation of the project:

| Folder/File | Description |
| :--- | :--- |
| 📦 **Ablator_Installer.exe** | **Standalone Windows binary.** Runs on any PC without MATLAB/Python licenses. |
| 📂 **Docs/** | **Technical & Physics Models.** Includes NASA-CEA raw data, Theseus nozzle derivations, and the core manual for the Stefan Condition. |
| 📂 **Input Examples/** | **Simulation Presets.** Validated `.txt` configurations for the **Nova Engine** and generic templates. |
| 📂 **Resources/** | **Engineering Support.** Excel databases for material properties ($k$, $C_p$) and viscosity exponent ($w$) adjustment tools. |

---

## 🔬 3. Scientific & Mathematical Basis

### 3.1 Gas Dynamics & Convection
Utilizes the **Bartz Correlation** to calculate the convective heat transfer coefficient ($h_g$) as a function of the local Mach number and stagnation conditions.

### 3.2 1D Radial Heat Conduction
A transient solver calculating temperature gradients through multiple liner layers, accounting for variable thermal properties ($k$, $C_p$) as a function of temperature.

### 3.3 Ablation Logic (The Stefan Condition)
Real-time thickness reduction based on the **latent heat of vaporization** once the wall temperature matches the material's $T_{abl}$.

### 3.4 Integrated Thermodynamics (CoolProp)
The **Film Cooling** module is powered by integrated **CoolProp binary libraries (.dll)**. It retrieves real-fluid properties (Enthalpy, Density, Viscosity) at supercritical pressures without requiring external environments.

---

## 🛠️ 4. Installation & Setup Guide

### 4.1 Requirements
* **OS:** Windows 10/11 (64-bit).
* **RAM:** 8GB Minimum recommended.
* **Note:** No external software (MATLAB or Python) is required.

### 4.2 Process
1.  Run `Ablator_Installer.exe`.
2.  The installer will verify the **MATLAB Runtime R2024b**. If missing, it will download and install it automatically (free of charge).
3.  Launch **Ablator** from your Start Menu.

---

## 🚀 5. Operational Workflow

1.  **Import Data:** Click `IMPORT .txt CONFIGURATION` and select `Nova_Engine_Config.txt`.
2.  **CEA Inputs:** Enter $P_c$, $A_t$, and $T_c$. Use the Viscosity Excel in `/Resources` to find the specific $w$ exponent.
3.  **Liner Materials:** Set thickness and properties. Refer to `Property values.xlsx` for accurate data.
4.  **Active Cooling:** Toggle `Film Cooling`, select your coolant (RP-1, Water, etc.), and set the mass flow.
5.  **Execution:** Hit `START SIMULATION`. Export your results for technical reports using the `Export Results` button.

---

## ❓ 6. Troubleshooting & FAQ

> **Q: Do I need to install Python for the Film Cooling to work?**
> **A:** No. All thermodynamic libraries are pre-compiled and included in the installer.

> **Q: The simulation crashes immediately after clicking Start.**
> **A:** Check your inputs. Ensure no thickness or density values are set to 0.

---

<div align="center">

**Andres Chamorro Domenech**
*Aerospace Research Engineer – LPL*
*University of Southern California*
