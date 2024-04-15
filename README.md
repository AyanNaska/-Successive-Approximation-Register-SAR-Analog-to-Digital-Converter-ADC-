# -Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC
## Introduction
A Successive Approximation Register (SAR) Analog-to-Digital Converter (ADC) is a type of ADC that is widely used in modern electronics in applications that require high-speed, high-resolution, and low-power ADCs, such as in wireless communication systems, image sensors, and biomedical devices. Additionally, SAR ADCs are known for their low complexity and ease of implementation, making them a popular choice in many electronics applications.

## Working
The analog input voltage (VIN) is held on a track/hold. If VIN is greater than VDAC, the comparator output is a logic high, or 1, and the MSB of the N-bit register remains at 1. Conversely, if VIN is less than VDAC, the comparator output is a logic low and the MSB of the register is cleared to logic 0.
The SAR control logic then moves to the next bit down, forces that bit high, and does another comparison. The sequence continues all the way down to the LSB. Once this is done, the conversion is complete and the N-bit digital word is available in the register.

## Block Diagram

## Circuits in Cadence
### 1.Sample and Hold
The sample-and-hold circuit samples the analog input signal and holds its voltage constant during the conversion process.

### 2.Comparator
Compares the sampled analog input voltage to the output voltage of the DAC.

### 3.SAR
Successive approximation register (SAR):
The SAR is a shift register that stores the bits of the digital output code of the ADC.

### 4.DAC
The DAC converts the digital output of the SAR into an analog voltage that is compared to the input voltage by the comparator.
