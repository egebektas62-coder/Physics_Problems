# Electric Potential: Multiple Point Charges

## Necessary Definitions and Formulas

### 1. Electric Potential of a Point Charge
Electric potential ($V$) is a scalar quantity that represents the amount of work energy needed to move a unit of electric charge from a reference point to the specific point in an electric field. Unlike electric force or electric field, it is not a vector, meaning direction does not matter—only magnitude and sign.

$$
V = k \frac{q}{r}
$$

Where:
* **$V$**: Electric potential (measured in Volts, V)
* **$k$**: Coulomb's constant ($\approx 8.99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$)
* **$q$**: Point charge (including its positive or negative sign)
* **$r$**: Distance from the charge to the point of observation

### 2. The Superposition Principle for Potential
Because electric potential is a scalar quantity, finding the total potential at a point due to multiple charges is much simpler than finding the net force. You simply calculate the algebraic sum of the individual potentials (keeping their positive or negative signs).

$$
V_{net} = V_1 + V_2 + \dots + V_n = \sum_{i=1}^{n} k \frac{q_i}{r_i}
$$

---

## Problem Statement

Point charges of +1C, -2C, +3C, and -4C are placed at the corners of a square with sides of 1.0 m (in order). Calculate the electric potential at the center of the square.

---

## Step-by-Step Solution

### Step 1: Analyze the Geometry
Let the square have a side length of $a = 1.0 \text{ m}$. We need to find the distance $r$ from each corner to the exact center of the square.

The diagonal $d$ of the square is:

$$
d = \sqrt{a^2 + a^2} = \sqrt{1.0^2 + 1.0^2} = \sqrt{2} \text{ m}
$$

The distance $r$ from any corner to the center is half of the diagonal:

$$
r = \frac{\sqrt{2}}{2} \text{ m} \approx 0.707 \text{ m}
$$

*Explanation:* Because the observation point is at the exact center, all four charges are at the exact same distance $r$ from our point of interest.

### Step 2: Set Up the Superposition Equation
We apply the superposition principle to sum the potentials from all four charges at the center:

$$
V_{net} = k \frac{q_1}{r} + k \frac{q_2}{r} + k \frac{q_3}{r} + k \frac{q_4}{r}
$$

Since $k$ and $r$ are constant for all terms, we can factor them out:

$$
V_{net} = \frac{k}{r} (q_1 + q_2 + q_3 + q_4)
$$

### Step 3: Substitute the Values and Calculate
Substitute the given charge values:
* $q_1 = +1 \text{ C}$
* $q_2 = -2 \text{ C}$
* $q_3 = +3 \text{ C}$
* $q_4 = -4 \text{ C}$

Sum the charges:

$$
\sum q = 1 - 2 + 3 - 4 = -2 \text{ C}
$$

Now, substitute this sum, Coulomb's constant, and the distance $r$ back into the factored equation:

$$
V_{net} = \frac{8.99 \times 10^9}{\frac{\sqrt{2}}{2}} \cdot (-2)
$$

Multiply the numerator by 2 to clear the complex fraction:

$$
V_{net} = \frac{(8.99 \times 10^9) \cdot (-4)}{\sqrt{2}}
$$

Calculate the numerical value:

$$
V_{net} = \frac{-35.96 \times 10^9}{1.414}
$$

$$
V_{net} \approx -25.43 \times 10^9 \text{ V}
$$

*Explanation:* The net electric potential is massively negative because the algebraic sum of the charges heavily favors the negative side ($-2 \text{ C}$ net charge acting at distance $r$). Since potential is a scalar, the specific order of the charges around the corners doesn't actually matter, only their algebraic sum.

---

## Final Results Summary

* **Distance to center ($r$):** $\approx 0.707 \text{ m}$
* **Net Charge Sum:** $-2.0 \text{ C}$
* **Net Electric Potential ($V_{net}$):** $\approx -2.54 \times 10^{10} \text{ V}$ (or $-25.43 \text{ GV}$)
