# Ideal, Natural, & Flat-top -Sampling
## Aim
Write a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.
# Tools required
# Program
```
# Impulse Sampling
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample

fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)

# Sampling
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)

# Reconstruction
reconstructed_signal = resample(signal_sampled, len(t))

# Create subplots
plt.figure(figsize=(12, 8))

# Plot 1: Continuous Signal
plt.subplot(3, 1, 1)
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()

# Plot 2: Sampled Signal
plt.subplot(3, 1, 2)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()

# Plot 3: Reconstructed Signal
plt.subplot(3, 1, 3)
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()

plt.tight_layout()
plt.show()
```
# Output Waveform
```

```
# Results
```
Attach the output waveform
```
# Hardware experiment output waveform.
