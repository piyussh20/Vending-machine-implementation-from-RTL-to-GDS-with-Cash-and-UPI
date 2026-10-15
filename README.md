# Vending-machine-implementation-from-RTL-to-GDS-with-Cash-and-UPI
Design and RTL-to-GDS implementation of a vending machine controller using Verilog HDL. The project covers RTL design, functional simulation, logic synthesis using Yosys, and physical design using OpenROAD/OpenLane, targeting the SkyWater SKY130 PDK. Includes source code, testbenches, simulation waveforms, implementation and final GDSII layout


# Vending Machine — RTL-to-GDS Implementation

A digital vending machine controller designed using Verilog HDL and implemented through an RTL-to-GDS physical design flow using open-source electronic design automation tools.

The project demonstrates the complete digital design workflow, from RTL development and functional simulation to logic synthesis, physical implementation, timing analysis, and final GDSII layout generation.

## 1. Project Overview

The vending machine is implemented as a finite state machine (FSM) that accepts coin inputs, tracks the inserted amount, and generates product dispensing and change return signals.

The design is written in Verilog HDL and functionally verified using EDA Playground.

Following functional verification, the RTL is synthesized into a gate-level netlist using Yosys. Physical implementation is then performed using OpenROAD/OpenLane on Linux, targeting the SkyWater SKY130 process design kit (PDK).

The objective is to demonstrate the complete RTL-to-GDS implementation flow using open-source EDA tools.

## 2. Project Objectives

- Design a vending machine controller using Verilog HDL.
- Implement the controller using a finite state machine.
- Verify the functionality using a Verilog testbench.
- Simulate the design and inspect signal waveforms.
- Perform logic synthesis using Yosys.
- Implement the synthesized design using OpenROAD/OpenLane.
- Perform floorplanning, placement, clock tree synthesis, and routing.
- Analyze timing and area reports.
- Generate and inspect the final GDSII layout.

## 3. Design Specifications

| Parameter | Description |
|---|---|
| Project | Vending Machine Controller |
| Design language | Verilog HDL |
| Architecture | Finite State Machine |
| Product price | ₹15 |
| Coin inputs | ₹5 and ₹10 |
| Main outputs | Product dispense and change return |
| RTL simulation | EDA Playground |
| Logic synthesis | Yosys |
| Physical design | OpenROAD/OpenLane |
| Operating environment | Linux |
| Target PDK | SkyWater SKY130 |
| Final layout format | GDSII |

The specifications above describe the basic coin-operated implementation. Update them if the final RTL uses quantity selection, cash/UPI payment selection, or other functionality.

## 4. Features

- Coin-based payment input.
- FSM-based control logic.
- Product dispensing output.
- Change return output.
- Synchronous state transitions.
- Reset functionality.
- Testbench-based functional verification.
- Gate-level synthesis.
- Physical design implementation.
- Timing and area analysis.
- Final layout generation.

## 5. System Architecture

The design consists of the following stages:

1. Coin input interface.
2. FSM controller.
3. Payment tracking logic.
4. Product dispensing logic.
5. Change return logic.

The controller processes coin inputs and generates the corresponding output signals according to the implemented state transitions.

![Project Architecture](images/project_architecture.png)

## 6. Finite State Machine

The FSM manages the payment process and determines when the required payment has been reached.

The state definitions and transitions depend on the final RTL implementation.

![FSM Diagram](images/fsm_diagram.png)

## 7. RTL-to-GDS Implementation Flow

The project follows the standard digital implementation workflow.

1. RTL design using Verilog HDL.
2. Functional simulation using EDA Playground.
3. RTL synthesis using Yosys.
4. Gate-level netlist generation.
5. Floorplanning.
6. Standard-cell placement.
7. Clock tree synthesis.
8. Signal routing.
9. Timing analysis.
10. Physical verification.
11. GDSII layout generation.

![RTL-to-GDS Flow](images/rtl_to_gds_flowchart.png)

## 8. Tools and Technologies

| Tool | Purpose |
|---|---|
| Verilog HDL | RTL design |
| EDA Playground | RTL simulation |
| Icarus Verilog | Functional simulation engine, when selected |
| EPWave | Waveform inspection |
| Linux/Ubuntu | Development environment |
| Yosys | Logic synthesis |
| OpenROAD | Physical design |
| OpenLane | RTL-to-GDS implementation flow |
| SKY130 PDK | Standard-cell and technology data |
| KLayout | Layout visualization and inspection |
| Git and GitHub | Version control and project hosting |

## 9. Repository Structure

```text
Vending-Machine-RTL-to-GDS/
├── docs/
├── rtl/
├── testbench/
├── simulation/
├── constraints/
├── synthesis/
├── physical_design/
├── results/
├── layout/
├── images/
└── README.md
```

## 10. RTL Implementation

The main Verilog source file is:

`rtl/vending_machine.v`

The module defines the vending machine inputs, outputs, state register, next-state logic, and control logic.

The testbench is available at:

`testbench/vending_machine_tb.v`

## 11. Functional Simulation

The RTL is simulated using EDA Playground.

The testbench applies reset and coin inputs to verify the intended payment sequences and output behavior.

Simulation evidence is available in:

`simulation/screenshots/`

The screenshots should include the RTL code, testbench, simulation output, and waveform.

## 12. Logic Synthesis

Logic synthesis is performed using Yosys.

The synthesis stage converts the RTL description into a gate-level netlist using the selected target technology and synthesis settings.

The generated netlist and synthesis reports are stored in:

`synthesis/netlist/`

`synthesis/reports/`

## 13. Physical Design

The synthesized design is implemented using OpenROAD/OpenLane.

The physical design process includes:

- Floorplanning
- Power distribution network implementation
- Standard-cell placement
- Clock tree synthesis
- Global and detailed routing
- Timing analysis
- Design-rule verification
- Final layout generation

Implementation reports and screenshots are stored in:

`physical_design/`

The exact stages depend on the flow configuration and the checks supported by the selected toolchain.

## 14. Results

The final results will be documented after the implementation flow completes.

| Metric | Result |
|---|---|
| Synthesis status | To be measured |
| Standard-cell area | To be measured |
| Core area | To be measured |
| Die area | To be measured |
| Clock period | To be specified |
| Worst Negative Slack (WNS) | To be measured |
| Total Negative Slack (TNS) | To be measured |
| Power estimate | To be measured, if available |
| DRC status | To be verified |
| LVS status | To be verified |
| GDSII generation | To be verified |

All reported metrics should be taken from the actual tool-generated reports.

## 15. Final Layout

The final physical layout is generated in GDSII format when the implementation flow completes successfully.

The layout can be inspected using KLayout.

A screenshot of the completed layout will be added below.

![Final Chip Layout](physical_design/screenshots/05_final_layout.png)

## 16. How to Reproduce the Project

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Vending-Machine-RTL-to-GDS.git
cd Vending-Machine-RTL-to-GDS
```

Replace `YOUR_USERNAME` with the actual GitHub username.

### Step 2: Run RTL simulation

Open the RTL and testbench in EDA Playground, select the appropriate Verilog simulator, and run the testbench.

### Step 3: Run synthesis

Install and configure Yosys, the target PDK, and the required technology libraries. Run the synthesis script provided in the repository.

### Step 4: Run physical implementation

Install the required OpenROAD/OpenLane environment and use the documented configuration to run the physical design flow.

### Step 5: Inspect results

Review the generated netlist, implementation reports, and physical layout.

The exact commands and configuration will be documented in the corresponding folders.

## 17. Future Improvements

- Add product selection.
- Support multiple product prices.
- Add quantity selection.
- Introduce cash and UPI payment modes.
- Improve payment validation.
- Add additional FSM states.
- Optimize the RTL for area and timing.
- Compare synthesis and physical implementation results.

## 18. References

- EDA Playground: https://www.edaplayground.com/
- Yosys: https://github.com/YosysHQ/yosys
- OpenROAD: https://github.com/The-OpenROAD-Project/OpenROAD
- OpenLane: https://github.com/efabless/openlane
- SkyWater SKY130 PDK: https://github.com/google/skywater-pdk
- KLayout: https://www.klayout.de/

---

**Project:** Vending Machine — RTL-to-GDS Implementation  
**Design Language:** Verilog HDL  
**Implementation:** Open-source EDA tools
