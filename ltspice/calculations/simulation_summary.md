# Simulation Summary

## Design Targets

- Input Voltage: 12 V
- Target Output Voltage: 5 V
- Load Resistance: 2.5 Ω
- Switching Frequency: 500 kHz
- Inductor: 10 µH
- Output Capacitor: 47 µF

## Simulation Results

### Output Voltage

Steady-state output voltage measured approximately 4.73 V.

### Switch Node Voltage

Switch node toggled between approximately +12 V and -1 V.

### Inductor Current

Average inductor current approximately 1.9 A.

Measured ripple current approximately 0.6 A peak-to-peak.

### Output Ripple

Output ripple observed to be on the order of several millivolts.

## Observations

The converter successfully stepped down the 12 V input to approximately 5 V output.

Waveforms matched expected buck converter behavior including:

- Startup transient response
- Square-wave switch-node voltage
- Triangular inductor current
- Low output voltage ripple

The simulation verified proper operation of the converter before PCB implementation.
