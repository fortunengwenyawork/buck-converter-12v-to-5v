# Gerber Files

## Overview

This folder contains the Gerber manufacturing files generated from the KiCad PCB layout of a 12V to 5V buck converter using the LM2596S-5 switching regulator.

These files can be sent directly to a PCB fabrication service for manufacturing.

## Generated Files

| File | Description |
|--------|------------|
| default-F_Cu.gbr | Front copper layer |
| default-B_Cu.gbr | Back copper layer |
| default-F_Mask.gbr | Front solder mask |
| default-B_Mask.gbr | Back solder mask |
| default-F_Paste.gbr | Front paste layer |
| default-B_Paste.gbr | Back paste layer |
| default-F_Silkscreen.gbr | Front silkscreen |
| default-B_Silkscreen.gbr | Back silkscreen |
| default-Edge_Cuts.gbr | PCB outline |
| default-job.gbrjob | Gerber job definition |

## PCB Specifications

- Input Voltage: 12 V DC
- Output Voltage: 5 V DC
- Converter Type: Buck Converter
- Controller IC: LM2596S-5
- Inductor: 68 µH
- Input Capacitor: 100 µF
- Output Capacitor: 330 µF
- Schottky Diode: SS34

## Design Workflow

1. LTspice circuit simulation
2. Component selection and calculations
3. KiCad schematic capture
4. PCB layout and routing
5. Ground plane implementation
6. Design Rule Check (DRC)
7. Gerber generation

## Verification

The PCB layout completed Design Rule Check (DRC) verification with no critical errors before Gerber generation.

## Project Purpose

This project demonstrates the complete workflow for designing a switch-mode DC-DC power converter from simulation through PCB layout and manufacturing output generation.
