# Low-Power Dual-Edge Triggered Flip-Flop in Cadence Virtuoso

> **Transistor-Level Design, Layout, Simulation, and Comparative Analysis of Dual-Edge Triggered Flip-Flop Architectures**

A Cadence Virtuoso-based VLSI design project focused on the implementation, simulation, layout, and performance comparison of multiple **Dual-Edge Triggered Flip-Flop (DETFF)** architectures. The project investigates low-power flip-flop designs and evaluates their **power consumption, propagation delay, Power-Delay Product (PDP), transistor count, and physical area**.

The work culminates in the implementation and evaluation of a **Single-Transistor Clocked (STC) DETFF** architecture based on the referenced IEEE research paper.

---

## Project Overview

Flip-flops are fundamental sequential elements in digital integrated circuits and can contribute significantly to overall system power consumption due to their continuous clock activity.

**Dual-Edge Triggered Flip-Flops (DETFFs)** capture data on both the rising and falling edges of the clock. This enables the same throughput to be achieved at a lower clock frequency, potentially reducing dynamic power consumption.

This project implements and evaluates multiple DETFF architectures at the **transistor level using Cadence Virtuoso**, followed by custom layout design and post-layout verification.

The study compares conventional and proposed architectures to investigate the trade-offs between:

- Power consumption
- Propagation delay
- Power-Delay Product
- Transistor count
- Silicon area
- Functional correctness
- Layout verification

---

## Objectives

The primary objectives of this project are:

- Implement multiple DETFF architectures at the transistor level.
- Design and simulate the circuits using **Cadence Virtuoso and Spectre**.
- Develop custom CMOS layouts for the implemented architectures.
- Perform functional verification using transient simulations.
- Evaluate power consumption and propagation delay.
- Compare the Power-Delay Product (PDP) of different architectures.
- Analyze transistor count and physical area.
- Perform layout verification using DRC/LVS methodologies.
- Study the power-performance trade-offs of low-power DETFF architectures.
- Implement and evaluate the proposed **Single-Transistor Clocked (STC) DETFF**.

---

## Implemented Architectures

The repository contains implementations and simulation results for several flip-flop architectures:

| Architecture | Description |
|---|---|
| **TGFF** | Transmission Gate Flip-Flop |
| **S_DET** | Static Dual-Edge Triggered Flip-Flop |
| **S_TSPC_DET** | Static TSPC Dual-Edge Triggered Flip-Flop |
| **FS_TSPC_DET** | Fully Static TSPC Dual-Edge Triggered Flip-Flop |
| **FNC_DET** | Four-Node Clocked Dual-Edge Triggered Flip-Flop |
| **Proposed STC DETFF** | Single-Transistor Clocked Dual-Edge Triggered Flip-Flop |

The different architectures are simulated and compared to identify their respective advantages and limitations in terms of power, speed, and area.

---

## Design Flow

The project follows a complete transistor-level VLSI design flow:

```text
        Architecture Selection
                |
                v
       Transistor-Level Design
                |
                v
       Schematic Implementation
          (Cadence Virtuoso)
                |
                v
        Functional Simulation
             (Spectre)
                |
                v
        Performance Analysis
       +--------+--------+
       |        |        |
       v        v        v
     Power    Delay     PDP
                |
                v
          Layout Design
                |
                v
        DRC / LVS Verification
                |
                v
       Post-Layout Simulation
                |
                v
        Comparative Analysis
```

---

## Design Environment

| Tool / Technology         | Purpose                              |
| ------------------------- | ------------------------------------ |
| **Cadence Virtuoso**      | Schematic and circuit design         |
| **Cadence Spectre**       | Transistor-level simulation          |
| **Virtuoso Layout Suite** | Custom physical layout               |
| **DRC**                   | Design Rule Checking                 |
| **LVS**                   | Layout Versus Schematic verification |
| **CMOS Technology**       | Transistor-level implementation      |

---

## Repository Structure

```text
Low-Power-DET-Flip-Flop-in-Cadence-Virtuoso/
|
+-- Cadence_Virtuoso/
|   +-- DETFF/
|       +-- FNC_DET/
|       +-- ...
|       +-- ...
|
+-- DETFF_Plots/
|   |
|   +-- FNC_DET/
|   |   +-- Delay_Vdd/
|   |   +-- FlipFlop/
|   |   +-- Power_Activity/
|   |   +-- Power_Vdd/
|   |   +-- ProcessCorner/
|   |
|   +-- FS_TSPC_DET/
|   +-- Proposed/
|   +-- S_DET/
|   +-- S_TSPC_DET/
|   +-- TGFF/
|   |
|   +-- Delay_Vdd_Final.png
|   +-- Power_Corner_Final.png
|   +-- Power_Vdd_Final.png
|
+-- Documents/
|   |
|   +-- Reference_Papers/
|   |
|   +-- VLSI_Arch_Project_DETFF_*.pdf
|   +-- VLSI_Arch_Project_Final_Report_*.pdf
|
+-- LICENSE
+-- README.md
```

### Repository Contents

**`Cadence_Virtuoso/`**
Contains the Cadence Virtuoso design data, including the transistor-level implementation and associated circuit design files.

**`DETFF_Plots/`**
Contains simulation results and plots generated during the characterization of the different DETFF architectures. Results include power, delay, supply-voltage, process-corner, and activity-based analyses.

**`Documents/`**
Contains project documentation, final reports, presentations, and reference research papers.

**`LICENSE`**
Contains the licensing information for the repository.

---

## Performance Evaluation

Each flip-flop architecture is evaluated using multiple design metrics.

### Power Consumption

The average power consumed by each architecture is measured under comparable operating conditions.

### Propagation Delay

The propagation delay is measured to determine the speed of the flip-flop during data transitions.

### Power-Delay Product

The **Power-Delay Product (PDP)** is used as a combined metric for evaluating the energy-performance trade-off:

$$PDP = P_{avg} \times t_{delay}$$

A lower PDP indicates better energy efficiency for a given operating condition.

### Transistor Count

The number of MOS transistors required by each architecture is considered as an indicator of circuit complexity and implementation cost.

### Physical Area

The custom layout area is evaluated to understand the physical overhead associated with each architecture.

### Process and Supply-Voltage Analysis

The designs are characterized across different supply-voltage and process conditions to evaluate robustness and sensitivity to operating conditions.

---

## Simulation and Analysis

The repository includes plots and analysis covering:

- Power vs. Supply Voltage
- Delay vs. Supply Voltage
- Power vs. Process Corner
- Power vs. Activity
- Flip-flop functional behavior
- Comparative performance analysis

The final comparison plots are available in:

```text
DETFF_Plots/
|
+-- Delay_Vdd_Final.png
+-- Power_Corner_Final.png
+-- Power_Vdd_Final.png
```

---

## Low-Power Design Focus

The primary focus of the project is to investigate techniques for reducing the power consumption of DETFF architectures while maintaining acceptable timing performance.

Particular attention is given to the **Single-Transistor Clocked (STC)** approach, which aims to reduce redundant clock transitions and associated switching activity.

The proposed architecture is therefore evaluated against conventional DETFF implementations using power, delay, PDP, and area-related metrics.

---

## Verification

The implemented circuits undergo multiple stages of verification.

### Functional Verification

Transient simulations are used to verify correct data capture on both clock edges.

### DRC Verification

Design Rule Checking is performed to ensure that the custom layout satisfies the required fabrication design rules.

### LVS Verification

Layout Versus Schematic verification is used to ensure that the physical implementation corresponds to the intended transistor-level schematic.

### Post-Layout Analysis

The verified layouts can be further evaluated through post-layout simulation to account for physical implementation effects.

---

## Documentation

Project documentation is available under:

```text
Documents/
```

This directory contains:

- Final project report
- Project presentation
- Reference research papers

The `Reference_Papers` directory contains the research material used as the basis for the architecture study and implementation.

---

## Reference Paper

The proposed architecture is based on the following IEEE publication:

> **"Low-Power Redundant-Transition-Free TSPC Dual-Edge Triggering Flip-Flop Using Single-Transistor Clocked Buffer"**

This repository contains an **independent academic implementation and evaluation** of the concepts presented in the referenced work.

Please refer to the original publication for the complete theoretical methodology and proposed circuit architecture.

---

## Authors

- **Bharat Kumar DD**
- **Vinay P Ramesh**
- **R Vaikunth**
- **Surya Sumeet Singh**
- **Pravin Kumar V**
- **Shudharshan A**
- **Harshith Krishna R**

**Integrated M.Tech. — Electronics and Communication Engineering, **
**International Institute of Information Technology Bangalore (IIIT Bangalore)**

---

## Acknowledgement

This project was developed as an academic VLSI design project involving transistor-level circuit design, simulation, custom layout, and performance analysis.

The implementation and characterization were carried out using **Cadence Virtuoso** and associated VLSI design and verification tools.

---

## License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

## Project Highlights

```text
[x] Multiple DETFF architectures implemented
[x] Transistor-level CMOS design
[x] Cadence Virtuoso schematic design
[x] Spectre transient simulation
[x] Custom physical layout
[x] DRC / LVS verification
[x] Power and delay characterization
[x] Process-corner analysis
[x] Supply-voltage analysis
[x] Comparative performance evaluation
[x] Low-power STC DETFF implementation
```

---

<p align="center">
  <b>Low-Power VLSI Design &bull; Dual-Edge Triggered Flip-Flops &bull; Cadence Virtuoso</b>
</p>

<p align="center">
  <i>Designed and evaluated as an academic VLSI circuit design project at IIIT Bangalore.</i>
</p>
