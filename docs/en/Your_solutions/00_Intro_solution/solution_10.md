# 10. Infinite Series: The Ant's Path

## Necessary Definitions and Formulas

### 1. Infinite Series
An infinite series is the sum of the terms of an infinite sequence. If the sum approaches a specific finite value as more terms are added, the series is said to **converge**.

### 2. Alternating Series
An alternating series is a series whose terms alternate between positive and negative signs. 

### 3. Taylor / Maclaurin Series Expansions
Certain infinite series converge to well-known functions. Two critical expansions centered at zero (Maclaurin series) are needed for this problem:

**The Arctangent Series (Gregory-Leibniz Series):**
For $x = 1$, the series expansion for $\arctan(x)$ is:

$$
\arctan(1) = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots = \frac{\pi}{4}
$$

**The Natural Logarithm Series (Mercator Series):**
For $x = 1$, the series expansion for $\ln(1+x)$ is the alternating harmonic series:

$$
\ln(1+1) = \ln(2) = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \dots
$$



---

## Problem Statement

Determine the final position of an ant that starts at the origin and moves according to the following pattern: 1 m east, 1/2 m north, 1/3 m west, 1/4 m south, 1/5 m east, and so on.

---

## Step-by-Step Solution

To find the final position, we must separate the ant's movement into independent horizontal ($x$-axis) and vertical ($y$-axis) components. 
* East is $+x$, West is $-x$
* North is $+y$, South is $-y$

### Step 1: Analyze the X-axis (Horizontal) movement
The ant moves horizontally on the 1st, 3rd, 5th, 7th... steps.
* Step 1: $+1$ (East)
* Step 3: $-\frac{1}{3}$ (West)
* Step 5: $+\frac{1}{5}$ (East)
* Step 7: $-\frac{1}{7}$ (West)

We can write the total horizontal displacement as an infinite series:

$$
x = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots
$$

### Step 2: Solve the X-axis series
Looking at our definitions, this exact sequence matches the Gregory-Leibniz series for the arctangent of 1. Therefore:

$$
x = \arctan(1)
$$

$$
x = \frac{\pi}{4}
$$

### Step 3: Analyze the Y-axis (Vertical) movement
The ant moves vertically on the 2nd, 4th, 6th, 8th... steps.
* Step 2: $+\frac{1}{2}$ (North)
* Step 4: $-\frac{1}{4}$ (South)
* Step 6: $+\frac{1}{6}$ (North)
* Step 8: $-\frac{1}{8}$ (South)

We can write the total vertical displacement as an infinite series:

$$
y = \frac{1}{2} - \frac{1}{4} + \frac{1}{6} - \frac{1}{8} + \dots
$$

### Step 4: Solve the Y-axis series
This looks similar to the alternating harmonic series, but every denominator is multiplied by 2. We can factor out $\frac{1}{2}$ from the entire series:

$$
y = \frac{1}{2} \left( 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \dots \right)
$$

The expression inside the parentheses is exactly the Maclaurin series for $\ln(2)$. Substituting this in, we get:

$$
y = \frac{1}{2} \ln(2)
$$

Using the properties of logarithms ($a \ln(b) = \ln(b^a)$), this can also be written as:

$$
y = \ln(2^{1/2}) = \ln(\sqrt{2})
$$

---

## Final Result

By evaluating the independent infinite series for both axes, the final coordinates of the ant's position are exactly:

$$
\left( \frac{\pi}{4}, \frac{1}{2}\ln(2) \right)
$$
