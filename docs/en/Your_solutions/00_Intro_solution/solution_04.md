# 4. Rearranging Formulas: The Simple Pendulum

## Necessary Definitions and Formulas

### 1. Simple Pendulum Period Formula
The period of a simple pendulum (the time it takes for one complete cycle of a swing) is determined by its length and the acceleration due to gravity. It is independent of the mass of the pendulum bob.



The formula is:

$$
T = 2\pi \sqrt{\frac{L}{g}}
$$

Where:
* **$T$**: Period of the pendulum (time for one full swing)
* **$L$**: Length of the pendulum
* **$g$**: Acceleration due to gravity
* **$\pi$**: The mathematical constant pi (approximately 3.14159)

### 2. Inverse Operations for Algebraic Rearrangement
To isolate a variable in an equation, you must perform the inverse operation to move other terms to the opposite side:
* The inverse of multiplying by $2\pi$ is dividing by $2\pi$.
* The inverse of taking a square root ($\sqrt{x}$) is squaring the term ($x^2$).
* To move a variable from the denominator to the numerator, you can multiply both sides by that variable or use cross-multiplication.

---

## Problem Statement

Rearrange the equation for the period of a simple pendulum to give a formula for $g$ (acceleration due to gravity).

---

## Step-by-Step Solution

### Step 1: Isolate the square root term
We want to get $g$ by itself. The first step is to move the $2\pi$ term to the other side by dividing both sides of the equation by $2\pi$:

$$
\frac{T}{2\pi} = \sqrt{\frac{L}{g}}
$$

### Step 2: Eliminate the square root
To remove the square root over the fraction $\frac{L}{g}$, we must square both sides of the entire equation:

$$
\left(\frac{T}{2\pi}\right)^2 = \left(\sqrt{\frac{L}{g}}\right)^2
$$

Applying the square to the left side gives:

$$
\frac{T^2}{4\pi^2} = \frac{L}{g}
$$

### Step 3: Get $g$ out of the denominator
Currently, $g$ is in the denominator on the right side. To bring it up, we multiply both sides by $g$:

$$
g \cdot \frac{T^2}{4\pi^2} = L
$$

### Step 4: Isolate $g$
Now, we need to move the $\frac{T^2}{4\pi^2}$ fraction to the other side to leave $g$ completely alone. We do this by multiplying both sides by the reciprocal of the fraction, which is $\frac{4\pi^2}{T^2}$:

$$
g = L \cdot \frac{4\pi^2}{T^2}
$$

Which can be written cleanly as:

$$
g = \frac{4\pi^2 L}{T^2}
$$

---

## Final Result

The rearranged formula to solve for the acceleration due to gravity ($g$) is:

$$
g = \frac{4\pi^2 L}{T^2}
$$
