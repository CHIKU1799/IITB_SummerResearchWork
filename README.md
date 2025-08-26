# IITB_SummerResearchWork
# Summer Research Fellowship: DC-DC Converters & MPPT in PV Systems

This repository documents my 8-week summer research fellowship at IIT Bombay, under the guidance of Prof. Vivek Agarwal. The research focused on the fundamental principles and practical application of **DC-DC converters** for **Maximum Power Point Tracking (MPPT)** in photovoltaic (PV) systems.

---

## 💡 Project Overview
The primary goal of this fellowship was to understand and simulate the role of DC-DC converters as power processors in a PV system. By dynamically adjusting the input voltage, these converters can ensure the solar panel operates at its **Maximum Power Point (MPP)**, thereby maximizing energy extraction.

---

## 📚 Key Concepts & Topics

### DC-DC Converters
The project began with a theoretical deep dive into DC-DC converters, including both isolated and non-isolated types. I focused on the non-isolated family, specifically:
* **Buck Converter**: A step-down converter used to decrease voltage.
* **Boost Converter**: A step-up converter used to increase voltage.
* **Buck-Boost Converter**: A versatile converter that can both step up and step down voltage.

### Photovoltaic (PV) Cell Modeling
A crucial component of the research involved understanding the behavior of a PV cell. This included:
* **Mathematical Modeling**: Simulating the electrical characteristics of a PV cell using its equivalent circuit diagram, which includes a diode, a series resistor, and a parallel resistor.
* **Fill Factor**: An important metric used to evaluate the efficiency of a solar cell, representing the ratio of maximum power to the product of open-circuit voltage and short-circuit current.

---

## 💻 Simulation & Algorithms

All simulations were performed using **MATLAB**, which allowed for a detailed analysis of converter operation and algorithm performance.

### Maximum Power Point Tracking (MPPT)
The core of the research centered on MPPT, the technique used to extract the maximum available power from a PV module under varying conditions. A DC-DC converter is essential for this, acting as an impedance matcher between the solar panel and the load.

#### **Perturb and Observe (P&O) Algorithm**
This algorithm operates by periodically perturbing (increasing or decreasing) the converter duty cycle and observing the resulting change in power. If the power increases, the algorithm continues to perturb in the same direction; otherwise, it reverses the direction.
* `po_mppt.m`: The MATLAB code for the P&O algorithm can be found in this file.

#### **Incremental Conductance (I.C.) Algorithm**
The I.C. algorithm is an improvement over P&O, as it determines the direction of perturbation more accurately by analyzing the slope of the power-voltage (P-V) curve. The algorithm tracks the relationship between the change in power and the change in voltage to find the optimal operating point.
* `ic_mppt.m`: The MATLAB code for the Incremental Conductance algorithm is available in this file.

### Results
The repository includes graphical results showing **Power vs. Load Resistance** curves, both with and without the MPPT algorithm enabled. These simulations clearly demonstrate the effectiveness of the DC-DC converter in maximizing power output.

---

## 📂 Repository Structure
.
├── README.md                     
├── po_mppt.m                     
├── ic_mppt.m                     
├── simulations/                   
│   ├── buck_boost_converter.slx   
│   └── pv_mppt_simulation.slx     
├── report/                        
│   └── final_report.pdf           
└── images/                        
└── pv_curve.png              


undefined
