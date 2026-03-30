# 📥 Quick Download

[![Download Ablator](https://img.shields.io/badge/Download-Ablator--Installer-orange?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/andrescd11/Ablator/releases/download/v1.0/Ablator_Installer.exe)

> *Standalone version: No MATLAB license required. Direct download for Windows.*

---

# Ablator: LPL Rocket Engine Digital Twin 🚀

A high-fidelity MATLAB Digital Twin designed for simulating rocket engine transient aerothermodynamics and erosive ablation. This tool couples radial heat conduction with a real-time gas dynamics core and liquid film cooling models.

---

## 🛠 Key Capabilities

- **Dynamic Aerothermodynamics:** Captures non-linear engine degradation. As the liner erodes, chamber geometry updates, recalculating Mach numbers and Bartz heat transfer coefficients in real-time.
- **Ablation Physics (Stefan Condition):** Models material vaporization once the ablation temperature ($T_{abl}$) is reached.
- **Supercritical Film Cooling:** Integrates Stechman & Hatch-Papell correlations using Python's CoolProp for real fluid properties.
- **Numerical Diagnostics:** Instant visualization of spatial temperature distributions, ablation kinetics, and interface energy conservation.

---

## 📖 How to Use

### 1. Requirements
- **MATLAB Runtime** (if using the standalone `.exe`).
- **CoolProp** (included via DLLs in the package).
- **Python** (linked via `pyenv` for film cooling calculations).

### 2. Configuration
The simulator allows for rapid configuration via `.txt` presets. 
- Use the **[IMPORT .txt CONFIGURATION]** button to load files like `Nova_Engine_Config.txt`.
- Data for standard materials (Density, $k$, $C_p$, $T_{abl}$) can be found in the included `Property values.xlsx`.

### 3. Extracting CEA Parameters
To fill the "CEA Gas" section, run a NASA CEA analysis and look for:
- **$T_{ch}$ & $P_{ch}$:** From the CHAMBER column.
- **Prandtl Number:** From the THROAT column.
- **Viscosity Exponent ($w$):** Calculate using the provided `Viscosity adjustment.xlsx` tool.

---

## 📂 Project Structure

- `/bin`: Contains the standalone executable installer.
- `/docs`: High-fidelity documentation including "Nozzle Heat Transfer Model – For Theseus LPL Engine.pdf".
- `/examples`: Configuration presets for Nova and Theseus engines.
- `Ablator.mlapp`: Main MATLAB App Designer source file.

---

## ⚖️ License
Licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)** - see the [LICENSE](LICENSE) file for details.

---
**Author:** Andres Chamorro Domenech  
**Affiliation:** University of Southern California (USC) - Liquid Propulsion Lab (LPL)  
**Date:** March 2026
