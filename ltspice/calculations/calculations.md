# Buck Converter Design Calculations

## Specifications

| Parameter | Value |
|------------|--------|
| Input Voltage | 12 V |
| Output Voltage | 5 V |
| Output Capacitor | 330 uF |
| Input Capacitor | 100 uF |
| Inductor | 68 uH |
| Switching Frequency | 150 kHz |
| Load Resistance | 10 Ohms |

---

## Duty Cycle

For an ideal buck converter:

D = Vout / Vin

D = 5 / 12

D = 0.417

Duty Cycle = 41.7%

---

## Output Current

Using Ohm's Law:

Iout = Vout / Rload

Iout = 5 / 10

Iout = 0.5 A

---

## Output Power

Pout = Vout × Iout

Pout = 5 × 0.5

Pout = 2.5 W

---

## Inductor Ripple Current

Using:

ΔIL = ((Vin − Vout) × D) / (L × fsw)

Where:

Vin = 12 V

Vout = 5 V

D = 0.417

L = 68 uH

fsw = 150 kHz

Substituting:

ΔIL = ((12 − 5) × 0.417) / (68e−6 × 150000)

ΔIL ≈ 0.286 A

Inductor Ripple Current = 286 mA

---

## Peak Inductor Current

IL_peak = Iout + ΔIL/2

IL_peak = 0.5 + 0.286/2

IL_peak = 0.643 A

Peak Inductor Current = 643 mA

---

## Estimated Output Voltage Ripple

Assuming ideal capacitor:

ΔVout = ΔIL / (8 × fsw × Cout)

Where:

ΔIL = 0.286 A

fsw = 150 kHz

Cout = 330 uF

Substituting:

ΔVout = 0.286 / (8 × 150000 × 330e−6)

ΔVout ≈ 0.00072 V

ΔVout ≈ 0.72 mV

Actual ripple will be larger due to capacitor ESR.

---

## Component Selection

### LM2596S-5

Fixed 5 V switching regulator operating at approximately 150 kHz.

### SS34 Schottky Diode

Selected for low forward voltage drop and fast switching characteristics.

### 68 uH Inductor

Chosen to maintain continuous current operation and reduce ripple current.

### 100 uF Input Capacitor

Reduces input voltage ripple and supplies switching current pulses.

### 330 uF Output Capacitor

Reduces output voltage ripple and improves load transient response.

---

## Design Summary

The converter was designed to step down a 12 V DC input to a regulated 5 V output using the LM2596S-5 switching regulator.

Key performance values:

- Input Voltage: 12 V
- Output Voltage: 5 V
- Output Current: 0.5 A
- Output Power: 2.5 W
- Duty Cycle: 41.7 %
- Ripple Current: 286 mA
- Peak Inductor Current: 643 mA
- Estimated Output Ripple: 0.72 mV

The design was verified through LTspice simulation and implemented as a PCB layout using KiCad.
