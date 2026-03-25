# 7. Dynamics with Friction: Stacked Blocks

## Necessary Definitions and Formulas

### 1. Kinetic Friction
Friction is a force that opposes the relative motion between two surfaces in contact. When the surfaces are sliding past one another, we use kinetic friction ($f_k$).



**Formula:**

$$
f_k = \mu_k N
$$

Where:
* **$f_k$**: Force of kinetic friction
* **$\mu_k$**: Coefficient of kinetic friction
* **$N$**: Normal force perpendicular to the surface

### 2. Normal Force ($N$)
The normal force is the support force exerted upon an object that is in contact with another stable object. For flat, horizontal surfaces with no vertical acceleration, it equals the weight of the objects being supported ($N = mg$).

### 3. Newton's Second Law
The net force acting on an object is equal to its mass times its acceleration.

$$
F_{net} = m \cdot a
$$

---

## Problem Statement

A 5 kg block is placed on a 10 kg block. A horizontal force of 45 N is applied to the 10 kg block, and the 5 kg block is tied to the wall. The coefficient of kinetic friction between all moving surfaces is 0.2. Find the acceleration of the 10 kg block.

---

## Step-by-Step Solution

Let's define our variables:
* Top block mass ($m_1$): 5 kg
* Bottom block mass ($m_2$): 10 kg
* Applied force ($F_{app}$): 45 N
* Coefficient of kinetic friction ($\mu_k$): 0.2
* Acceleration due to gravity ($g$): $\approx 9.8 \text{ m/s}^2$

Because the 5 kg block is tied to the wall, it does not move. The 10 kg block slides underneath it. This means the 10 kg block experiences **two** friction forces: one from the 5 kg block on top of it, and one from the floor beneath it. Both friction forces will act in the opposite direction of the applied force.

### Step 1: Calculate the normal forces
**Normal force between the top and bottom block ($N_1$):**
The 10 kg block is supporting the weight of the 5 kg block.

$$
N_1 = m_1 g = 5 \cdot 9.8 = 49 \text{ N}
$$

**Normal force between the bottom block and the floor ($N_2$):**
The floor is supporting the weight of *both* blocks.

$$
N_2 = (m_1 + m_2)g = (5 + 10) \cdot 9.8 = 15 \cdot 9.8 = 147 \text{ N}
$$

### Step 2: Calculate the friction forces
Now we apply the kinetic friction formula ($f_k = \mu_k N$) for both surfaces.

**Friction from the top block ($f_{k1}$):**

$$
f_{k1} = \mu_k N_1 = 0.2 \cdot 49 = 9.8 \text{ N}
$$

**Friction from the floor ($f_{k2}$):**

$$
f_{k2} = \mu_k N_2 = 0.2 \cdot 147 = 29.4 \text{ N}
$$

### Step 3: Apply Newton's Second Law to the 10 kg block
We want to find the acceleration ($a$) of the bottom block ($m_2$). The net force ($F_{net}$) on the 10 kg block is the applied force pulling it forward, minus the two friction forces pulling it backward.

$$
F_{net} = F_{app} - f_{k1} - f_{k2}
$$

Substitute the values we calculated:

$$
F_{net} = 45 - 9.8 - 29.4
$$

$$
F_{net} = 45 - 39.2 = 5.8 \text{ N}
$$

Now, use Newton's Second Law ($F_{net} = m_2 \cdot a$) to find the acceleration:

$$
5.8 = 10 \cdot a
$$

$$
a = \frac{5.8}{10} = 0.58 \text{ m/s}^2
$$

*(Note: If your professor uses $g = 10 \text{ m/s}^2$ for simplicity instead of 9.8, the frictions would be 10 N and 30 N, resulting in a net force of 5 N and an exact acceleration of $0.5 \text{ m/s}^2$.)*

---

## Final Results Summary

**Friction from the top block:**

$$
f_{k1} = 9.8 \text{ N}
$$

**Friction from the floor:**

$$
f_{k2} = 29.4 \text{ N}
$$

**Net Force on the 10 kg block:**

$$
F_{net} = 5.8 \text{ N}
$$

**Acceleration of the 10 kg block:**

$$
a = 0.58 \text{ m/s}^2
$$
