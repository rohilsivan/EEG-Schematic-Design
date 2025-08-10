# EEG Schematic Design – Cadence Virtuoso  
   Analog EEG Sensor Project

---

## 📌 Overview

This repository contains the **complete design documentation**, **schematics**, **simulation results**, and **analysis** for an **analog EEG sensor** designed using **Cadence Virtuoso**.  
The project focuses on delivering a **low-cost**, **high-sensitivity**, and **low-noise** EEG front-end for **brain-computer interface (BCI)** and **diagnostic** applications.

All resources in this repository support **hands-on IC design, simulation, and layout implementation**.


---

## 🎯 Project Aim

To design and implement a **cost-effective**, **high-sensitivity**, and **low-noise** analog EEG sensor for **accurate brain signal acquisition**, optimized for **BCI integration** and ready for **IC layout tape-out** in Cadence Virtuoso.

---

## 🛠 System Architecture

The EEG front-end circuit consists of:

- **Instrumentation Amplifier**  
  - High **CMRR**, adjustable gain, differential measurement.  
  - Two-stage: input buffering + difference amplification.  
  - Gain ≈ **52 dB**, bandwidth **1–100 Hz**.

- **Bandpass Filter (Sallen-Key)**  
  - Passes **1–100 Hz** range, preserving brainwave signals.  
  - Gain ≈ **37 dB**, 2nd-order active filter.

- **50 Hz Notch Filter (Twin-T)**  
  - Suppresses mains interference at **50 Hz**.  
  - High Q-factor (~100) for sharp rejection.

- **CMOS Two-Stage Operational Amplifier**  
  - Differential input, gain stage, frequency compensation.  
  - Gain ≈ **70 dB**, phase margin ≈ **60°**, 180 nm technology.

- **Data Acquisition**  
  - Output ready for **ADC** and oscilloscope capture.  
  - Simulations confirm real-time waveform fidelity.

---

## 📊 Simulation & Testing

- **Cadence Virtuoso**  
  - AC & transient analysis for **block-level** and **system-level** verification.  
  - Tests cover gain, phase, bandwidth, and stability.

- **MATLAB**  
  - Synthetic EEG signals for validation.  
  - Enables controlled benchmarking of the sensor design.

---

## 🔍 Key Results

| Block                  | Gain (dB) | Bandwidth (Hz) | Phase Margin (°) | Notes                    |
|------------------------|-----------|----------------|------------------|--------------------------|
| OpAmp (CMOS 2-stage)   | ~70       | 1–100          | ~60              | Stable, low power        |
| Instrumentation Amp    | ~52       | 1–100          | ~45              | High CMRR                |
| Bandpass Filter        | ~37       | 1–100          | —                | Sallen-Key topology      |
| Notch Filter           | —         | 50 (notch)     | —                | Twin-T, deep rejection   |
| System (Front-end)     | Up to 110 | 1–100          | —                | Verified via simulations |

---

## 🚀 Usage

1. Explore simulation results and schematics in `eeg_screenshots/` and `eeg_100_dbgain/`.
2. Review **`Presentation.pdf`** for:
   - Project introduction
   - Literature survey
   - Block diagrams
   - Complete results and references
3. Recreate circuits in **Cadence Virtuoso** using the provided specs.

---

## ⚠ Legal & Research Notes

- **For academic/research use only** – *not validated for clinical/medical use*.  
- Review `LICENSE` for reuse permissions.  
- Clinical adaptation requires compliance with medical data regulations.

---

## 📚 References

Complete bibliography is included in **`Presentation.pdf`**.

---

**Thank you for exploring the EEG Project!**  
For questions or collaboration, reach out via this repository’s Issues page.


