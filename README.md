# ONERA-M6-Wing-CFD-Simulation-in-ANSYS-Fluent
This repository documents a high-fidelity Computational Fluid Dynamics (CFD) analysis of the ONERA M6 wing, a benchmark case widely used for validating aerodynamic solvers. The simulation was carried out in ANSYS Fluent, covering all phases from domain generation and meshing to solver setup, post-processing, grid convergence .

📄 Project Overview
The ONERA M6 simulation investigates transonic airflow characteristics over a swept wing using varying mesh resolutions and physical conditions. Results include flow visualizations, force coefficients, and pressure distributions compared with NASA-provided experimental datasets.

🧩 Simulation Workflow
Fluid Domain Creation
Accurate 3D geometry of the ONERA M6 wing
Far-field boundaries placed several chord lengths away
Symmetry plane used to reduce computational cost

Meshing Strategy
Hybrid mesh: structured hex mesh near wing; unstructured tetrahedrals in far-field
Inflation layers along wing surface for boundary layer resolution
Mesh quality checked with skewness, aspect ratio, orthogonality

CFD Solver Setup
Solver: ANSYS Fluent (density-based)
Turbulence Model: Spalart-Allmaras or SST k-ω
Boundary Conditions:
Mach numbers and angles of attack based on experimental runs
Pressure far-field, symmetry, and wall (no-slip) boundaries

Solver Settings
Iterations: 500
Time scale factor: 1
Reporting interval: 1

📊 Post-Processing & Analysis
Flow Visuals: Pressure coefficient contours, velocity vectors, shockwaves
Forces: Coefficient of lift (C_L), drag (C_D), and moment (C_M)

Flow Features:
Boundary layer development
Flow separation
Shock-boundary layer interaction
Vorticity and turbulence regions

📈 Grid Convergence Study
Base, medium, and fine mesh levels
Residuals and force coefficients monitored for convergence
Grid Convergence Index (GCI) applied to validate mesh independence
Optimal mesh selected balancing accuracy and computational efficiency

🔬 Experimental Validation
Compared CFD results against NASA’s ONERA M6 datasets:
Run 308 (α = 3.06°, M = 0.8395)
Run 565 (α = 6.06°, M = 0.8372)
Cp distribution at various spanwise stations compared with experimental results
Higher angle of attack produced greater suction (more negative Cp) on the wing’s upper surface


📄 README.md: Full technical explanation and project summary

🧠 Skills & Learnings
Meshing and turbulence modeling for transonic wings
Grid convergence validation using Richardson extrapolation and GCI
Critical evaluation of aerodynamic performance using lift, drag, and pressure coefficients
Comparing simulated data with physical test results

🛠 Tools Used
ANSYS Fluent
ANSYS Meshing
CFD-Post / ParaView for visualization
Excel/Python for result comparison and plotting
