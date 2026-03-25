# 2. Harmonic Motion: Mass-Spring System

## Necessary Definitions and Formulas

### 1. Equation of Simple Harmonic Motion (SHM)
The position of an object undergoing simple harmonic motion is often described by a cosine or sine function of time:

$$
x(t) = A \cos(\omega t + \phi)
$$

Where:
* **$A$**: Amplitude (maximum displacement from equilibrium)
* **$\omega$**: Angular frequency (how fast the system oscillates, in rad/s)
* **$t$**: Time
* **$\phi$**: Phase angle (initial starting position, assumed 0 here)



### 2. Angular Frequency and Spring Constant
For a mass-spring system, the angular frequency depends strictly on the mass ($m$) and the stiffness of the spring, known as the spring constant ($k$):

$$
\omega = \sqrt{\frac{k}{m}}
$$

To solve for the spring constant $k$, we square both sides and rearrange:

$$
k = m\omega^2
$$

### 3. Total Mechanical Energy
In an ideal, frictionless mass-spring system, the total mechanical energy ($E$) is conserved. It is equal to the maximum potential energy stored in the spring when it is fully stretched or compressed (at the amplitude $A$):

$$
E = \frac{1}{2}kA^2
$$

---

## Problem Statement

A 10 kg mass is attached to a spring and oscillates according to the equation $x(t) = 0.2 \cos(10\pi t)$ (in meters). What is the spring constant $k$? What is the total mechanical energy of the system?

---

## Step-by-Step Solution

### Step 1: Identify the given parameters from the equation
By comparing the given equation $x(t) = 0.2 \cos(10\pi t)$ with the standard SHM formula $x(t) = A \cos(\omega t)$, we can extract the specific values:
* **Mass ($m$)**: 10 kg
* **Amplitude ($A$)**: 0.2 m
* **Angular frequency ($\omega$)**: $10\pi$ rad/s

### Step 2: Calculate the spring constant ($k$)
We use the rearranged angular frequency formula to find $k$:

$$
k = m\omega^2
$$

Substitute the known values of mass and angular frequency:

$$
k = 10 \cdot (10\pi)^2
$$

Square the term inside the parentheses:

$$
k = 10 \cdot 100\pi^2
$$

$$
k = 1000\pi^2 \text{ N/m}
$$

*(If a numerical approximation is needed: $\pi^2 \approx 9.87$, so $k \approx 9869.6$ N/m).*

### Step 3: Calculate the total mechanical energy ($E$)
Now that we have the spring constant and the amplitude, we can find the total mechanical energy of the system:

$$
E = \frac{1}{2}kA^2
$$

Substitute the values for $k$ and $A$:

$$
E = \frac{1}{2}(1000\pi^2)(0.2)^2
$$

Square the amplitude:

$$
E = \frac{1}{2}(1000\pi^2)(0.04)
$$

Multiply the constants:

$$
E = 500\pi^2 \cdot 0.04
$$

$$
E = 20\pi^2 \text{ Joules}
$$

*(If a numerical approximation is needed: $20 \times 9.87 \approx 197.4$ Joules).*

---

## Final Results Summary

**Spring Constant ($k$):**

$$
k = 1000\pi^2 \text{ N/m}
$$

**Total Mechanical Energy ($E$):**

$$
E = 20\pi^2 \text{ J}
$$
