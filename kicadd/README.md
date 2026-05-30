# KiCad PCB Design

## Overview

This folder contains the complete PCB implementation of the 12V to 5V buck converter designed around the LM2596S-5 switching regulator.

## Design Objectives

- Convert 12V DC input to regulated 5V DC output
- Implement a compact PCB layout
- Minimize routing complexity
- Use a ground plane for improved return current paths
- Generate fabrication-ready manufacturing files

## Components

| Reference | Component |
|------------|------------|
| U1 | LM2596S-5 |
| D1 | SS34 Schottky Diode |
| L1 | 68uH Inductor |
| C1 | 330uF Output Capacitor |
| C2 | 100uF Input Capacitor |
| J1 | Input Connector |
| J2 | Output Connector |

## PCB Design Process

1. Imported schematic from KiCad schematic editor
2. Assigned footprints to all components
3. Performed PCB placement
4. Routed all electrical connections
5. Added copper ground plane
6. Verified design using DRC
7. Generated Gerber manufacturing files

## Design Verification

The final design passed Design Rule Check (DRC) with:

- 0 Errors
- 0 Unconnected Nets

## Files

### Schematic

schematic.png

### PCB Routing

pcb-routing.png

### Ground Plane

pcb-ground-plane.png

### DRC Verification

drc-clean.png

## Software

- KiCad 9
