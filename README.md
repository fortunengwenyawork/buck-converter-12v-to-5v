# 12V to 5V Buck Converter

## Overview

This project documents the complete design workflow of a 12V to 5V DC-DC buck converter using the LM2596S-5 switching regulator.

The project includes:

- Circuit design and component selection
- LTspice simulation and verification
- Ripple and transient analysis
- KiCad schematic capture
- PCB layout and routing
- Ground plane implementation
- Design Rule Check (DRC) verification
- Gerber file generation for manufacturing

The objective was to gain practical experience with power electronics design and PCB development while following a professional engineering workflow.

---

## Specifications

| Parameter | Value |
|------------|------------|
| Input Voltage | 12 V |
| Output Voltage | 5 V |
| Target Output Current | 2 A |
| Switching Frequency | 500 kHz |
| Controller IC | LM2596S-5 |
| Diode | SS34 Schottky |
| Inductor | 68 µH |
| Input Capacitor | 100 µF |
| Output Capacitor | 330 µF |

---

## Design Calculations

### Duty Cycle

For an ideal buck converter:

D = Vout / Vin

D = 5 / 12

D = 0.417

Duty Cycle ≈ 41.7%

### Output Power

Pout = Vout × Iout

Pout = 5 × 2

Pout = 10 W

### Load Resistance

Rload = Vout / Iout

Rload = 5 / 2

Rload = 2.5 Ω

---

## LTspice Simulation

The converter was modeled and simulated in LTspice to verify operation before PCB design.

### Analyses Performed

- Startup transient response
- Output voltage ripple
- Inductor current ripple
- Inductor startup behavior
- Switch node voltage waveform

Simulation screenshots are available in:

```text
docs/
ltspice/
```

---

## PCB Design

The circuit was transferred to KiCad for schematic capture and PCB implementation.

### PCB Features

- Single-sided routing
- Ground plane implementation
- Power trace routing
- LM2596S-5 footprint integration
- Through-hole connectors
- DRC verified layout

### Design Verification

The PCB successfully passed KiCad Design Rule Check (DRC) verification with no critical errors.

---

## Manufacturing Outputs

Gerber files were generated from the completed PCB layout.

Generated files include:

- Front Copper
- Back Copper
- Front Solder Mask
- Back Solder Mask
- Front Paste
- Back Paste
- Front Silkscreen
- Back Silkscreen
- Board Outline
- Gerber Job File

These files are located in:

```text
gerbers/
```

---

## Project Status

### Completed

- [x] Component selection
- [x] LTspice schematic creation
- [x] Startup transient analysis
- [x] Output ripple analysis
- [x] Inductor current analysis
- [x] Switch node verification
- [x] KiCad schematic capture
- [x] PCB layout and routing
- [x] Ground plane implementation
- [x] Design Rule Check verification
- [x] Gerber generation
- [x] Documentation

Status: Complete

---

## Repository Structure

```text
buck-converter-12v-to-5v/
│
├── docs/
│   ├── project_overview.md
│   ├── buck_converter_ltspice_schematic.png
│   ├── startup_response.png
│   ├── output_ripple.png
│   ├── switch_node_voltage.png
│   ├── inductor_current_ripple.png
│   ├── inductor_current_startup.png
│   ├── pcb_schematic.png
│   ├── pcb_routing_with_ground_pour.png
│   ├── pcb_ground_plane.png
│   ├── drc_clean.png
│   └── project_report.md
│
├── ltspice/
│   ├── buck_converter.asc
│   ├── calculations.md
│   └── README.md
│
├── kicad/
│   ├── buck_converter.kicad_sch
│   ├── buck_converter.kicad_pcb
│   ├── buck_converter.kicad_pro
│   └── README.md
│
├── gerbers/
│   ├── README.md
│   ├── *.gbr
│   └── default-job.gbrjob
│
├── LICENSE
└── README.md
```

---

## Learning Outcomes

Through this project I gained experience with:

- Switching power supply fundamentals
- Buck converter operation
- LTspice simulation workflows
- Ripple analysis techniques
- PCB schematic capture
- PCB layout and routing
- Ground plane design
- Design Rule Checking
- Gerber generation
- Engineering documentation

---

## Future Improvements

Potential future enhancements include:

- PCB fabrication and testing
- Thermal analysis
- Efficiency measurements
- EMI optimization
- Higher current versions
- Synchronous buck topology

---

## Author

Fortune Ngwenya

Electrical Engineering Student and professional.

---

## License

This project is released under the MIT License.
