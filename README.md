# High-Velocity Ball-Plate Impact Analysis using ANSYS LS-DYNA

Explicit dynamics finite element simulation of high-velocity ball-plate impacts using ANSYS LS-DYNA with rigorous mesh convergence and energy validation checks.

## Project Overview
[cite_start]This project presents a finite element simulation of a high-velocity ball impacting a stationary metal plate[cite: 1]. [cite_start]Utilizing the explicit dynamics capabilities of **ANSYS LS-DYNA**, the study focuses on tracking transient stress propagation, non-linear material deformation patterns, and energy absorption mechanics during a severe structural impact event[cite: 1].

## Technical Stack & Framework
* [cite_start]**Solver / FEA Engine:** ANSYS LS-DYNA (Explicit Dynamics Solver) [cite: 1]
* **Pre/Post-Processor:** LS-PrePost
* [cite_start]**Key Methodologies:** Finite Element Analysis (FEA), Mesh Convergence Study, Energy Conservation Validation [cite: 1]

## Simulation Setup & Methodology
1. [cite_start]**Geometry & Domain:** Modeled a spherical object (ball) impacting a thin bounded target plate[cite: 1].
2. [cite_start]**Material Modeling:** Configured non-linear plastic material properties to accurately represent high-strain-rate deformation behavior[cite: 1].
3. [cite_start]**Boundary Conditions:** Defined an explicit velocity vector for the projectile and constrained the outer edges of the plate to simulate a fixed fixture[cite: 1].
4. [cite_start]**Solver Setup:** Executed an explicit time-integration scheme suited for transient, short-duration impact phenomena[cite: 1].

## Grid Independence & Numerical Validation
To ensure solution accuracy and eliminate common numerical errors inherent in explicit dynamics, the following verification pipeline was established:
* [cite_start]**Mesh Refinement:** Conducted systematic mesh convergence checks at the high-stress impact zone to establish structural response independence from element sizing[cite: 1].
* [cite_start]**Energy Balance Verification:** Analyzed the global energy balance to ensure physical consistency[cite: 1]. [cite_start]Total energy remained stable, confirming that artificial energies (such as hourglassing) were minimized and kept within acceptable industrial thresholds (typically < 5% of internal energy)[cite: 1].

## Key Results & Engineering Insights
* [cite_start]**Deformation Analysis:** Captured structural deformation histories and localized plastic strain distributions across the target plate[cite: 1].
* [cite_start]**Stress Propagation:** Visualized Von-Mises stress waves radiating outward from the point of impact[cite: 1].
* [cite_start]**Energy Absorption:** Quantified the conversion of the projectile's Kinetic Energy into the plate's Internal (Plastic Strain) Energy[cite: 1].

## Visualizations


### 1. Impact Animation (Explicit Dynamics)
![Impact Animation](Results/impact_animation.gif)
*Figure 1: High-velocity transient impact propagation and plate deformation.*

### 2. Von-Mises Stress Distribution
![Stress Distribution](Results/von_mises_stress.png)
*Figure 2: Peak stress contours at the time of maximum penetration.*

### 3. Energy Conservation Plot
![Energy Validation Plot](Results/energy_plot.png)
*Figure 3: Global energy curve displaying Kinetic Energy, Internal Energy, and Hourglass Energy over time.*

## Repository Structure
```text
├── Input_Decks/          # LS-DYNA keyword files (.k / .key)
├── CAD_Models/           # Geometry files (.STEP / .IGS)
├── Results/              # Animation GIFs, stress plots, and energy graphs
└── README.md             # Project documentation
