# Wave Equation Analysis: Reverse Engineering a Wave

## Necessary Definitions and Formulas

### 1. The Standard Wave Equation
A one-dimensional traveling wave is mathematically described by the standard sinusoidal wave function:

$$
y(x,t) = A \sin(kx - \omega t + \phi)
$$

Where:
* **$y(x,t)$**: The vertical displacement of the wave at position $x$ and time $t$.
* **$A$**: Amplitude (maximum displacement from the equilibrium position).
* **$k$**: Angular Wave Number (relates to the spatial period).
* **$\omega$**: Angular Frequency (relates to the time period).
* **$\phi$**: Phase constant (shifts the wave left or right). The minus sign ($-$) indicates the wave is traveling in the positive x-direction.



### 2. Formulas for Extracting Properties
Once $k$ and $\omega$ are extracted from the equation, we can find the physical properties of the wave:

* **Wavelength ($\lambda$):**
  
$$
\lambda = \frac{2\pi}{k}
$$

* **Frequency ($f$):**
  
$$
f = \frac{\omega}{2\pi}
$$

* **Wave Speed ($v$):**
  
$$
v = f \cdot \lambda \quad \text{or} \quad v = \frac{\omega}{k}
$$

---

## Problem Statement

A wave is described by the equation $y(x,t) = 0.05 \sin(2\pi x - 50\pi t)$, where $x$ and $y$ are in meters and $t$ is in seconds. Determine the wave's:
a) Amplitude $A$
b) Wavelength $\lambda$
c) Frequency $f$
d) Wave speed $v$

---

## Step-by-Step Solution

### Preliminary Step: Pattern Matching
We align the given equation with the standard wave equation to extract the raw variables.

Given: 

$$
y(x,t) = 0.05 \sin(2\pi x - 50\pi t)
$$

Standard: 

$$
y(x,t) = A \sin(kx - \omega t)
$$

By direct comparison, we extract:
* $A = 0.05$
* $k = 2\pi$
* $\omega = 50\pi$

### a) Determine Amplitude ($A$)
The amplitude is the coefficient in front of the sine function. We extracted this directly.

$$
A = 0.05 \text{ m}
$$

### b) Determine Wavelength ($\lambda$)
We use the extracted angular wave number ($k = 2\pi \text{ rad/m}$) to find the wavelength.

$$
\lambda = \frac{2\pi}{k}
$$

Substitute $k = 2\pi$:

$$
\lambda = \frac{2\pi}{2\pi} = 1 \text{ m}
$$

### c) Determine Frequency ($f$)
We use the extracted angular frequency ($\omega = 50\pi \text{ rad/s}$) to find the standard frequency.

$$
f = \frac{\omega}{2\pi}
$$

Substitute $\omega = 50\pi$:

$$
f = \frac{50\pi}{2\pi} = 25 \text{ Hz}
$$

*Explanation:* The wave oscillates 25 times per second.

### d) Determine Wave Speed ($v$)
We can calculate the speed using either $v = f \cdot \lambda$ or $v = \frac{\omega}{k}$. Both will yield the exact same result. Let's use the extracted frequency and wavelength:

$$
v = f \cdot \lambda
$$

Substitute $f = 25$ and $\lambda = 1$:

$$
v = 25 \cdot 1 = 25 \text{ m/s}
$$

---

## Final Results Summary

* **a) Amplitude ($A$):** $0.05 \text{ m}$
* **b) Wavelength ($\lambda$):** $1 \text{ m}$
* **c) Frequency ($f$):** $25 \text{ Hz}$
* **d) Wave Speed ($v$):** $25 \text{ m/s}$
