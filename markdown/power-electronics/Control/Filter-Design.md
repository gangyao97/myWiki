## 1. First Order Filters

### 1.1. First Order Low Pass Filter

**S-Domain Transfer Function**
$$
H(s) = \frac{\omega_c}{s + \omega_c}
$$
Where:

- $\omega_c = 2\pi f_c$ (cutoff frequency in rad/s)

- $f_c$ = cutoff frequency in Hz

**Z-Domain Transfer Function**

$$
H(z) = \frac{b_0 + b_1z^{-1}}{1 + a_1z^{-1}}
$$

Where:

- $T$ = sampling period

- $K = 2/T$

- $b_0 = \frac{\omega_c}{K + \omega_c}$

- $b_1 = \frac{\omega_c}{K + \omega_c}$

- $a_1 = \frac{\omega_c - K}{K + \omega_c}$

**Bode Plot Characteristics:**

- DC gain: 0 dB

- -3 dB at $\omega_c$

- -20 dB/decade slope above $\omega_c$

- Phase: 0° at DC, -45° at $\omega_c$, -90° at high frequencies

### 1.2 First Order High Pass Filter

**S-Domain Transfer Function**
$$
H(s) = \frac{s}{s + \omega_c}
$$

**Z-Domain Transfer Function**
$$
H(z) = \frac{b_0 + b_1z^{-1}}{1 + a_1z^{-1}}
$$

Where:

- $T$ = sampling period

- $K = 2/T$

- $b_0 = \frac{K}{K + \omega_c}$

- $b_1 = -\frac{K}{K + \omega_c}$

- $a_1 = \frac{\omega_c - K}{K + \omega_c}$

**Bode Plot Characteristics:**

- Gain: -∞ at DC, 0 dB at high frequencies

- -3 dB at $\omega_c$

- +20 dB/decade slope below $\omega_c$

- Phase: +90° at DC, +45° at $\omega_c$, 0° at high frequencies

### 1.3 Lead-Lag and Lag-Lead Filters

**S-Domain Transfer Function**

$$
H(s) = \frac{\omega_p}{\omega_z} \frac{s + \omega_z}{s + \omega_p} 
$$

- Lead-lag Filter: $\omega_z<\omega_p$

- Lag-lead Filter: $\omega_z>\omega_p$

**Z-Domain Transfer Function**

$$
H(z) = \frac{\omega_p}{\omega_z}\frac{b_0 + b_1z^{-1}}{1 + a_1z^{-1}}
$$

Where:

- $b_0 = \frac{K + \omega_z}{K + \omega_p}$

- $b_1 = \frac{\omega_z - K}{K + \omega_p}$

- $a_1 = \frac{\omega_p - K}{K + \omega_p}$

- $T$ = sampling period

- $K = 2/T$

## 2. Second Order Filters

### 2.1 Second Order Low Pass Filter

**S-Domain Transfer Function**

$$
H(s) = \frac{\omega_0^2}{s^2 + \frac{\omega_0}{Q}s + \omega_0^2}
$$

Where:

- $\omega_0 = 2\pi f_0$ (natural frequency)

- $Q$ = quality factor

**Z-Domain Transfer Function**

$$
H(z) = \frac{b_0 + b_1z^{-1} + b_2z^{-2}}{1 + a_1z^{-1} + a_2z^{-2}}
$$

Where:

- $T$ = sampling period

- $b_0 = \frac{\omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}$

- $b_1 = \frac{2 \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}$

- $b_2 = b_0$

- $a_1 = \frac{-8 + 2 \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}$

- $a_2 = \frac{4 - \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}$

**Bode Plot Characteristics:**

- DC gain: 0 dB

- -3 dB at $\omega_0$

- -40 dB/decade slope above $\omega_0$

- Resonance peak increases with higher Q values

- Maximum peak when Q > 0.707

### 2.2 Second Order High Pass Filter

**S-Domain Transfer Function**

$$
H(s) = \frac{s^2}{s^2 + \frac{\omega_0}{Q}s + \omega_0^2}
$$

**Z-Domain Transfer Function**

$$
H(z) = \frac{b_0 + b_1z^{-1} + b_2z^{-2}}{1 + a_1z^{-1} + a_2z^{-2}}
$$

where:

$$
\begin{aligned}
b_0 &= \frac{4}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
b_1 &= \frac{-8}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
b_2 &= \frac{4}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
a_1 &= \frac{-8 + 2 \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
a_2 &= \frac{4 - \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}
\end{aligned}
$$

**Bode Plot Characteristics:**

- High frequency gain: 0 dB

- -3 dB at $\omega_0$

- +40 dB/decade slope below $\omega_0$

- Resonance characteristics similar to LPF

### 2.3 Band-Pass Filter

**S-Domain Transfer Function**

$$
H(s) = \frac{\frac{\omega_0}{Q}s}{s^2 + \frac{\omega_0}{Q}s + \omega_0^2}
$$

**Z-Domain Transfer Function:**
$$
H(z) = \frac{b_0 + b_1z^{-1} + b_2z^{-2}}{1 + a_1z^{-1} + a_2z^{-2}}
$$

where:

$$
\begin{aligned}
b_0 &= \frac{\dfrac{2 \omega_0 T}{Q}}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
b_1 &= 0 \\
b_2 &= -\frac{\dfrac{2 \omega_0 T}{Q}}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
a_1 &= \frac{-8 + 2 \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
a_2 &= \frac{4 - \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}
\end{aligned}
$$

**Bode Plot Characteristics:**

- Center frequency gain: 0 dB

- +20 dB/decade below center, -20 dB/decade above center

- Bandwidth = $\omega_0/Q$

- Higher Q = narrower bandwidth

### 2.4 Band-Stop (Notch) Filter

**S-Domain Transfer Function**

$$
H(s) = \frac{s^2 + \omega_0^2}{s^2 + \frac{\omega_0}{Q}s + \omega_0^2}
$$

**Z-Domain Transfer Function**

$$
H(z) = \frac{b_0 + b_1z^{-1} + b_2z^{-2}}{1 + a_1z^{-1} + a_2z^{-2}}
$$

Where:

$$
\begin{aligned}
b_0 &= \frac{4 + \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
b_1 &= \frac{-8 + 2 \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
b_2 &= \frac{4 + \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
a_1 &= \frac{-8 + 2 \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2} \\
a_2 &= \frac{4 - \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}{4 + \dfrac{2 \omega_0 T}{Q} + \omega_0^2 T^2}
\end{aligned}
$$

**Bode Plot Characteristics:**

- DC and high frequency gain: 0 dB

- Deep notch at $\omega_0$

- Notch depth depends on Q (higher Q = deeper notch)

- Symmetrical response around $\omega_0$

- -20 dB/decade slopes around notch frequency

### 2.5 Second Order Peaking Equalizer 

**S-Domain Transfer Function**

$$
H(s) = \frac{s^2 + \frac{\omega_0}{Q_{z}}s + \omega_0^2}{s^2 + \frac{\omega_0}{Q_{p}}s + \omega_0^2}
$$

Z-Domain Implementation

$$
H(z) = \frac{Q_{p}}{Q_{z}}\frac{b_0 + b_1z^{-1} + b_2z^{-2}}{1 + a_1z^{-1} + a_2z^{-2}}
$$

Where:

$$
\begin{aligned}
b_0 &= \frac{4 Q_{z} + {2 \omega_0 T} +\omega_0^2 T^2 Q_{z}}{4 Q_{p} + {2 \omega_0 T} + \omega_0^2 T^2 Q_{p}} \\
b_1 &= \frac{-8 + 2 \omega_0^2 T^2 Q_{z}}{4 Q_{p} + {2 \omega_0 T} + \omega_0^2 T^2 Q_{p}} \\
b_2 &= \frac{4 Q_{z} -{2 \omega_0 T} + \omega_0^2 T^2 Q_{z}}{4 Q_{p} + {2 \omega_0 T} + \omega_0^2 T^2 Q_{p}} \\
a_1 &= \frac{-8 Q_{p} + 2 \omega_0^2 T^2 Q_{p}}{4 Q_{p} + {2 \omega_0 T} + \omega_0^2 T^2 Q_{p}} \\
a_2 &= \frac{4 Q_{p} -{2 \omega_0 T} + \omega_0^2 T^2 Q_{p}}{4 Q_{p} + {2 \omega_0 T} + \omega_0^2 T^2 Q_{p}}
\end{aligned}
$$

- Positive Gain: $Q_{p}>Q_{z}$

- Negative Gain: $Q_{p}<Q_{z}$