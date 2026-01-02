# Analog PWM Signal Generator (LTSpice)

**Period:** 01/04/2022 – 17/05/2022  
**Tools:** LTSpice

Analog PWM generator designed in **LTSpice**, based on comparing a triangular carrier waveform with a DC reference signal.  
Duty cycle and output amplitude are adjustable through voltage divider networks and a Class B output stage for load driving.

---

## Core Features
- **Triangular wave generator** at ~12 kHz (frequency set by R/C network)
- **Comparator-based PWM** generation from DC reference input
- **Duty cycle adjustment:** approx. 10% → 50%
- **Amplitude control:** approx. 3V → 5V
- **Class B amplifier** on output for load independence
- **Tolerance validation:** Monte Carlo analysis
- **FFT analysis** confirming rectangular spectrum structure

---

## Circuit Blocks
- **Triangular carrier generator** (RC-calculated time constant)
- **Reference signal input** for duty cycle control
- **High-speed comparator** for switching action
- **Class B output** (transistor pair + global feedback)

---

## Simulation Highlights
- **Transient analysis** to verify switching and waveform shape
- **Parametric sweep** on reference voltage (duty cycle response)
- **Monte Carlo** tolerance sweep → stable output range (≈4.94V–5.07V)
- **FFT analysis** → central peak at ~12 kHz, harmonics following sinc envelope

---

## Repository Structure
| File | Description |
|------|-------------|
| `PWM Generator.pdf` | Project report and technical documentation |
| `PWM Generator.pptx` | Project presentation slides |
| `Triangular_signal.asc` | LTspice schematic for triangular signal generation |
| `Triangular_signal.plt` | LTspice plot configuration |
| `Triangular_signal.fft` | FFT analysis results of the generated signal |
| `Triangular_signal.log` | LTspice simulation log |
| `Triangular_signal.log.raw` | Transient simulation raw data |
| `Triangular_signal.op.raw` | Operating point analysis data |
