# 5. Inelastic Collision: Runner and Cart

## Necessary Definitions and Formulas

### 1. Conservation of Momentum
In any collision where no external horizontal forces are applied, the total momentum of the system is conserved. The total momentum before the collision equals the total momentum after the collision.



**Formula:**

$$
\vec{p}_{initial} = \vec{p}_{final}
$$

$$
m_1 v_1 + m_2 v_2 = (m_1 + m_2)v_f
$$

### 2. Perfectly Inelastic Collision
A perfectly inelastic collision occurs when two objects collide and stick together, moving as a single combined mass afterwards. While momentum is always conserved, **kinetic energy is not conserved** in an inelastic collision. Some kinetic energy is transformed into other forms of energy (like heat, sound, or internal deformation).

### 3. Kinetic Energy ($KE$)
The energy of motion. We can calculate it before and after the collision to prove whether it is conserved.

**Formula:**

$$
KE = \frac{1}{2}mv^2
$$

---

## Problem Statement

A 70 kg runner moving at $3 \text{ m/s}$ jumps onto a 140 kg stationary cart. What is the final speed of the cart with the runner? Is kinetic energy conserved in this collision? Explain.

---

## Step-by-Step Solution

### Part A: Find the final speed of the cart with the runner

**Step 1: Identify the initial values**
* Mass of runner ($m_1$): 70 kg
* Velocity of runner ($v_1$): 3 m/s
* Mass of cart ($m_2$): 140 kg
* Velocity of cart ($v_2$): 0 m/s (stationary)

**Step 2: Apply the conservation of momentum equation**

$$
m_1 v_1 + m_2 v_2 = (m_1 + m_2)v_f
$$

**Step 3: Substitute the known values and solve for $v_f$**

$$
(70)(3) + (140)(0) = (70 + 140)v_f
$$

$$
210 + 0 = 210 \cdot v_f
$$

$$
210 = 210 \cdot v_f
$$

Divide both sides by 210:

$$
v_f = 1 \text{ m/s}
$$

The final speed of the cart and runner together is **1 m/s**.

---

### Part B: Analyze Kinetic Energy Conservation

To determine if kinetic energy is conserved, we must calculate the total kinetic energy before and after the collision.

**Step 4: Calculate Initial Kinetic Energy ($KE_i$)**
Before the collision, only the runner is moving.

$$
KE_i = \frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2
$$

$$
KE_i = \frac{1}{2}(70)(3)^2 + 0
$$

$$
KE_i = 35 \cdot 9 = 315 \text{ Joules}
$$

**Step 5: Calculate Final Kinetic Energy ($KE_f$)**
After the collision, the combined mass is moving together at $v_f = 1 \text{ m/s}$.

$$
KE_f = \frac{1}{2}(m_1 + m_2)v_f^2
$$

$$
KE_f = \frac{1}{2}(210)(1)^2
$$

$$
KE_f = 105 \cdot 1 = 105 \text{ Joules}
$$

**Step 6: Compare and Explain**
* Initial Kinetic Energy: **315 J**
* Final Kinetic Energy: **105 J**

Since $315 \text{ J} \neq 105 \text{ J}$, kinetic energy is **not conserved**. In fact, 210 Joules of kinetic energy were lost. 

**Explanation:** In a perfectly inelastic collision (where objects stick together), the "lost" kinetic energy does not disappear from the universe; instead, it is converted into other forms of energy. In this scenario, the energy is dissipated as sound (the thud of landing), heat (friction between the runner's shoes and the cart), and the internal work done by the runner's muscles and joints to absorb the impact and stabilize on the cart.

---

## Final Results Summary

**Final Speed ($v_f$):**

$$
v_f = 1 \text{ m/s}
$$

**Is kinetic energy conserved?** **No**. The system had 315 J of kinetic energy before the collision, but only 105 J after. The missing 210 J was dissipated as heat, sound, and internal energy during the impact.
