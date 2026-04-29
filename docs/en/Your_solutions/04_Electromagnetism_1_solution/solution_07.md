# Cyclotron Motion: Electron in a Magnetic Field

## Necessary Definitions and Formulas

### 1. Acceleration by Electric Potential
When a charged particle accelerates from rest through a potential difference $V$, its electric potential energy is converted entirely into kinetic energy.

$$
K = qV \implies \frac{1}{2}mv^2 = qV
$$

### 2. Magnetic Lorentz Force
When a charged particle moves with velocity $v$ perpendicular to a uniform magnetic field $B$, it experiences a magnetic force that acts perpendicular to both its velocity vector and the magnetic field vector.

$$
F_B = qvB
$$

### 3. Centripetal Force and Circular Motion
Because the magnetic force is always perpendicular to the velocity, it acts as a centripetal force, forcing the particle into a circular path of radius $r$.

$$
F_c = \frac{mv^2}{r}
$$

Equating the magnetic force to the centripetal force gives the radius of the orbit:

$$
qvB = \frac{mv^2}{r} \implies r = \frac{mv}{qB}
$$

---

## Problem Statement

An electron is accelerated from rest through a potential difference of 5000 V. It then enters a region of uniform magnetic field B = 0.1 T, perpendicular to its velocity. What is the radius of the circular path it will follow?

---

## Step-by-Step Solution

### Step 1: Identify the Known Constants
* **Mass of an electron ($m$):** $\approx 9.11 \times 10^{-31} \text{ kg}$
* **Charge of an electron ($q$):** $\approx 1.60 \times 10^{-19} \text{ C}$
* **Potential difference ($V$):** $5000 \text{ V}$
* **Magnetic field ($B$):** $0.1 \text{ T}$

### Step 2: Calculate the Velocity ($v$)
Using the kinetic energy equation:

$$
\frac{1}{2}mv^2 = qV \implies v = \sqrt{\frac{2qV}{m}}
$$

Substitute the exact values:

$$
v = \sqrt{\frac{2(1.60 \times 10^{-19})(5000)}{9.11 \times 10^{-31}}}
$$

$$
v = \sqrt{\frac{1.60 \times 10^{-15}}{9.11 \times 10^{-31}}} = \sqrt{1.756 \times 10^{15}}
$$

$$
v \approx 4.19 \times 10^7 \text{ m/s}
$$

*(Note: This is approximately 14% the speed of light. A classical mechanics approach is standard for this problem, but relativistic effects are just starting to become noticeable).*

### Step 3: Calculate the Radius ($r$)
Using the isolated radius equation:

$$
r = \frac{mv}{qB}
$$

Substitute the calculated velocity and other given values:

$$
r = \frac{(9.11 \times 10^{-31})(4.19 \times 10^7)}{(1.60 \times 10^{-19})(0.1)}
$$

$$
r = \frac{3.817 \times 10^{-23}}{1.60 \times 10^{-20}}
$$

$$
r \approx 2.38 \times 10^{-3} \text{ m}
$$

---

## Final Results Summary

* **Velocity of the electron ($v$):** $\approx 4.19 \times 10^7 \text{ m/s}$
* **Radius of the circular path ($r$):** $\approx 2.38 \text{ mm}$ (or $2.38 \times 10^{-3} \text{ m}$)
