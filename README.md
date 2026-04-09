# Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__
```Python
import numpy as np
import matplotlib.pyplot as plt

Am = 10.3
Fm = 400
B  = 5
Ac = 20.6
Fc = 4000
Fs = 40000

T = np.arange(0, 2/Fm, 1/Fs)

em = Am * np.cos(2 * np.pi * Fm * T)

plt.subplot(3, 1, 1)
plt.plot(T, em)
plt.title("Message Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()

ec = Ac * np.cos(2 * np.pi * Fc * T)

plt.subplot(3, 1, 2)
plt.plot(T, ec)
plt.title("Carrier Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()

efm = Ac * np.cos((2 * np.pi * Fc * T) + (B * np.sin(2 * np.pi * Fm * T)))

plt.subplot(3, 1, 3)
plt.plot(T, efm)
plt.title("FM Signal")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()

plt.tight_layout()
plt.show()

```
__Tabulation__

![FM tbale](https://github.com/user-attachments/assets/6da95663-801a-4733-8665-b817a9218df1)

__Output:__

<img width="801" height="602" alt="FM Modulation using python" src="https://github.com/user-attachments/assets/9597f9be-d659-4462-a0b2-7d9708eaa08e" />


__Result:__

Thus Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib is experimentally done and the output is verified
