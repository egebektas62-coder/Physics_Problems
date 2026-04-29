# Lorentz Force Acting on a Current-Carrying Wire

## Necessary Definitions and Formulas

### 1. Magnetic Force on a Wire
When a current $I$ flows through a straight wire of length $L$ in a uniform magnetic field $B$, every moving charge inside the wire experiences a Lorentz force. The macroscopic sum of all these microscopic forces results in a measurable mechanical force on the wire itself.

The force vector is given by the cross product:

$$
\vec{F}_B = I (\vec{L} \times \vec{B})
$$

### 2. Magnitude of the Force
Since it's a cross product, the magnitude depends heavily on the angle ($\theta$) between the direction of the current (the wire) and the direction of the magnetic field lines.

$$
F_B = I \cdot L \cdot B \cdot \sin(\theta)
$$

Where:
* **$F_B$**: Magnetic force (in Newtons, N)
* **$I$**: Current (in Amperes, A)
* **$L$**: Length of the wire inside the field (in meters, m)
* **$B$**: Magnetic field strength (in Teslas, T)
* **$\theta$**: Angle between the wire and the magnetic field

---

## Problem Statement

A straight wire 2.0 m long carries a current of 10 A. It is placed in a uniform magnetic field of $B = 0.5$ T. Calculate the magnetic force on the wire if the angle between the wire and the magnetic field is:
a) $90^\circ$
b) $45^\circ$
c) $0^\circ$

---

## Step-by-Step Solution

### Preliminary Step: Calculate the Maximum Possible Force
Let's pre-calculate the constant multiplier $(I \cdot L \cdot B)$ which represents the maximum theoretical force when the wire is perfectly perpendicular to the field.

* **$I$:** $10 \text{ A}$
* **$L$:** $2.0 \text{ m}$
* **$B$:** $0.5 \text{ T}$

$$
F_{max} = 10 \cdot 2.0 \cdot 0.5 = 10 \text{ N}
$$

Now we apply the specific angles.

### a) Angle $\theta = 90^\circ$ (Perpendicular)
When the wire is perpendicular to the field, $\sin(90^\circ) = 1$. The force is at its absolute maximum.

$$
F_B = 10 \cdot \sin(90^\circ) = 10 \cdot 1 = 10 \text{ N}
$$

### b) Angle $\theta = 45^\circ$
When the wire is tilted, only the perpendicular component of the wire interacts with the field. $\sin(45^\circ) = \frac{\sqrt{2}}{2} \approx 0.707$.

$$
F_B = 10 \cdot \sin(45^\circ) = 10 \cdot 0.707 = 7.07 \text{ N}
$$

### c) Angle $\theta = 0^\circ$ (Parallel)
When the wire is perfectly parallel to the magnetic field lines, $\sin(0^\circ) = 0$. The cross product of two parallel vectors is zero.

$$
F_B = 10 \cdot \sin(0^\circ) = 10 \cdot 0 = 0 \text{ N}
$$

*Explanation:* If the electrons are flowing in the exact same direction as the magnetic river (or exactly against it), they cut across zero field lines. No lines cut = no force generated.

---

## Final Results Summary

* **a) At $90^\circ$:** $10 \text{ N}$ (Maximum Force)
* **b) At $45^\circ$:** $\approx 7.07 \text{ N}$ (Partial Force)
* **c) At $0^\circ$:** $0 \text{ N}$ (Zero Force / Blind Spot)
