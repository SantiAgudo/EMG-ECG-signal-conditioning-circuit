# EMG-ECG Signal Conditioning Circuit

## Overview

This project presents the design and implementation of a biomedical signal conditioning circuit for **electromyography (EMG)** and **electrocardiography (ECG)** signals.  

The circuit is designed to acquire low-amplitude biological signals and prepare them for further processing in biomedical systems such as:

- Prosthetic limb control
- Biomedical signal analysis
- Rehabilitation devices
- Human–machine interfaces

The design focuses on improving signal quality while considering **morphophysiological variations among individuals**.

---

## System Architecture

ECG / EMG Electrodes  
→ Instrumentation Amplifier  
→ Bandpass Filtering  
→ Gain Adjustment  
→ Notch Filter (Powerline Noise Removal)  
→ High-Pass Filter  
→ Output Signal for Microcontroller Processing

---

## Circuit Components

The signal conditioning circuit includes several stages:

### Instrumentation Amplifier

An **INA128 instrumentation amplifier** is used for differential amplification of the EMG-ECG signals.

Features:
- High input impedance
- Low noise
- High common-mode rejection ratio

---

### Filtering Stages

To improve signal quality, multiple filtering stages are implemented:

- **Low-pass filter** → removes high-frequency noise
- **High-pass filter** → removes baseline drift
- **Notch filter** → removes powerline interference (50/60 Hz)

---

### Gain Adjustment

A variable gain amplifier based on a **TL072 operational amplifier** allows manual calibration using a potentiometer.

This enables adaptation to different subjects and morphophysiological conditions.

---

### Signal Level Adjustment

A zero-span circuit is used to adjust the DC offset of the signal to ensure compatibility with microcontroller input ranges.

---

## PCB Design

The circuit was implemented on a printed circuit board (PCB) optimized for:

- low noise
- compact layout
- reliable signal acquisition

![PCB Design](images/pcb_design.png)

---

## Experimental Results

The circuit was tested with ECG electrodes connected to a healthy subject.

The output signal showed clean waveform characteristics suitable for digital processing.

![ECG Signal](images/ecg_signal_test.png)

The maximum measured signal voltage was approximately **2.16V**, which is compatible with typical **3.3V microcontroller inputs**.

---

## Applications

This signal conditioning system can be integrated into:

- EMG-controlled prosthetic limbs
- wearable biomedical monitoring systems
- human-machine interfaces
- rehabilitation technologies

---

## Paper

The full research paper describing this work is available here:

📄 [Read the paper](paper/emg_ecg_signal_conditioning_circuit.pdf)

---

## Technologies Used

- Analog electronics
- Instrumentation amplifiers
- Operational amplifiers
- PCB design
- Biomedical signal processing

---

## Author

**Santiago Agudo Muñoz**  
Electronic Engineer – Biomedical Engineering Focus

---

## License

This project is intended for research and educational purposes.
