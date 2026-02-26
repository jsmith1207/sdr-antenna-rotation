# SDR-Based Antenna Radiation Pattern Measurement System

## Project Summary

This project develops a Software-Defined Radio (SDR) based experimental platform for measuring received power as a function of antenna orientation.

The objective is to characterize antenna radiation patterns through controlled transmission, mechanical rotation, and digital power measurement.

The system integrates RF theory, SDR modulation, embedded motor control, and signal processing.

---

## System Architecture

Transmitter Chain:
Baseband Signal Generation → Complex Modulation → LimeSDR Upconversion → RF Radiation

Receiver Chain:
RF Reception → LimeSDR Downconversion → IQ Sampling → Power Estimation → Data Logging

Mechanical Subsystem:
Stepper Motor Rotation → Angular Position Control → Synchronized Measurement

---

## Signal Generation

Signal generation is performed in GNU Radio.

- Complex baseband signal generation
- Controlled frequency placement relative to RF center frequency
- Narrowband test tone for controlled bandwidth
- Configurable transmit gain

The LimeSDR performs hardware upconversion to the selected RF carrier frequency.

---

## Power Measurement Method

Received power is computed digitally from complex IQ samples:

P = mean(|I + jQ|²)

Converted to relative dB:

P_dB = 10 log10(P)

Initial validation uses relative power measurement. Future work includes calibration to approximate absolute dBm.

---

## Theoretical Basis

Radiation behavior is analyzed using the Friis Transmission Equation:

Pr = Pt Gt Gr (λ / (4πR))²

Where:
- Pt = transmitted power
- Gt = transmit antenna gain
- Gr = receive antenna gain
- R = separation distance
- λ = wavelength

Measurements will be compared against theoretical predictions to evaluate system behavior.

---

## Hardware

- LimeSDR-USB (full-size)
- Dual-band VHF/UHF antennas
- Stepper motor (28BYJ-48)
- ULN2003 driver module
- Arduino-based rotation control

---

## Development Status

✔ SDR transmission and reception validation  
✔ Digital power estimation pipeline  
⏳ Mechanical rotation integration  
⏳ Automated data logging  
⏳ Polar radiation pattern plotting  

---

## Engineering Objectives

- Establish controlled RF link
- Prevent receiver front-end overload
- Maintain repeatable measurement conditions
- Quantify directional gain variation
- Develop synchronized angle vs power dataset

---

## Long-Term Goals

- Full automation of measurement cycle
- Absolute power calibration
- Comparison of measured vs theoretical radiation patterns
- Extension toward radar and RF sensing applications
- Complete function open-source system