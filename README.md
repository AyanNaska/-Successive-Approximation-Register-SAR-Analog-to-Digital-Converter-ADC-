# -Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC
## Introduction
A Successive Approximation Register (SAR) Analog-to-Digital Converter (ADC) is a type of ADC that is widely used in modern electronics in applications that require high-speed, high-resolution, and low-power ADCs, such as in wireless communication systems, image sensors, and biomedical devices. Additionally, SAR ADCs are known for their low complexity and ease of implementation, making them a popular choice in many electronics applications.

## Working
The analog input voltage (VIN) is held on a track/hold. If VIN is greater than VDAC, the comparator output is a logic high, or 1, and the MSB of the N-bit register remains at 1. Conversely, if VIN is less than VDAC, the comparator output is a logic low and the MSB of the register is cleared to logic 0.
The SAR control logic then moves to the next bit down, forces that bit high, and does another comparison. The sequence continues all the way down to the LSB. Once this is done, the conversion is complete and the N-bit digital word is available in the register.

## Block Diagram
![Picture1](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/bc348e96-6384-49c7-adee-3f5e3b7bf084)

## Circuits in Cadence
### 1.Sample and Hold
The sample-and-hold circuit samples the analog input signal and holds its voltage constant during the conversion process.
![Picture2](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/d9315022-a80f-4bb2-846d-a0612c8d9015)

### 2.Comparator
Compares the sampled analog input voltage to the output voltage of the DAC.
![Picture3](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/2fffe09a-1c87-4eb8-a01c-fa5a4aeb56d1)

### 3.SAR
Successive approximation register (SAR):
The SAR is a shift register that stores the bits of the digital output code of the ADC.
![Picture4a](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/9ea22a0a-3014-44ee-985f-05af4e3fb9e4)
![Picture4](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/73ce11e5-646f-4bd2-9ca2-0780934a486f)
![Picture5](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/81c3783f-e93a-4885-aff9-860acf7fa528)

### 4.DAC
The DAC converts the digital output of the SAR into an analog voltage that is compared to the input voltage by the comparator.
![Picture6](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/81d24af2-fc36-489d-8f7b-bb789b3705be)

## SAR ADC
![Picture7](https://github.com/AyanNaska/-Successive-Approximation-Register-SAR-Analog-to-Digital-Converter-ADC-/assets/113054786/fa8d46b3-0496-4a05-af04-aaed6b1468de)
