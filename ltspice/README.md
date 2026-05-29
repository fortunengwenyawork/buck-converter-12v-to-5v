# LTspice Simulation

This folder contains the LTspice schematic, simulation source file, waveform captures, and supporting calculations for the 12 V to 5 V buck converter project.

## Contents

### Design Files
- buck_converter.asc
- buck_converter_schematic.png

### Waveform Results
- startup_response.png
- switch_node_voltage.png
- output_ripple.png
- inductor_current_startup.png
- inductor_current_ripple.png

### Calculations
- calculations/simulation_summary.md

## Key Results

| Parameter | Value |
|------------|---------|
| Input Voltage | 12 V |
| Output Voltage | 4.73 V |
| Load Resistance | 2.5 Ω |
| Switching Frequency | 500 kHz |
| Inductor | 10 µH |
| Output Capacitor | 47 µF |

## Description of Waveforms

### Startup Response
Shows converter startup transient and settling behavior.

### Switch Node Voltage
Shows the PWM switching action between approximately +12 V and -1 V.

### Output Ripple
Shows steady-state output voltage ripple in the millivolt range.

### Inductor Current Startup
Shows inductor current during startup and transient settling.

### Inductor Current Ripple
Shows steady-state triangular inductor current ripple.

The simulated converter successfully stepped down the 12 V input to approximately 5 V while maintaining low output ripple and stable inductor current operation.
