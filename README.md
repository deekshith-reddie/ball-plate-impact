# High-Velocity Ball-Plate Impact Analysis using ANSYS LS-DYNA

Explicit dynamics finite element simulation of high-velocity ball-plate impacts using ANSYS LS-DYNA with rigorous mesh convergence and energy validation checks.

## Project Overview
This project presents a finite element simulation of a high-velocity ball impacting a stationary metal plate.Utilizing the explicit dynamics capabilities of **ANSYS LS-DYNA**, the study focuses on tracking transient stress propagation, non-linear material deformation patterns, and energy absorption mechanics during a severe structural impact event

## Technical Stack & Framework
* **Solver / FEA Engine:** ANSYS LS-DYNA (Explicit Dynamics Solver)
* **Pre/Post-Processor:** LS-PrePost
* **Key Methodologies:** Finite Element Analysis (FEA), Mesh Convergence Study, Energy Conservation Validation

## Simulation Setup & Methodology
1. **Geometry & Domain:** Modeled a spherical object (ball) impacting a thin bounded target plate
2. **Material Modeling:** Configured non-linear plastic material properties to accurately represent high-strain-rate deformation behavior
3. **Boundary Conditions:** Defined an explicit velocity vector for the projectile and constrained the outer edges of the plate to simulate a fixed fixture
4. **Solver Setup:** Executed an explicit time-integration scheme suited for transient, short-duration impact phenomena

## Grid Independence & Numerical Validation
To ensure solution accuracy and eliminate common numerical errors inherent in explicit dynamics, the following verification pipeline was established:
* **Mesh Refinement:** Conducted systematic mesh convergence checks at the high-stress impact zone to establish structural response independence from element sizing
* **Energy Balance Verification:** Analyzed the global energy balance to ensure physical consistency. Total energy remained stable, confirming that artificial energies (such as hourglassing) were minimized and kept within acceptable industrial thresholds (typically < 5% of internal energy).
## Key Results & Engineering Insights
* **Deformation Analysis:** Captured structural deformation histories and localized plastic strain distributions across the target plate
***Stress Propagation:** Visualized Von-Mises stress waves radiating outward from the point of impact.
* **Energy Absorption:** Quantified the conversion of the projectile's Kinetic Energy into the plate's Internal (Plastic Strain) Energy.

## Visualizations


### 1. Impact Animation (Explicit Dynamics)
![Impact Animation](Results/<img width="1174" height="540" alt="Image" src="https://github.com/user-attachments/assets/01ba0bb4-e546-4710-8c49-f119171a6b81" />)
*Figure 1: High-velocity transient impact propagation and plate deformation.*


### 2. Energy Conservation Plot
![Energy Validation Plot](Results/<img width="683" height="304" alt="Image" src="https://github.com/user-attachments/assets/5102343d-0556-46c9-82fc-af288075cbe1" />
<img width="680" height="309" alt="Image" src="https://github.com/user-attachments/assets/57af3bd9-3872-490a-a129-513b8eb4103f" />)
*Figure 2.1: Global energy curve displaying Kinetic Energy, Internal Energy, and Hourglass Energy over time.*
*Figure 2.2: Component energy curve displaying Kinetic Energy, Internal Energy, and Hourglass Energy over time.*
