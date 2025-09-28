## PM Synchronous Machine Drives

### PM machine equivalent circuit models
The amplitude of the back-emf phasor can be expressed simply as

- $E$ = $\omega_r$ * $\psi_m$

Parameter Definitions

- $E$: Amplitude of the back EMF phasor in V-pk (Volts peak)

- $\omega_r$: Rotor angular frequency in electrical radians per second (rad/s)

- $\psi_m$: Magnetic flux linkage (typically permanent magnet flux $\psi_{pm}$)

**DQ Transformation Equations:**

```math
\begin{align*}
v_d &= \frac{2}{3}\left[v_{a}\cos(\theta_r) + v_{b}\cos\left(\theta_r - \frac{2\pi}{3}\right) + v_{c}\cos\left(\theta_r - \frac{4\pi}{3}\right)\right] \\
v_q &= -\frac{2}{3}\left[v_{a}\sin(\theta_r) + v_{b}\sin\left(\theta_r - \frac{2\pi}{3}\right) + v_{c}\sin\left(\theta_r - \frac{4\pi}{3}\right)\right]
\end{align*}
```
<p align="center">
<img src="../../../..//src/assets/PM%20machine%20synchronously%20rotating%20dq%20reference%20frame.png" alt="PM machine synchronously rotating dq reference frame" width="400"/> 
<p align="center">


### PMSM dq-axis Voltage and Flux Linkage Equations

The voltage equations in the **d–q reference frame** are:

$$
v_d = R_s i_d + L_d \frac{di_d}{dt} - \omega_r L_q i_q
$$

$$
v_q = R_s i_q + L_q \frac{di_q}{dt} + \omega_r (L_d i_d + \psi_{pm})

$$


The **d–q axes flux linkages** are defined as:

$$
\psi_d = L_d i_d + \psi_{pm} \quad \text{[Wb]}
$$

$$
\psi_q = L_q i_q

$$
### PMSM Electromagnetic Torque Equation

The electromagnetic torque in the **d–q reference frame** is given by:

$$
T_e = \frac{3p}{2} \Big[ \psi_{pm} i_q + i_q i_d (L_d - L_q) \Big]

$$

# Alternative PMSM Torque Equation with Torque Angle γ

$$
T_e = \frac{3}{2}p \left[ \lambda_{pm} I \cos\gamma + \frac{1}{2}(L_d - L_q) I^2 \sin(2\gamma) \right]
$$

**Where:**
- $p$ = number of pole pairs  
- $\lambda_{pm}$ = permanent magnet flux linkage
- $I$ = Current magnitude  
- $\gamma$ = torque angle (angle between $I$ and $i_{q}$)

# PM Machine Power Equations

## Torque–Speed–Power Relationship

The electromagnetic torque and mechanical power are related as:

$$
P_{\text{mech}} = T_e \, \omega_m
$$

where:
- $T_e$ = electromagnetic torque  
- $\omega_m$  = mechanical angular speed (rad/s)  

The electrical angular speed is related by:

$$
\omega_e = p \, \omega_m
$$

with $p$ = number of pole pairs.

The torque equation is:

$$
T_e = \frac{3p}{2}\left(\psi_{pm} i_q + (L_d - L_q)i_d i_q\right)
$$

---

## Power in the dq Reference Frame

The instantaneous electrical power in the \( dq \) frame is:

$$
p(t) = \frac{3}{2}\,(v_d i_d + v_q i_q)
$$

The average real power is:

$$
P = \frac{3}{2}\,\big(\overline{v_d i_d} + \overline{v_q i_q}\big)
$$

Reactive power is defined as:

$$
Q = \frac{3}{2}\,(v_q i_d - v_d i_q)
$$

Apparent power:

$$
S = \sqrt{P^2 + Q^2}
$$

---

## Power in the abc Reference Frame

The instantaneous three-phase power is:

$$
p(t) = v_a i_a + v_b i_b + v_c i_c
$$

In balanced sinusoidal steady state (RMS values):

$$
P = 3 V_{\text{ph}} I_{\text{ph}} \cos\varphi
$$

or equivalently:

$$
P = \sqrt{3} V_{LL} I_{L} \cos\varphi
$$

where:
- $V_{\text{ph}}$ = RMS phase voltage  
- $I_{\text{ph}}$ = RMS phase current  
-  $V_{LL}$= RMS line-to-line voltage
