# Multiphysics Structural and Thermal FEA of a Single-Cylinder Engine Crank Assembly

## Overview
This repository presents a **comprehensive multiphysics Finite Element Analysis (FEA)** of a **parametrically modeled single-cylinder engine crank-slider mechanism**, integrating **structural, thermal, and transient simulations**.  
The study replicates real-world operating conditions of an IC engine crank mechanism under combustion and heat load, using **ANSYS Workbench** for simulation and **SolidWorks / Autodesk Inventor** for CAD modeling.

---

## Project Objective
To evaluate the **mechanical integrity, thermal behavior, and time-dependent motion response** of a single-cylinder engine crank mechanism by performing:
1. **Static Structural Analysis** – Assess stresses and deformations under combustion load.  
2. **Steady-State Thermal Analysis** – Simulate heat conduction and distribution through the assembly.  
3. **Transient Structural Analysis** – Analyze motion-induced deformation during crank rotation.

---

## Tools and Software

| Task | Software Used |
|------|----------------|
| 3D CAD Modeling | Autodesk Inventor 2024 / SolidWorks 2025 |
| Simulation & FEA | ANSYS Workbench |
| File Format | STEP (.stp) |

---

## Model Composition
The crank-slider assembly was modeled parametrically and includes:
- Piston head  
- Piston pin  
- Piston ring  
- Connecting rod  
- Crankshaft  

---

## Mesh and Boundary Setup

**Mesh Details**
| Parameter | Value |
|------------|--------|
| Element Size | 0.005 m |
| Smoothing | High |
| Span Angle Center | Fine |

---

## Static Structural Analysis

**Boundary Conditions:**
- **Load:** 6 MPa combustion pressure applied on piston head  
- **Support:** Crankshaft end fixed  

**Results:**
| Parameter | Max Value | Location |
|------------|------------|----------|
| Total Deformation | 3.18×10⁻⁴ m | Piston Head |
| Equivalent (von-Mises) Stress | 2.39×10⁸ Pa | Piston Head |
| Elastic Strain | 2.74×10⁻³ | Piston Head |

*Observation:* Deformation and stresses are within safe limits, confirming mechanical robustness under peak combustion pressure.

---

## Steady-State Thermal Analysis

**Boundary Conditions:**
- Ambient temperature: 22°C  
- Applied temperature on piston head: 660°C  
- Radiation enabled on crankshaft surfaces  

**Results:**
| Component | Max Temp (°C) | Max Heat Flux (W/m²) |
|------------|----------------|----------------------|
| Piston Head | 660.0 | 1.47×10⁵ |
| Connecting Rod | 660.0 | 1.82×10⁵ |
| Crankshaft | 252.6 | 5.64×10⁴ |

*Observation:* Heat transfer is most significant between the piston and connecting rod, validating expected conduction patterns through the assembly.

---

## Transient Structural Analysis

**Joint Setup:**
| Connection | Joint Type |
|-------------|-------------|
| Crankshaft ↔ Ground | Revolute |
| Piston Head | Translational |
| Crankshaft ↔ Connecting Rod | Revolute |
| Connecting Rod ↔ Piston Pin | Revolute |
| Piston Pin ↔ Piston Head | Revolute |

**Input Motion:**
- Rotational displacement on crankshaft (Z-axis)  
- Time duration: 0 → 360 seconds  

**Results:**
- Max deformation over full rotation: **1.58×10⁻³ m**

*Observation:* Dynamic simulation replicates real engine kinematics with accurate constraint behavior, enabling future vibration and fatigue studies.

---

## Key Insights

- Structural stress concentrations observed near **piston pin and crankshaft junctions**.  
- Effective heat dissipation from **piston to crankshaft**, confirming realistic conduction behavior.  
- Time-based deformation correlates well with crank rotation phase, demonstrating **dynamic stability**.  

---

## Future Work

- Fatigue life prediction using transient stress outputs.  
- Modal and harmonic vibration analysis.  
- Thermal-structural coupling for improved accuracy.  
- Material optimization to reduce weight.  
- Incorporate CFD-based pressure distribution for realism.

---

## Results
---
## Static Structural

---

![TD_Piston_Head](https://github.com/user-attachments/assets/13351b6f-0028-4466-a384-bde6991e2954)
![TD_Cranckshaft](https://github.com/user-attachments/assets/3a1ca28f-71ff-4d83-acba-2bf53036c8f6)
![TD_Connecting_rod](https://github.com/user-attachments/assets/5d3c25a3-a8f2-4592-ae86-41032af916c8)
![TD](https://github.com/user-attachments/assets/44ad3f4e-ab2b-4e13-98ba-5dd48785d624)
<img width="1018" height="691" alt="SS Pressure" src="https://github.com/user-attachments/assets/3ea1d74e-e499-4ec1-acf5-ce3a2a9b64cb" />
<img width="1020" height="693" alt="Fixed Support" src="https://github.com/user-attachments/assets/feb2e0d3-8587-4656-afd7-39825bece5da" />
![ES_Crankshaft](https://github.com/user-attachments/assets/d6b88843-99c9-436d-b936-a69a2a004b33)
![ES_Connecting_rod](https://github.com/user-attachments/assets/b325c352-17f4-4c57-90d1-e134358d3825)
![ES](https://github.com/user-attachments/assets/f0c70aea-bfb9-497a-8fc6-f3d1647616bf)
<img width="1657" height="894" alt="ES Plot" src="https://github.com/user-attachments/assets/50380c6c-d52e-4e85-bf86-4b5d0f4930ca" />
<img width="1662" height="888" alt="ES Plot 1" src="https://github.com/user-attachments/assets/15714a93-d802-45f0-b162-a4289d2f6f50" />
![EES](https://github.com/user-attachments/assets/1003b260-d0d4-49fb-872e-cacad2325c95)


---

## Transient Analysis

---

![TD](https://github.com/user-attachments/assets/25e79567-f720-4234-99b8-a9e346c21795)
<img width="1658" height="896" alt="TD Plot" src="https://github.com/user-attachments/assets/b78b2815-6218-4a29-bf6c-fd51f3c5b1d6" />
<img width="1660" height="893" alt="Joint Rotations" src="https://github.com/user-attachments/assets/b9f75a54-f385-40e5-9fdd-a0f128fa9235" />
![ES](https://github.com/user-attachments/assets/22ffb965-79a6-41c1-8441-bb5b0ae2478f)
<img width="1659" height="899" alt="ES Plot" src="https://github.com/user-attachments/assets/11fa298c-c573-49e4-8ea1-be6507954e3f" />
![EES](https://github.com/user-attachments/assets/f36f294f-dcc4-462e-84e5-5801d7bb439a)
<img width="1658" height="893" alt="EES Plot" src="https://github.com/user-attachments/assets/e2772720-7394-4de5-aa75-bde4b05a3d78" />


---


## Steady State Analysis

---

![THF_Piston_Head](https://github.com/user-attachments/assets/2c4b98a2-59ed-409c-b10a-b76932d0e68e)
![THF_Crankshaft](https://github.com/user-attachments/assets/c2587cd7-03cc-4a2d-8419-5a8f37a97ec8)
![THF_Connecting_rod](https://github.com/user-attachments/assets/ee78f616-82aa-4b63-a23c-6c615ae2d4f3)
![THF](https://github.com/user-attachments/assets/9745049e-a32e-4519-8f0d-7d25927e8114)
<img width="1661" height="902" alt="THF Plot1" src="https://github.com/user-attachments/assets/63d22662-f82c-45cd-99c8-3bfc8fabfe1c" />
<img width="1659" height="893" alt="THF Plot" src="https://github.com/user-attachments/assets/366e667a-8e0a-446d-ba3e-7bd540b55e6e" />
![T](https://github.com/user-attachments/assets/7dec202d-abc5-4f3d-8ce3-08c3527703ed)
<img width="1530" height="637" alt="SST Temp" src="https://github.com/user-attachments/assets/064e3722-f1db-491e-b185-3718bbc27543" />
<img width="1528" height="642" alt="SST Radiation" src="https://github.com/user-attachments/assets/739cbe63-2150-4472-b156-db60b2e5f957" />


---


## 🧩 Conclusion
The analysis of the **single-cylinder crank-slider assembly** provides a holistic understanding of how **mechanical loads, heat transfer, and motion constraints** affect the engine mechanism.  
Results confirm that the design is:
- **Mechanically sound**, with all stress values below yield limits.  
- **Thermally consistent**, exhibiting realistic conduction from piston to crankshaft.  
- **Dynamically stable**, maintaining controlled deformation throughout the crank rotation.

This multiphysics investigation establishes a **robust foundation for future optimization**, including fatigue, modal, and coupled thermal-structural analyses, thereby contributing to improved reliability and performance of engine components.



---

## Skills and Keywords
`Computer-Aided Design (CAD)` • `Computer-Aided Engineering (CAE)` • `Finite Element Analysis (FEA)`  
`ANSYS Workbench` • `SolidWorks` • `Thermo-Mechanical Coupling` • `Dynamic Simulation`

---

## Outcome
This multiphysics simulation provided valuable insights into **stress zones, thermal conduction paths, and time-dependent deformation** in an IC engine crank mechanism.  
It informs design optimization strategies for **enhanced durability, thermal performance, and mechanical efficiency**.

---


## Author
**Mohammad Haris**  
Final Year B.Tech – Mechanical Engineering  
VIT-AP,Amaravati   
[Linkedin Profile](https://linkedin.com/in/mohammad-haris-13032002) | [Email](mailto:mohammaddharis1303@gmail.com)
---




