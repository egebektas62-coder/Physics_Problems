# 4. Energy & Momentum: Sliding Block and Collision

## Necessary Definitions and Formulas

### 1. Conservation of Mechanical Energy
In the first phase of this problem, a block slides down a frictionless track. Since there is no friction to do non-conservative work, the total mechanical energy is conserved. The gravitational potential energy at the top is completely converted into kinetic energy at the bottom.



**Formula:**

$$
mgh = \frac{1}{2}mv^2
$$

### 2. Conservation of Momentum (Perfectly Inelastic Collision)
In the second phase, the sliding block hits a stationary block and they stick together. This is called a **perfectly inelastic collision**. In any collision (without external horizontal forces), momentum is conserved, even if kinetic energy is lost.

**Formula:**

$$
m_1 v_1 + m_2 v_2 = (m_1 + m_2)v_f
$$

Where:
* **$m_1, m_2$**: Masses of the two objects
* **$v_1, v_2$**: Initial velocities before the collision
* **$v_f$**: Final shared velocity of the combined mass

---

## Problem Statement

A 0.5 kg block slides down a frictionless track from a height of 3.0 m. At the bottom, it collides and sticks to a 1.5 kg block, which is initially at rest. What is the speed of the combined mass just after the collision?

---

## Step-by-Step Solution

### Phase 1: Finding the speed of the first block at the bottom

**Step 1: Apply Conservation of Energy**
Let $m_1$ be the 0.5 kg block. It starts from rest at height $h =$ 3.0 m. 
Initial Potential Energy = Final Kinetic Energy

$$
m_1 gh = \frac{1}{2} m_1 v_1^2
$$

**Step 2: Solve for the velocity ($v_1$)**
Notice that the mass $m_1$ cancels out on both sides:

$$
gh = \frac{1}{2}v_1^2
$$

$$
v_1 = \sqrt{2gh}
$$

**Step 3: Substitute the known values**
Use the standard acceleration due to gravity ($g \approx$ 9.8 m/s²).

$$
v_1 = \sqrt{2 \cdot 9.8 \cdot 3.0}
$$

$$
v_1 = \sqrt{58.8} \approx 7.668 \text{ m/s}
$$

This is the speed of the 0.5 kg block just before the collision.

---

### Phase 2: The Collision at the Bottom

**Step 4: Set up the Conservation of Momentum equation**
We have two blocks before the collision:
* $m_1 =$ 0.5 kg with $v_1 = \sqrt{58.8}$ m/s
* $m_2 =$ 1.5 kg with $v_2 =$ 0 m/s (at rest)

After the collision, they stick together, meaning their combined mass is $(m_1 + m_2)$.

$$
m_1 v_1 + m_2 v_2 = (m_1 + m_2)v_f
$$

**Step 5: Substitute the known values**

$$
(0.5)(\sqrt{58.8}) + (1.5)(0) = (0.5 + 1.5)v_f
$$

Simplify the equation:

$$
0.5\sqrt{58.8} = 2.0 \cdot v_f
$$

**Step 6: Solve for the final velocity ($v_f$)**
Divide both sides by 2.0:

$$
v_f = \frac{0.5\sqrt{58.8}}{2.0}
$$

$$
v_f = 0.25\sqrt{58.8}
$$

Calculate the numerical approximation:

$$
v_f \approx 0.25 \cdot 7.668 \approx 1.917 \text{ m/s}
$$

---

## Final Results Summary

**Speed of the first block just before collision ($v_1$):**

$$
v_1 = \sqrt{58.8} \approx 7.67 \text{ m/s}
$$

**Speed of the combined mass just after collision ($v_f$):**

$$
v_f = \frac{\sqrt{58.8}}{4} \approx 1.92 \text{ m/s}
$$
