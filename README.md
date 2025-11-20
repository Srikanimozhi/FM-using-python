# FM-using-python
Aim

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. Apparatus Required
1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer Theory
Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:


Algorithm

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

program

import numpy as np

import matplotlib.pyplot as plt
```asm
Am = 4.9
Ac = 9.8
fm = 677
fc = 6770
fs = 67700
kf = 100
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
integral_m = np.cumsum(m) / fs
s = Ac * np.cos(2 * np.pi * fc * t + 2 * np.pi * kf * integral_m)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```
Output
<img width="627" height="469" alt="image" src="https://github.com/user-attachments/assets/0b339047-f9ff-4a2f-9ff3-19b7747f4fc3" />

calculation
![WhatsApp Image 2025-10-23 at 22 45 58_71bce3db](https://github.com/user-attachments/assets/af407bb0-8d6d-4227-87ea-e8bb8cd6fc20)



Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
 
