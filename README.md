# SIMPLE_EEG_VERSION_0

## Author
Aditya Sharma

## Introduction
This project involves the creation of an EEG system using an Arduino UNO and various operational amplifiers for brain wave amplification and noise filtering. The project was inspired by a 12-step DIY EEG/ECG instructable.

## Components Used
- Operational amplifiers: TL084CN, A620AN
- EEG electrodes
- Capacitors and resistors
- Arduino UNO R3

## Design
The EEG system was designed with a high pass filter of 7 Hz for alpha waves and a low pass filter of 31 Hz. A notch filter of 60 Hz was initially used, but it turned out to be problematic as the real interference was at 50 Hz, causing significant errors.

## Data Acquisition
Data was collected using the ADC of an Arduino UNO R3, with the ATmega 328P chip's internal 1.1V used for analog reference.

## Signal Processing
The main challenge of the project was signal processing. The code provided in the instructable had deprecated libraries of the processing language. To overcome this, I had to learn about Fast Fourier Transform (FFT). After writing a sample code in Python, it didn't work properly with the Matplotlib library due to a significant delay in data received after signal processing. I then used the FFT code in Arduino itself from the YouTube channel Curio Res. The code worked fine, but I later shifted to a serial analyzer app, which made things much easier.

## Issues and Solutions
The main problem of the project was the incorrect notch filter. The new notch filter of 50 Hz had designs with resistors that were not easily available.

## Contact
For any queries, you can reach out to me at adduabbu2005sharma@gmail.com
