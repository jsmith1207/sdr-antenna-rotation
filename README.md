SDR Antenna Rotation Measurement System
Overview

This project implements a Software-Defined Radio (SDR) signal transmission and antenna rotation system to measure received power as a function of angle. The goal is to characterize antenna radiation patterns and analyze signal propagation using real-world hardware.

This system integrates:

GNU Radio signal generation

SDR hardware transmission (LimeSDR Mini)

Ham radio signal reception

Stepper-motor-controlled antenna rotation

Python-based received power analysis

Objectives

Generate NBFM test beacon using GNU Radio

Transmit RF signal via SDR

Rotate receiving antenna using stepper motor

Record received signal strength vs angle

Construct radiation pattern visualization

Compare measured data to theoretical models (Friis Transmission Equation)

System Architecture

Signal Source → GNU Radio Modulation → SDR Transmitter → RF Propagation → Rotating Antenna → Receiver → Power Measurement → Python Analysis

Hardware

LimeSDR Mini

Ham Radio Receiver

28BYJ-48 Stepper Motor

ULN2003 Driver Module

Arduino (motor control)

Directional antenna

Software Stack

GNU Radio

SoapySDR

Python (NumPy, Matplotlib)

Arduino IDE

Current Status

✔ NBFM signal generation in GNU Radio
✔ SDR configuration via SoapySDR
⏳ Antenna rotation apparatus integration
⏳ Automated received power logging
⏳ Radiation pattern plotting

Future Work

Implement automated angle stepping + synchronized logging

Add theoretical vs measured comparison plots

Integrate polar radiation pattern visualization

Evaluate SNR vs angle
