# tensile-testing-machine-astm-d638
Open-hardware tensile testing machine for plastics (ASTM D638). Project by Diego Víctor Saavedra Ravier.

# Máquina de Ensayo de Tracción de Plásticos (ASTM D638)

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](LICENSE_CC_BY-SA)
[![License: CERN-OHL-S v2](https://img.shields.io/badge/License-CERN--OHL--S%20v2-blue.svg)](LICENSE_CERN_OHL_S)

Máquina de ensayo de tracción (UTM) para **plásticos**, orientada a piezas fabricadas por **manufactura aditiva (impresión 3D)** y diseñada para cumplir con los requerimientos de la norma **ASTM D638** para garantizar obtener ensayos válidos y comparables con otras máquinas bajo el mismo estándar.

Proyecto de **grado en Ingeniería Electromecánica** – UTN FR Chubut.  

> Autor: **Diego Víctor Saavedra Ravier**  
> Año: **2025**  
> Licencias: **CC BY-SA 4.0** (documentación) y **CERN-OHL-S v2** (hardware)

---

## 📸 Vista general de la máquina

<p align="center">
  <img src="documentation/img/vista%20con%20cubres.jpg" alt="Máquina de Ensayo de Tracción de Plásticos - Render frontal" width="480">
</p>

---

## 🧩 Descripción general

Este proyecto presenta el **diseño y cálculo** de una máquina de ensayo de tracción para todo tipo de plásticos, pero con mayor foco en materiales utilizados en **Manufactura Aditiva** (FFF/FDM, SLA, SLS, etc.). La máquina busca ser:

- **Accesible y de bajo costo**
- **Replicable** con recursos locales
- **Documentada y abierta** para la comunidad académica y maker

El diseño cumple con los requerimientos principales de la norma **ASTM D638** para probetas tipo “dog bone”, poniendo especial énfasis en:

- Limitación de la deformación propia de la máquina  
- Correcta selección de celda de carga, transmisión, estructura, mordazas y accesorios  
- Posibilidad de integrar un sistema extensométrico basado en **correlación digital de imágenes (DIC)**

Actualmente el proyecto abarca el diseño completo, cálculos, propuesta de electrónica y control, planos, listado de materiales (BOM) y costos de fabricación. No se incluye la fabricación del prototipo físico.

---

## 🔧 Características principales

- **Norma de referencia:** **ASTM D638** (ensayo de tracción en plásticos)
- **Capacidad de ensayo objetivo:** hasta **10 kN** (dimensionada para cubrir la mayoría de polímeros usados en impresión 3D)
- **Rigidez:** **25,4[kN/mm]** (para cumplir con el requerimiento 5.1.6 de la norma)
- **Peso de la máquina:** **75[kg]**
- **Probetas:** **tipo (I, II, II, IV, V)**
- **velocidad máxima:** **100[mm/min]**
- **Ámbito de uso:**  
  - Laboratorios de universidades e institutos  
  - Talleres y emprendimientos que utilizan manufactura aditiva
  - Industria del plástico
- **Diseño estructural:**  
  - Marco con caños estructurales
  - Cruceta móvil en la parte superior de la máquina 
  - Sistema de transmisión con tornillos de potencia y caja reductora
  - Uso intensivo de análisis FEA en componentes críticos
- **Componentes impresos en 3D:**  
  - Caja reductora de 2 etapas con poleas y correas sincrónicas (i=8,16 T=11Nm)
  - Piezas auxiliares y de soporte  
- **Sistema extensométrico propuesto:**  
  - **DIC** con Raspberry Pi + cámara de 108 MP Arducam  
  - Alternativas de software open source para el procesado de imágenes

---
### Estado del proyecto

- ✅ Diseño y documentación completos
- ⚙️ En espera de fabricación del prototipo
- 📈 Abierto a mejoras y contribuciones

---

## 📂 Estructura del repositorio

> Nota: Esta sección describe la estructura de los archivos de este proyecto.

```text
tensile-testing-machine-astm-d638/
│
├── documentation/               # Documentación bajo licencia (CC BY-SA 4.0)
│   ├── informe.pdf              # Informe completo del Proyecto Final de Grado
│   ├── anexos/                  # Anexos, planillas y recursos complementarios
│   └── img/                     # Renders, fotos y videos
│
├── hardware/                    # Hardware bajo licencia (CERN-OHL-S v2)          
│   ├── cad/                     # Archivos CAD nativos (ensambles, piezas)          
│   ├── drawings/                # Planos técnicos (PDF, DWG, DXF)          
│   │   ├── mechanical/          # Planos mecánicos de conjuntos y piezas          
│   │   └── electrical/          # Planos eléctricos de conjuntos y piezas           
│   ├── step/                    # Exportaciones neutrales (STEP, IGES)          
│   └── stl/                     # Archivos STL para impresión 3D
│
├── LICENSE_CC_BY-SA             # Licencia para documentación (CC BY-SA 4.0)
├── LICENSE_CERN_OHL_S           # Licencia para hardware (CERN-OHL-S v2)
└── README.md                    # Este archivo
