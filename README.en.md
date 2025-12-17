# tensile-testing-machine-astm-d638
Open-hardware tensile testing machine for plastics (ASTM D638).  
Project by Diego Víctor Saavedra Ravier.

# Tensile Testing Machine for Plastics (ASTM D638)

[![License: CERN-OHL-S v2](https://img.shields.io/badge/License-CERN--OHL--S%20v2-blue.svg)](LICENSE_CERN_OHL_S)

Universal Testing Machine (UTM) for **plastics**, primarily focused on parts manufactured by
**Additive Manufacturing (3D printing)**, and designed to comply with the requirements of
the **ASTM D638** standard, ensuring valid and comparable tensile test results with other
machines operating under the same standard.

**Final Degree Project in Electromechanical Engineering** – UTN FR Chubut.

> Academic title: **Tensile testing machine for plastics**  
> *Design and calculation according to ASTM D638*

> Author: **Diego Víctor Saavedra Ravier**

> Year: **2025**

> Licenses: **CC BY-SA 4.0** (documentation) and **CERN-OHL-S v2** (hardware)

> Complete project documentation ➠  
> [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17923969.svg)](https://doi.org/10.5281/zenodo.17945725)

---

## 📸 General view of the machine

<p align="center">
  <img src="hardware/img/vista%20con%20cubres.jpg" alt="Plastic Tensile Testing Machine - Front render" width="480">
</p>

---

## 🧩 General description

This project presents the **design and mechanical calculation** of a tensile testing machine
for plastics, with particular emphasis on materials used in **Additive Manufacturing**
(FFF/FDM, SLA, SLS, etc.).

The machine is intended to be:

- **Affordable and low-cost**
- **Replicable** using locally available resources
- **Fully documented and open** for the academic and maker communities

The design complies with the main requirements of **ASTM D638** (the standard used for tensile
testing of plastics) for “dog-bone” specimens, with special focus on:

- Limiting machine compliance (structural deformation)
- Proper selection of load cell, transmission system, structure, grips and accessories
- The possibility of integrating an extensometric system based on
  **Digital Image Correlation (DIC)**

At its current stage, the project covers the complete mechanical design, calculations,
proposed electronics and control system, technical drawings, bill of materials (BOM),
and manufacturing cost estimation.  
**The physical prototype has not yet been manufactured.**

---

## 🔧 Main features

- **Reference standard:** **ASTM D638** (plastic tensile testing)
- **Target testing capacity:** up to **10 kN**
  (dimensioned to cover most polymers used in 3D printing)
- **Machine stiffness:** **25.4 [kN/mm]**
  (to comply with requirement 5.1.6 of the standard)
- **Machine weight:** **75 kg**
- **Specimens:** **Type I, II, III, IV and V**
- **Maximum crosshead speed:** **100 mm/min**
- **Application fields:**
  - University and research laboratories
  - Workshops and small enterprises using additive manufacturing
  - Plastics industry
- **Structural design:**
  - Frame built from structural steel tubing
  - Upper moving crosshead
  - Power transmission using trapezoidal lead screws (TR20x4) and a reduction gearbox with
    synchronous pulleys and belts (XL-L profile)
  - Wedge-type grips with lever and spring mechanism
  - Extensive use of FEA on critical components to ensure a safety factor
    **greater than 2** at maximum machine capacity
- **3D-printed components:**
  - Two-stage reduction gearbox with synchronous pulleys and belts
    (i = 8.16, T = 11 Nm)
  - Auxiliary and support parts
- **Proposed extensometric system:**
  - **DIC** using Raspberry Pi + 108 MP Arducam camera
  - Open-source software alternatives for image processing

---

### 🔄 Project status

- ✅ Design and documentation completed
- ⚙️ Awaiting someone brave enough to build the first prototype
- 📈 Open to improvements and community contributions

---

### 🎯 Project objectives

- ⚙️ Manufacturing of the first physical prototype
- ⚙️ Community feedback regarding improvements or design reviews
- ⚙️ Development of machine variants for other types of tests, such as
  **flexural**, **compression**, or even tensile testing of wood according to
  **ASTM D143**
- 📈 Community feedback on improvements to the **reduction gearbox**, aiming to
  increase output torque or implement a third stage to exceed 30 Nm
  (see Section 5.2.1 of the report ➠
  [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17923969.svg)](https://doi.org/10.5281/zenodo.17945725))
- 🔌 Potential development of dedicated software and control integration for the machine
- 💡 Development of a tensile testing methodology without using a physical extensometer
  (see Section 6.8 of the report ➠
  [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17923969.svg)](https://doi.org/10.5281/zenodo.17945725))

---

## 📂 Repository structure

> Note: This section describes the file structure of the project.

```text
tensile-testing-machine-astm-d638/
│
├── hardware/                    # Hardware under open license (CERN-OHL-S v2)
│   ├── cad/                     # Native CAD files (assemblies, parts)
│   ├── drawings/                # Technical drawings (PDF, DWG, DXF)
│   │   ├── mechanical/          # Mechanical drawings of assemblies and parts
│   │   └── electrical/          # Electrical drawings (schematics, layouts and wiring)
│   ├── img/                     # Images and renders of the machine
│   ├── step/                    # Neutral CAD exports (STEP, IGES)
│   └── stl/                     # STL files for 3D printing
│
├── LICENSE_CERN_OHL_S           # Hardware license (CERN-OHL-S v2)
└── README.md                    # Main README (Spanish)
