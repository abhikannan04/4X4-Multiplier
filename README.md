# 4x4 Multiplier in Cadence Virtuoso

## Project Overview
This project implements a CMOS 4x4 Array Multiplier using fundamental logic components, such as AND gates and 28-Transistor Mirror Full Adders. The design focuses on verifying the correct functionality of the multiplier circuit without any low-power optimization techniques.

The project progressed in phases, starting with the basic building blocks (AND gates and Full Adders) and culminating in a functional 4x4 multiplier. The design has been verified using Cadence Virtuoso, with output waveforms analyzed to confirm accuracy.

### Components Built
- **AND Gate**: 
  - Implemented using PMOS and NMOS transistors in a basic CMOS design.
  
- **CMOS 28T Mirror Full Adder**: 
  - Designed using a 28-transistor mirror technique to achieve balanced performance for carry and sum operations.
  
- **2x2 Multiplier**: 
  - Built using the AND gates and Full Adders. Output waveforms were verified for various input combinations, confirming correct multiplication results.

- **4x4 Multiplier**: 
  - Extended from the 2x2 multiplier using an array multiplication approach. The circuit was simulated, and output graphs were verified to be accurate.

![Simulation Output](https://github.com/user-attachments/assets/eb96acd6-9e12-4f74-be27-d807999b0a88)

### Technology
- **Process**: GPDK180 (180 nm CMOS)
- **Tools**: Cadence Virtuoso (for schematic entry, simulation, layout)
- **Voltage**: 1.8V (adjustable for Dynamic Voltage Scaling)

---

## Project Phases

### Phase 1: Circuit Design and Setup
1. **AND Gates and Full Adders**:
   - Designed the basic building blocks with minimum-sized transistors for low power.
   - Initial transistor parameters selected based on GPDK180 values:
     - **Threshold Voltage (Vt)**: Standard, low, or high (to be tuned in later phases).
     - **Transistor Widths (Wp/Wn)**: Set to **Wn = 180 nm** and **Wp = 360 nm**.

2. **Combining Partial Products**:
   - The 4x4 multiplier is built by combining partial products using AND gates.
   - The partial products are summed with half adders and full adders to produce the final result.

### Phase 2: Simulation and Power Analysis
1. **Schematic and Functional Verification**:
   - The complete 4x4 multiplier circuit is assembled and simulated in **Cadence Virtuoso ADE**.
   - Functional tests verify that the circuit correctly multiplies two 4-bit numbers.

2. **Power and Timing Analysis**:
   - Static and dynamic power consumption analysis is conducted.
   - Timing analysis identifies critical paths in the design.

---

## How to Run Simulations

1. **Environment Setup**:
   - Ensure that **GPDK180 technology** is properly installed in **Cadence Virtuoso**.
   - Set up the design environment by creating a new project and selecting GPDK180 as the process.

2. **Simulation Steps**:
   - Use **Virtuoso ADE** to run simulations.
   - Run functional simulations with different sets of 4-bit inputs.
   - Perform power analysis using built-in ADE tools to evaluate total power consumption.

---

## Future Steps
**Phase 3 (Upcoming)**:
- Apply **multi-Vt optimization** and **Dynamic Voltage Scaling (DVS)** to reduce power consumption.
- Complete final layout and parasitic extraction.

---

