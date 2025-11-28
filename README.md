# SIMULATION OF AUTOCORRELATION AND PSD USING SCILAB

# AIM:

Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

# EQUIPMENTS Needed

• Computer with i3 Processor
• SCI LAB

# THEORY:

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.

<img width="585" height="95" alt="image" src="https://github.com/user-attachments/assets/49a48340-ffa0-4e35-8e40-b7f7aad9c87d" />

# Algorithm
1. Load or Define the Signal: Input your time-domain signal.

2. Compute Autocorrelation: Calculate the autocorrelation function of the signal.

3. Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.

4. Plot Results: Visualize the autocorrelation function and PSD.

# PROCEDURE

• Refer Algorithms and write code for the experiment.

• Open SCILAB in System

• Type your code in New Editor

• Save the file

• Execute the code

• If any Error, correct it in code and execute again

• Verify the generated waveform using Tabulation and Model Waveform

# PROGRAM:
```
clc
clear all; 
t=0:0.01:2*%pi;
x=sin(4*t) + cos(5*t); 
subplot(3,2,1); 
plot(x); 
au=xcorr(x,x);
subplot (3,2,2); 
plot (au); 
v=fft(au); 
subplot(3,2,3);
plot(abs(v)); 
fw=fft(x); 
subplot(3,2,4); 
plot(fw); 
fw2=(abs(fw)).^2;
subplot(3,2,5); 
plot(fw2);
```
# OUTPUT:

![WhatsApp Image 2025-11-28 at 22 08 47_56485228](https://github.com/user-attachments/assets/4a455d6b-3a5e-4af0-9eb9-3343fb62fb5c)



![output](https://github.com/user-attachments/assets/3546010e-c081-4438-aff1-8ff2486cc383)

# RESULT:
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
