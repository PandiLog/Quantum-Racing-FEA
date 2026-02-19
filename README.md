# Python FEA Post-Processing & Structural Optimization: Steering Extension
### Formula SAE Steering System Validation

## Project Overview
[cite_start]This repository documents the structural validation and optimization of a steering knuckle extension for a Formula SAE-style vehicle[cite: 101, 110]. [cite_start]The project transitions from traditional manual FEA to an **automated data-driven workflow** using Python to process simulation results, enabling rapid design iteration and objective decision-making[cite: 132].

[cite_start]The primary objective was to design a monolithic extension that balances structural safety ($FOS > 2.0$), weight reduction, and manufacturability to recover the functionality of a detached steering arm[cite: 107, 111].

## Automated CAE Workflow
To align with industry-standard "CAE Champ" roles, this project implements a **reproducible simulation pipeline**:

1.  [cite_start]**FEA Iterations**: Linear static analysis of three distinct design families (110mm V1, 110mm V2, and 90mm Final) conducted in **SolidWorks Simulation**[cite: 106, 134].
2.  [cite_start]**Data Extraction**: Raw stress and displacement data exported as CSV datasets to ensure full traceability of results[cite: 132, 141].
3.  **Python Post-Processing**: A custom script parses the datasets to:
    * [cite_start]Calculate the **Efficiency Metric** ($\frac{FOS}{kg}$) for each design[cite: 141].
    * [cite_start]Generate **Normalized Path Plots** to visualize stress distribution along critical geometric features[cite: 142, 162].
    * [cite_start]Produce a comparative **Performance Matrix** to justify the final selection[cite: 198].

## Key Results & Optimization
[cite_start]The automated analysis identified the **90mm Monolithic Design** as the optimal solution, significantly outperforming the initial assembly[cite: 107, 200]:

| Performance Metric | Initial Prototype (110mm V1) | Optimized Design (90mm) | Improvement (%) |
| :--- | :--- | :--- | :--- |
| **Max. Stress** | 574.91 MPa | 242.02 MPa | [cite_start]**57.9% Reduction** [cite: 198] |
| **Total Mass** | 0.088 kg | 0.033 kg | [cite_start]**62.5% Reduction** [cite: 198] |
| **Min. FOS** | 1.02 | 2.42 | [cite_start]**137.3% Increase** [cite: 198] |
| **Displacement** | 2.50 mm | 0.13 mm | [cite_start]**94.7% Reduction** [cite: 198] |

## ⚙️ Tech Stack
* [cite_start]**CAE/FEA**: SolidWorks Simulation (CSWA-S Certified)[cite: 134].
* [cite_start]**Data Science**: Python (Pandas for data cleaning, Matplotlib for dashboards/plotting)[cite: 132].
* **CAD**: SolidWorks (CSWP Certified - Perfect Score 318/318).
* **Standards**: ASME Y14.5-2018 (GD&T) for manufacturing readiness.

## 🚀 "Machine Learning Ready" Data
[cite_start]All simulation results are structured in standardized CSV formats[cite: 141]. This ensures **data traceability** and readiness for integration into larger engineering databases or machine-learning models for predictive structural analysis—directly supporting the requirements for the **Wheels CAE team** workflow.

---

### Contact
**Galo Aréchiga Gutiérrez**
* [LinkedIn](https://linkedin.com/in/galo)
* [Email](mailto:galo.arechiga@gmail.com)
