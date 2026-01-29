# Triangle and Square Wave Generator (Op-Amp)

<img width="1156" height="487" alt="Zrzut ekranu 2026-01-29 195136" src="https://github.com/user-attachments/assets/6fcfa7b2-685d-4619-8292-0cd3bde1c2ce" />
<img width="1291" height="468" alt="Zrzut ekranu 2026-01-29 195050" src="https://github.com/user-attachments/assets/585cff87-2634-4001-ae08-587b8626934b" />



## System Architecture

The generator consists of two functional blocks:

### Schmitt Trigger (W1)
A non-inverting comparator that generates a **square wave output**:

### Integrator (W2)
An active integrating circuit that converts the square wave into a **triangle wave** by charging and discharging capacitor C with a constant current.

![61d9e96a-408f-43d2-95c9-b301cc2c364c](https://github.com/user-attachments/assets/cc25892e-319a-4ece-8263-d73e952ce01f)


## Mathematical Model

The oscillation period and output characteristics are defined by the following equations.

### 1. Oscillation Period (T)

The total period of the generated waveforms depends on the RC constant and the feedback resistor ratio:

T = 4 * R * C * (R1 / R2)



### 2. Triangle Wave Amplitude (U2m)

The peak voltage of the triangle wave depends on the square wave amplitude (U1m) and the resistor ratio:

U_2m = (R1 / R2) * U_1m



### 3. Integrator Output Voltage (u2)

The output of the second stage is the integral of the square wave:

u_2(t) = u_2(0) - (1 / (R * C)) * ∫_0^t u_1(t) dt



## Operating Requirements and Regulation

### Frequency Control
The frequency is adjusted by varying the resistance **R** or the capacitance **C**.

### Amplitude Control
- Square wave amplitude is limited by the supply voltage.
- Triangle wave amplitude is controlled by the resistor ratio **R1 / R2**.

### Stability Condition
To ensure proper switching of the Schmitt trigger, the following resistor condition must be met:

R2 > R1

## Waveform Characteristics

- **Output u1:** Square wave with amplitude ±U1m  
- **Output u2:** Triangle wave with amplitude ±U2m  
- **Phase:** The integrator introduces a phase relationship where the slopes of the triangle wave correspond to the constant voltage levels of the square wave
