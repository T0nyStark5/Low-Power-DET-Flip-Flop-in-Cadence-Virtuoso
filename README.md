# Low-Power Dual-Edge Triggered Flip-Flop

A Cadence Virtuoso implementation of a low-power Dual-Edge Triggered Flip-Flop (DETFF) based on the IEEE paper **"Low-Power Redundant-Transition-Free TSPC Dual-Edge Triggering Flip-Flop Using Single-Transistor Clocked Buffer."**

The project focuses on designing, simulating, and comparing several Dual-Edge Triggered Flip-Flop architectures to achieve lower power consumption while maintaining competitive speed and area. The work includes transistor-level schematic design, layout implementation, post-layout verification, and performance evaluation using Cadence Virtuoso.

---

## Project Overview

Conventional flip-flops account for a significant portion of the power consumption in modern digital integrated circuits because they are clocked continuously throughout system operation. Dual-Edge Triggered Flip-Flops (DETFFs) improve energy efficiency by capturing data on both the rising and falling edges of the clock, enabling the clock frequency to be reduced without affecting throughput.

This repository presents the implementation and comparison of multiple DETFF architectures, culminating in the implementation of the proposed low-power Single-Transistor Clocked (STC) DETFF architecture.

---

## Objectives

- Implement multiple DETFF architectures in Cadence Virtuoso
- Perform transistor-level simulations
- Design custom CMOS layouts
- Compare power consumption, delay, transistor count, and area
- Validate functionality through transient simulations
- Analyze trade-offs between conventional and proposed designs

---

## Implemented Architectures

- Transmission Gate Flip-Flop (TGFF)
- TSPC Dual-Edge Triggered Flip-Flop
- Fully Static TSPC DETFF
- Four-Node Clocked (FNC) DETFF
- Proposed Single-Transistor Clocked (STC) DETFF

---

## Design Environment

| Tool | Description |
|------|-------------|
| Cadence Virtuoso | Schematic Capture |
| Spectre | Circuit Simulation |
| Virtuoso Layout Suite | Physical Layout |
| Assura / LVS | Layout Verification |

---

## Technology

- CMOS Technology
- Transistor-Level Design
- Custom Layout Design
- Spectre Analog Simulation

---

## Repository Structure

```
├── Documents/
│   ├── Project_Report.pdf
│   ├── Final_Presentation.pdf
│   └── Reference_Papers/
│
├── Cadence_Virtuoso/
│   ├── DETFF/
│
├── DETFF_Plots/
│   ├── FNC_DET/
│   ├── FS_TSPC_DET/
│   ├── Proposed/
│   ├── S_DET/
│   └── S_TSPC_DET/
│   └── TGFF/
│   └── Delay_Vdd_Final.png/
│   └── Power_Corner_Final.png/
│   └── Power_Vdd_Final.png/
│   
├── LICENSE
└── README.md
```

---

## Performance Metrics

The implemented flip-flops are evaluated using

- Average Power Consumption
- Propagation Delay
- Power-Delay Product (PDP)
- Transistor Count
- Silicon Area
- Layout Verification
- Functional Correctness

Detailed numerical results are available in the project report and presentation.

---

## Results

The proposed Single-Transistor Clocked DETFF demonstrates significant power reduction compared to conventional DETFF architectures while maintaining competitive timing performance.

The repository includes

- Schematic Designs
- Layout Designs
- Simulation Waveforms
- Comparative Analysis
- Project Report
- Final Presentation

---

## Current Status

- Schematic implementation completed
- Layout implementation completed
- Functional verification completed
- Comparative analysis completed
- Documentation is being refined

Future updates will include additional characterization results and expanded verification.

---

## Reference

This project is based on the following IEEE publication:

> **Low-Power Redundant-Transition-Free TSPC Dual-Edge Triggering Flip-Flop Using Single-Transistor Clocked Buffer**

The repository contains an independent implementation created for academic and educational purposes. Please refer to the original publication for the complete research methodology.

---

## Authors
**Bharat Kumar DD**
**Vinay P Ramesh**
**R Vaikunth**
**Surya Sumeet Singh**
**Pravin Kumar V**
**Shudharshan A**
**Harshith Krishna R**


Integrated M.Tech  Electronics and Communication Engineering

IIIT Bangalore

---

## License

This project is licensed under the MIT License.

See the LICENSE file for details.

---

## Acknowledgement

This implementation was developed as an academic VLSI design project using Cadence Virtuoso for schematic design, simulation, layout generation, and performance evaluation.
