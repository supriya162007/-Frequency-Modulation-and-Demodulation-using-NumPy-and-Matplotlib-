# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

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
```
import numpy as np
import matplotlib.pyplot as plt
Am = 8.3          
Fm = 400          
B  = 6.3          
Ac = 16.6         
Fc = 4800         
Fs = 96000        

t = np.arange(0, 2/Fm, 1/Fs)

# Message signal
em = Am * np.sin(2 * np.pi * Fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, em)
plt.grid()

# Carrier signal
ec = Ac * np.sin(2 * np.pi * Fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, ec)
plt.grid()

# FM signal
efm = Ac * np.cos((2*np.pi*Fc*t) + (B * np.sin(2*np.pi*Fm*t)))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.grid()

plt.tight_layout()
plt.show()
```

__Output:__
![WhatsApp Image 2025-11-21 at 09 26 43_5eb979f3](https://github.com/user-attachments/assets/686225f7-4b9c-43c8-83af-cf30364d6c47)


__Result:__
The Code Is Executed and the output is verified 
