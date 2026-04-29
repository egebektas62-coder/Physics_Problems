# Field at a Point from a System of Charges

## Necessary Definitions and Formulas

### 1. Electric Field of a Point Charge
The electric field vector $\vec{E}$ created by a point charge $q$ at a position vector $\vec{r}$ is given by Coulomb's constant $k$, the charge $q$, and the inverse square of the distance.

$$
\vec{E} = k \frac{q}{r^2} \hat{r} = k \frac{q}{r^3} \vec{r}
$$

### 2. The Superposition Principle for Electric Fields
The total electric field at any point in space due to a system of point charges is the vector sum of the individual electric fields created by each charge.

$$
\vec{E}_{total} = \vec{E}_1 + \vec{E}_2
$$



---

## Problem Statement

Two point charges are given:
* $+q$ at point $(-a, 0)$
* $+2q$ at point $(a, 0)$

1. Determine the field vector $\vec{E}(0, y)$, $\vec{E}(x, 0)$ and generally $\vec{E}(x, y)$.
2. Determine the condition for which the components $E_x = 0$, $E_y = 0$ and the zero field $\vec{E} = 0$.
3. Calculate the field for: $a = 0.2\,\text{m}$, $y = 0.3\,\text{m}$, $q = 2\,\mu\text{C}$.
4. Investigate the limit $y \gg a$.

---

## Step-by-Step Solution

### Part 1: Determine the Field Vectors

**General Case $\vec{E}(x, y)$:**
Let the observation point be $P(x, y)$. 
* The vector from $+q$ to $P$ is $\vec{r}_1 = (x+a)\hat{i} + y\hat{j}$.
* The vector from $+2q$ to $P$ is $\vec{r}_2 = (x-a)\hat{i} + y\hat{j}$.

Using the electric field formula for both charges and summing them:

$$
\vec{E}(x,y) = kq \left[ \frac{(x+a)\hat{i} + y\hat{j}}{((x+a)^2 + y^2)^{3/2}} \right] + k(2q) \left[ \frac{(x-a)\hat{i} + y\hat{j}}{((x-a)^2 + y^2)^{3/2}} \right]
$$

Separating into $x$ and $y$ components:

$$
E_x(x,y) = kq \left[ \frac{x+a}{((x+a)^2+y^2)^{3/2}} + \frac{2(x-a)}{((x-a)^2+y^2)^{3/2}} \right]
$$

$$
E_y(x,y) = kqy \left[ \frac{1}{((x+a)^2+y^2)^{3/2}} + \frac{2}{((x-a)^2+y^2)^{3/2}} \right]
$$

**On the y-axis $\vec{E}(0, y)$:**
Set $x = 0$ in the general equations:

$$
E_x(0,y) = kq \left[ \frac{a}{(a^2+y^2)^{3/2}} - \frac{2a}{(a^2+y^2)^{3/2}} \right] = \frac{-kqa}{(a^2+y^2)^{3/2}}
$$

$$
E_y(0,y) = kqy \left[ \frac{1}{(a^2+y^2)^{3/2}} + \frac{2}{(a^2+y^2)^{3/2}} \right] = \frac{3kqy}{(a^2+y^2)^{3/2}}
$$

**On the x-axis $\vec{E}(x, 0)$:**
Set $y = 0$. The $y$-component vanishes entirely ($E_y = 0$).

$$
E_x(x,0) = kq \left[ \frac{x+a}{|x+a|^3} + \frac{2(x-a)}{|x-a|^3} \right]
$$

*(Note: The absolute value is required because distance is always positive, but the direction of the vector depends on which side of the charge the observation point lies).*

---

### Part 2: Conditions for Zero Field Components

**Condition for $E_y = 0$:**
Looking at the $E_y(x,y)$ formula, the term inside the brackets is a sum of two strictly positive magnitudes. Therefore, the only way for $E_y = 0$ is if the multiplier outside is zero:

$$
y = 0
$$

*(The y-component of the field is only zero on the x-axis).*

**Condition for $E_x = 0$:**
This must occur on the x-axis ($y=0$) between the two positive charges, where their repulsive forces oppose each other. Let $-a < x < a$.
Setting the magnitudes of the two opposing fields equal:

$$
k \frac{q}{(x+a)^2} = k \frac{2q}{(a-x)^2}
$$

Cancel $kq$ and take the square root of both sides (choosing positive roots for physical distance):

$$
\frac{1}{x+a} = \frac{\sqrt{2}}{a-x}
$$

Cross-multiply and solve for $x$:

$$
a - x = \sqrt{2}x + \sqrt{2}a
$$

$$
x(1+\sqrt{2}) = a(1-\sqrt{2})
$$

$$
x = a \frac{1-\sqrt{2}}{1+\sqrt{2}} = -a(3 - 2\sqrt{2}) \approx -0.172a
$$

**Condition for $\vec{E} = 0$ (The Dead Zone):**
For the total vector field to be zero, both $E_x$ and $E_y$ must be zero simultaneously.

$$
\text{Zero Field Coordinate: } (x, y) = (-a(3 - 2\sqrt{2}), 0)
$$

---

### Part 3: Calculation

Given: $a = 0.2\,\text{m}$, $y = 0.3\,\text{m}$, $q = 2 \times 10^{-6}\,\text{C}$, and $x = 0$ (calculating for $\vec{E}(0,y)$). Use $k \approx 8.99 \times 10^9\,\text{N}\cdot\text{m}^2/\text{C}^2$.

First, calculate the common denominator term $(a^2 + y^2)^{3/2}$:

$$
(0.2^2 + 0.3^2)^{3/2} = (0.04 + 0.09)^{3/2} = (0.13)^{3/2} \approx 0.04687 \text{ m}^3
$$

Calculate $E_x(0, 0.3)$:

$$
E_x = \frac{-(8.99 \times 10^9)(2 \times 10^{-6})(0.2)}{0.04687} = \frac{-3596}{0.04687} \approx -76,723 \text{ V/m}
$$

Calculate $E_y(0, 0.3)$:

$$
E_y = \frac{3(8.99 \times 10^9)(2 \times 10^{-6})(0.3)}{0.04687} = \frac{16182}{0.04687} \approx 345,253 \text{ V/m}
$$

*Explanation:* At this specific point on the y-axis, the electric field is pointing strongly upwards and slightly to the left.

---

### Part 4: Investigate the Limit $y \gg a$

Let's look at the field on the y-axis when $y$ is extremely large compared to the distance $a$. We take the expressions for $E_x$ and $E_y$ and approximate the denominator:
If $y \gg a$, then $a^2 + y^2 \approx y^2$. The denominator becomes $(y^2)^{3/2} = y^3$.

**For $E_y$:**

$$
E_y \approx \frac{3kqy}{y^3} = \frac{k(3q)}{y^2}
$$

**For $E_x$:**

$$
E_x \approx \frac{-kqa}{y^3}
$$

*Explanation:* From a macroscopic distance, the $y$-component behaves exactly like the electric field of a single "monopole" point charge with a total charge of $(q + 2q) = 3q$. The $x$-component drops off much faster ($1/y^3$) because it represents a residual "dipole" effect caused by the spatial asymmetry of the charges. At massive distances, the network abstracts the two individual nodes and treats them as a single cluster of charge $3q$.
