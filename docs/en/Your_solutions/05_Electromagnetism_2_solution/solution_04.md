# Magnetic Torque on a Rectangular Loop

## Necessary Definitions and Formulas

Before we solve the problem, let's review the key concepts related to magnetic torque.

### 1. Magnetic Dipole Moment ($\mu$)
A current-carrying loop acts like a small magnet, characterized by its magnetic dipole moment. The magnitude is the product of the current and the area of the loop.

$$
\mu = I \cdot A
$$

### 2. Magnetic Torque ($\tau$)
When a magnetic dipole is placed in an external magnetic field, it experiences a torque that tries to align the dipole moment with the field. The magnitude of this torque is given by:

$$
\tau = \mu \cdot B \cdot \sin(\theta)
$$

Where:
*   **$I$**: Current in the loop
*   **$A$**: Area of the loop
*   **$B$**: External magnetic field strength
*   **$\theta$**: The angle between the magnetic field vector ($\vec{B}$) and the **normal vector** (perpendicular line) to the plane of the loop.

---

## Step-by-Step Solution

Let's break down the given parameters and convert them to standard SI units:
*   **Length ($l$):** $10 \text{ cm} = 0.1 \text{ m}$
*   **Width ($w$):** $5 \text{ cm} = 0.05 \text{ m}$
*   **Current ($I$):** $2 \text{ A}$
*   **Magnetic Field ($B$):** $0.3 \text{ T}$
*   **Orientation:** Field is *parallel* to the plane of the loop.

### Step 1: Calculate the area of the loop ($A$)
First, we find the area of the rectangular loop in square meters.

$$
A = l \cdot w
$$

$$
A = 0.1 \text{ m} \cdot 0.05 \text{ m}
$$

**$A = 0.005 \text{ m}^2$**

### Step 2: Determine the angle ($\theta$)
This is the most critical conceptual step. The formula for torque uses the angle between the magnetic field and the **normal** to the loop's surface. 
Because the magnetic field is given as *parallel* to the plane of the loop, it is perfectly perpendicular to the normal vector of that plane.

$$
\theta = 90^\circ \implies \sin(90^\circ) = 1
$$

### Step 3: Calculate the magnetic torque ($\tau$)
Now we substitute all our values into the full torque equation.

$$
\tau = (I \cdot A) \cdot B \cdot \sin(\theta)
$$

$$
\tau = (2 \cdot 0.005) \cdot 0.3 \cdot 1
$$

$$
\tau = 0.01 \cdot 0.3
$$

**$\tau = 0.003 \text{ N}\cdot\text{m}$**

---

## Final Result

The magnitude of the magnetic torque on the rectangular loop is **$0.003 \text{ N}\cdot\text{m}$**.
