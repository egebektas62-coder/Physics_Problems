# Ampere's Law: Magnetic Field of Parallel Wires

## Necessary Definitions and Formulas

### 1. Magnetic Field of a Long Straight Wire
Ampere's Law tells us that a long, straight wire carrying a steady current $I$ creates a magnetic field $B$ that circles the wire. The magnitude of this field at a radial distance $r$ from the wire is:

$$
B = \frac{\mu_0 I}{2 \pi r}
$$

* **Vacuum permeability ($\mu_0$):** $4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}$

### 2. The Right-Hand Grip Rule
To find the direction of the magnetic field, point your right thumb in the direction of the current. Your fingers will curl around the wire in the direction of the circular magnetic field lines.

### 3. Superposition Principle
When multiple wires create magnetic fields in the same region of space, the net magnetic field at any point is the vector sum of the individual fields:

$$
\vec{B}_{net} = \vec{B}_1 + \vec{B}_2
$$

---

## Problem Statement

Two long, parallel wires are $10 \text{ cm}$ apart and carry currents of $5 \text{ A}$ in opposite directions. Calculate the magnitude and direction of the magnetic field at a point midway between the wires.

---

## Step-by-Step Solution

### Step 1: Identify the Known Variables
* **Currents ($I_1$ and $I_2$):** $5 \text{ A}$ (opposite directions)
* **Distance between wires ($d$):** $10 \text{ cm} = 0.1 \text{ m}$
* **Distance to the midpoint ($r$):** $\frac{0.1}{2} = 0.05 \text{ m}$ for both wires.

### Step 2: Determine the Directions of the Fields
Imagine the two wires laying flat on a table.
* Wire 1 is on the left, carrying current **UP** the table. By the right-hand rule, its magnetic field points **INTO** the table at the midpoint (to its right).
* Wire 2 is on the right, carrying current **DOWN** the table. By the right-hand rule, its magnetic field also points **INTO** the table at the midpoint (to its left).

Since both $\vec{B}_1$ and $\vec{B}_2$ point in the exact same direction at the midpoint, we simply add their magnitudes together.

### Step 3: Calculate the Magnitude from One Wire
Let's find the field produced by Wire 1 ($B_1$) at the midpoint:

$$
B_1 = \frac{(4\pi \times 10^{-7}) \cdot 5}{2 \pi \cdot 0.05}
$$

Cancel out the $\pi$ and simplify the constants:

$$
B_1 = \frac{(2 \times 10^{-7}) \cdot 5}{0.05} = \frac{10 \times 10^{-7}}{0.05}
$$

$$
B_1 = 200 \times 10^{-7} = 2 \times 10^{-5} \text{ T} \quad (\text{or } 20 \mu\text{T})
$$

### Step 4: Calculate the Total Magnetic Field
Since Wire 2 carries the same current at the same distance, its magnitude is identical ($B_2 = 2 \times 10^{-5} \text{ T}$). 

Because they point in the same direction, the total field is:

$$
B_{net} = B_1 + B_2 = (2 \times 10^{-5}) + (2 \times 10^{-5})
$$

$$
B_{net} = 4 \times 10^{-5} \text{ T} \quad (\text{or } 40 \mu\text{T})
$$

---

## Final Results Summary

* **Magnitude of the Magnetic Field ($B_{net}$):** $4 \times 10^{-5} \text{ T}$ (or $40 \mu\text{T}$)
* **Direction:** Perpendicular to the plane containing the wires, pointing in the same direction for both (e.g., "into the page" or "out of the page" depending on the chosen spatial orientation of the opposite currents).

---
