# señales de trasmisión.
# Código de python
import numpy as np
import sounddevice as sd

fs = 48000
t = np.linspace(0, 5, fs * 5, endpoint=False)  # 5 segundos de duración
tono = 0.5 * np.sin(2 * np.pi * 18500 * t)  # Señal a 18,500 Hz

sd.play(tono.astype(np.float32), samplerate=fs, blocking=True)
