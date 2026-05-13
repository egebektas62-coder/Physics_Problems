# Biot-Savart Law: Magnetic Field of a Current Segment

## Necessary Definitions and Formulas

### The Biot-Savart Law (Magnitude)
The magnetic field magnitude $dB$ produced by a small segment of wire of length $dl$ carrying a current $I$ at a distance $r$ is given by:

$$
dB = \frac{\mu_0 I dl \sin(\theta)}{4 \pi r^2}
$$

* **Vacuum permeability ($\mu_0$):** $4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}$
* **$\theta$**: The angle between the direction of the current segment and the line connecting it to the observation point $P$.

---

## Problem Statement

A small segment of a line wire of length $0.1 \text{ m}$ carries a current of $3 \text{ A}$. The segment is located at a distance of $0.2 \text{ m}$ from a point $P$. Calculate the magnetic field at point $P$ due to this current segment (assume the segment is perpendicular to the line connecting it to point $P$).

---

## Step-by-Step Solution

### Step 1: Identify the Known Variables
* **Current ($I$):** $3 \text{ A}$
* **Length of segment ($dl$):** $0.1 \text{ m}$
* **Distance to point P ($r$):** $0.2 \text{ m}$
* **Angle ($\theta$):** $90^\circ$ (since the segment is perpendicular to the line connecting it to P), so $\sin(90^\circ) = 1$

### Step 2: Apply the Formula
Substitute the known values into the Biot-Savart equation:

$$
dB = \frac{(4\pi \times 10^{-7}) \cdot 3 \cdot 0.1 \cdot \sin(90^\circ)}{4 \pi \cdot (0.2)^2}
$$

### Step 3: Calculate the Result
Cancel out the $4\pi$ from the numerator and denominator:

$$
dB = \frac{10^{-7} \cdot 0.3}{0.04}
$$

$$
dB = \frac{0.3}{0.04} \times 10^{-7}
$$

$$
dB = 7.5 \times 10^{-7} \text{ T}
$$

---

## Final Results Summary

* **Magnitude of the Magnetic Field ($dB$):** $7.5 \times 10^{-7} \text{ T}$ (or $0.75 \mu\text{T}$)
