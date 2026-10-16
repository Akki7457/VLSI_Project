# FSM Smart Traffic Light Controller

A Verilog HDL-based Smart Traffic Light Controller using a Finite State Machine (FSM) architecture.

## Project Overview

This project focuses on designing a digital traffic-light controller that manages vehicle signals at an intersection using sequential logic, state transitions, timing control, and reset handling.

The architecture is intended to support modular design, simulation-based verification, and future enhancements for pedestrian requests, green-wave coordination, and emergency overrides.

## Objectives

- Design an FSM-based traffic signal controller using Verilog HDL.
- Define safe and predictable traffic-light state transitions.
- Implement timer-based transitions between signal phases.
- Develop modular RTL and testbenches.
- Verify the design through simulation waveforms and test results.
- Document the design for future FPGA or ASIC implementation.

## Intended Architecture

The planned architecture includes:

- **Top-Level Controller:** Integrates the traffic-control modules.
- **Junction Controllers:** Manage signal sequences for the intersection.
- **Generic Timer:** Provides timing information for phase transitions.
- **Pedestrian Arbiter:** Coordinates pedestrian requests when implemented.
- **Green-Wave Coordination:** Supports coordinated signal timing when implemented.
- **Emergency Override:** Supports emergency-related signal control when implemented.
- **Clock and Reset Logic:** Establishes the design's timing and initialization behavior.

The final implemented architecture must be confirmed against the actual RTL source code.

## FSM States

The planned vehicle-signal sequence includes:

| State | Purpose |
|---|---|
| `NS_GREEN` | North–South traffic receives a green signal |
| `NS_YELLOW` | North–South traffic receives a yellow signal |
| `ALL_RED` | All vehicle directions are held red during the transition |
| `EW_GREEN` | East–West traffic receives a green signal |
| `EW_YELLOW` | East–West traffic receives a yellow signal |

The implemented state transitions and timing must be checked against the RTL and simulation results.

## Technology Stack

- **Hardware Description Language:** Verilog HDL
- **Simulation:** ModelSim or a compatible Verilog simulator
- **Version Control:** Git
- **Repository Hosting:** GitHub
- **Code Editor:** Visual Studio Code

## Repository Structure

The intended source organization is:

```text
VLSI_Project/
├── README.md
├── rtl/
│   ├── traffic_controller.v
│   └── generic_timer.v
├── tb/
│   ├── tb_traffic_controller.v
│   └── tb_generic_timer.v
├── docs/
│   ├── architecture.md
│   └── verification_plan.md
├── diagrams/
└── results/
    └── waveforms/
```

These are suggested filenames and folders. The final structure should match the actual modules and testbenches included in the repository.

## Verification Plan

The following checks are planned:

1. Reset and initial-state behavior.
2. Correct FSM state transitions.
3. Timer expiration and phase duration.
4. Safe transitions between traffic directions.
5. Pedestrian and emergency behavior, if implemented.
6. Compilation and simulation of the relevant testbenches.

Verification status should be updated only after the corresponding tests have been run.

## How to Simulate

1. Open the project in ModelSim.
2. Compile the RTL files.
3. Compile the relevant testbench.
4. Run the simulation.
5. Inspect the state, timer, and traffic-light outputs.
6. Save waveform screenshots and record the test results.

Exact commands depend on the filenames and simulator setup.

## Current Project Status

- [x] Git repository created and pushed to GitHub.
- [ ] RTL files organized into a dedicated source directory.
- [ ] Testbenches compiled and executed.
- [ ] FSM transitions verified.
- [ ] Waveforms captured and reviewed.
- [ ] Verification results documented.

## Future Enhancements

- Pedestrian-request handling.
- Emergency-vehicle priority.
- Green-wave coordination between junctions.
- Parameterized signal timing.
- FPGA implementation and hardware testing.

## Author

**Aakash Rayal**

GitHub: [Akki7457](https://github.com/Akki7457)

---

*This README describes the project goals and intended design. Implementation details and verification claims must be updated to reflect the actual RTL, testbench results, and hardware tests.*
