# Solving a Proportionality Problem: Universal Law of Gravitation



## Necessary Definitions & Formulas

**Newton's Law of Universal Gravitation:** A fundamental principle of physics stating that every particle attracts every other particle in the universe with a force that is directly proportional to the product of their masses and inversely proportional to the square of the distance between their centers.

The formula is defined as:

$$
F = G \frac{m_1 m_2}{r^2}
$$

Where:
* $F$ is the gravitational force between the two masses.
* $G$ is the gravitational constant.
* $m_1$ and $m_2$ are the two masses.
* $r$ is the distance between the centers of the two masses.

**Direct Proportionality:** When one quantity increases, the other increases at the same rate. In this formula, force ($F$) is directly proportional to the product of the masses ($m_1 \cdot m_2$).

**Inverse Square Proportionality:** When one quantity increases, the other decreases by the square of that factor. In this formula, force ($F$) is inversely proportional to the square of the distance ($r^2$).

---

## Problem Statement

Determine the factor by which the force $F$ changes if the distance $r$ is *doubled* and both masses ($m_1$ and $m_2$) are *halved*.

---

## Step-by-Step Solution

### Step 1: Establish the initial equation
Let the initial gravitational force be $F_{initial}$. This represents the system before any changes are made.

$$
F_{initial} = G \frac{m_1 m_2}{r^2}
$$

### Step 2: Define the new variables
According to the problem, we need to apply specific changes to our variables:
* The distance $r$ is doubled: Let $r_{new} = 2r$
* Mass $m_1$ is halved: Let $m_{1,new} = \frac{1}{2}m_1$
* Mass $m_2$ is halved: Let $m_{2,new} = \frac{1}{2}m_2$

### Step 3: Substitute the new variables into the formula
We now set up the equation for the new gravitational force, $F_{new}$, using our modified variables.

$$
F_{new} = G \frac{m_{1,new} \cdot m_{2,new}}{(r_{new})^2}
$$

Substitute the definitions from Step 2 into this equation:

$$
F_{new} = G \frac{(\frac{1}{2}m_1)(\frac{1}{2}m_2)}{(2r)^2}
$$

### Step 4: Simplify the numerator and the denominator
First, multiply the terms in the numerator (the masses):

$$
(\frac{1}{2}m_1)(\frac{1}{2}m_2) = \frac{1}{4}m_1 m_2
$$

Next, square the term in the denominator (the distance):

$$
(2r)^2 = 2^2 \cdot r^2 = 4r^2
$$

Now, put these simplified pieces back into the equation for $F_{new}$:

$$
F_{new} = G \frac{\frac{1}{4}m_1 m_2}{4r^2}
$$

### Step 5: Isolate the original equation
To find the factor of change, we need to extract the original formula ($G \frac{m_1 m_2}{r^2}$) from our new equation. 

Divide the fraction in the numerator by the denominator:

$$
\frac{\frac{1}{4}}{4} = \frac{1}{4} \cdot \frac{1}{4} = \frac{1}{16}
$$

Bring this constant to the front:

$$
F_{new} = \frac{1}{16} \left( G \frac{m_1 m_2}{r^2} \right)
$$

### Step 6: Conclude the final factor
Since the term inside the parentheses is exactly equal to our initial force ($F_{initial}$), we can substitute it back in:

$$
F_{new} = \frac{1}{16} F_{initial}
$$

---

## Final Answer

By halving both masses and doubling the distance, the new gravitational force becomes **$\frac{1}{16}$** of the original force. The force decreases by a factor of 16.
