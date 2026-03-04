# BJT Amplifier: Operating Point & Frequency Analysis
<img width="1296" height="562" alt="Zrzut ekranu 2026-03-04 155905" src="https://github.com/user-attachments/assets/5629e664-8e4e-4e11-8004-8a35086d4ced" />
<img width="1602" height="778" alt="Zrzut ekranu 2026-03-04 155652" src="https://github.com/user-attachments/assets/8c450e73-54d0-4355-8293-c17ca4da94a2" />



![d33045a0-7aa6-4be8-b0a9-dd033310051d](https://github.com/user-attachments/assets/1cab14b0-3f5a-43b2-aa29-f078655965fe)

## 1. DC Biasing and Voltage Gain

The operating point (Q-point) of the BJT amplifier is defined by the resistor network.
Resistors R_C and R_E determine the transistor's load line and signal amplification.

### Voltage Gain (Common Emitter)

Approximate voltage gain for a Common Emitter configuration:

A_V ≈ - R_C / R_E

Where:
- R_C – Collector resistor (collector biasing, higher value increases gain)
- R_E – Emitter resistor (thermal stability, negative feedback)

---

## 2. Coupling and Lower Cutoff Frequency

The input coupling capacitor C_1 provides DC isolation and defines the low-frequency behavior.

### Function
- Blocks DC components from the signal source
- Allows AC signals to pass

### Filter Behavior

C_1 forms a high-pass filter with the base input impedance.

### Lower Cutoff Frequency

Design condition:

f_filter < f_d

Where:
- f_filter – cutoff frequency of the input high-pass filter
- f_d – lower cutoff frequency of the amplifier

---

## 3. Frequency Response Parameters

The amplifier frequency response is divided into:
- Low-frequency region
- Mid-band region
- High-frequency region

### Key Parameters

Mid-band Gain (K_u0):
Maximum stable voltage gain

Lower Cutoff Frequency (f_d):
Frequency where gain drops by 3 dB

Upper Cutoff Frequency (f_g):
Frequency where gain drops by 3 dB

Bandwidth (B):
B = f_g - f_d

---

## Summary

This document describes:
- DC biasing and operating point (Q-point)
- Voltage gain estimation for a CE BJT amplifier
- Influence of coupling capacitor on low-frequency response
- Definition of frequency response parameters and bandwidth
