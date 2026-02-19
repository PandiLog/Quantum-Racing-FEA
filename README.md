# Python FEA Post-Processing & Structural Optimization: Steering Extension
### Formula SAE Steering System Validation

## Project Overview
This repository documents the structural validation and optimization of a steering knuckle extension for a Formula SAE-style vehicle[cite: 101, 110]. The project transitions from traditional manual FEA to an **automated data-driven workflow** using Python to process simulation results, enabling rapid design iteration and objective decision-making.

The primary objective was to design a monolithic extension that balances structural safety ($FOS > 2.0$), weight reduction, and manufacturability to recover the functionality of a detached steering arm.

## Automated CAE Workflow
This project implements a **reproducible simulation pipeline**:

1.  **FEA Iterations**: Linear static analysis of three distinct design families (110mm V1, 110mm V2, and 90mm Final) conducted in **SolidWorks Simulation**.
2.  **Data Extraction**: Raw stress and displacement data exported as CSV datasets to ensure full traceability of results.
3.  **Python Post-Processing**: A custom script parses the datasets to:
    * Calculate the **Efficiency Metric** ($\frac{FOS}{kg}$) for each design.
    * Generate **Normalized Path Plots** to visualize stress distribution along critical geometric features.
    * Produce a comparative **Performance Matrix** to justify the final selection.

## Key Results & Optimization
The automated analysis identified the **90mm Monolithic Design** as the optimal solution, significantly outperforming the initial assembly:

| Performance Metric | Initial Prototype (110mm V1) | Optimized Design (90mm) | Improvement (%) |
| :--- | :--- | :--- | :--- |
| **Max. Stress** | 574.91 MPa | 242.02 MPa | **57.9% Reduction**  |
| **Total Mass** | 0.088 kg | 0.033 kg | **62.5% Reduction**  |
| **Min. FOS** | 1.02 | 2.42 | **137.3% Increase**  |
| **Displacement** | 2.50 mm | 0.13 mm | **94.7% Reduction**  |

##  Tech Stack
* **CAE/FEA**: SolidWorks Simulation .
* **Data Science**: Python (Pandas for data cleaning, Matplotlib for plotting).
* **CAD**: SolidWorks .

## Documentation
For breakdown of the FEA methodology, loading conditions, and the results, please refer to the following report:

> [** View Full Report (PDF)**](./reports/Validación y Optimización Estructural_ Extensión de Dirección.pdf)
---

### Contact
**Galo Aréchiga Gutiérrez**
* [LinkedIn](https://www.linkedin.com/in/galo-arechiga-gutierrez-b81b5935b/)
* [Email](mailto:galo.arechiga@gmail.com)
