# Superposition Principle: Forming a Standing Wave

## Necessary Definitions and Formulas

### 1. The Principle of Superposition
When two or more waves overlap in space, the resultant disturbance (wave) is equal to the algebraic sum of the individual disturbances. If you have two wave functions $y_1$ and $y_2$, the combined wave is simply:

$$
y_{total}(x, t) = y_1(x, t) + y_2(x, t)
$$

### 2. Standing Wave
A standing wave is formed when two identical traveling waves (same amplitude and frequency) move in opposite directions and interfere with each other. Instead of traveling through space, the resulting wave appears to "stand still," oscillating up and down in place.



### 3. Trigonometric Identity for Sum of Sines
To mathematically combine the two wave equations, we must use the sum-to-product trigonometric identity:

$$
\sin(\alpha) + \sin(\beta) = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right)
$$

### 4. Wave Number ($k$) and Wavelength ($\lambda$)
The wave number $k$ relates to the physical length of the wave:

$$
k = \frac{2\pi}{\lambda}
$$

---

## Problem Statement

Two waves are described by the equations $y_1(x, t) = A \sin(kx - \omega t)$ and $y_2(x, t) = A \sin(kx + \omega t)$. What is the equation of the resulting standing wave? Identify the positions of the nodes.

---

## Step-by-Step Solution

### Step 1: Set up the Superposition Equation
According to the superposition principle, we add the two wave equations:

$$
y(x, t) = y_1(x, t) + y_2(x, t)
$$

$$
y(x, t) = A \sin(kx - \omega t) + A \sin(kx + \omega t)
$$

Factor out the amplitude $A$:

$$
y(x, t) = A \left[ \sin(kx - \omega t) + \sin(kx + \omega t) \right]
$$

### Step 2: Apply the Trigonometric Identity
Let $\alpha = kx - \omega t$ and $\beta = kx + \omega t$. We apply the sum-to-product identity.

First, calculate the sum term:

$$
\frac{\alpha + \beta}{2} = \frac{(kx - \omega t) + (kx + \omega t)}{2} = \frac{2kx}{2} = kx
$$

Next, calculate the difference term:

$$
\frac{\alpha - \beta}{2} = \frac{(kx - \omega t) - (kx + \omega t)}{2} = \frac{-2\omega t}{2} = -\omega t
$$

Substitute these back into the identity:

$$
y(x, t) = A \left[ 2 \sin(kx) \cos(-\omega t) \right]
$$

Since the cosine function is an even function, $\cos(-\omega t) = \cos(\omega t)$. The equation simplifies to:

$$
y(x, t) = 2A \sin(kx) \cos(\omega t)
$$

*Explanation:* This new equation separates space ($x$) and time ($t$). The term $2A \sin(kx)$ dictates the amplitude at any given position, while $\cos(\omega t)$ dictates the up-and-down oscillation over time. This separation is the mathematical proof of a **standing wave**.

### Step 3: Identify the Positions of the Nodes
Nodes are points on the standing wave that *never* move. Their amplitude is always exactly zero, regardless of time ($t$).



To find the nodes, we set the spatial amplitude part of our equation to zero:

$$
2A \sin(kx) = 0 \implies \sin(kx) = 0
$$

The sine function equals zero when its argument is an integer multiple of $\pi$:

$$
kx = n\pi \quad \text{for } n = 0, 1, 2, 3, \dots
$$

Substitute the definition of the wave number $k = \frac{2\pi}{\lambda}$:

$$
\left(\frac{2\pi}{\lambda}\right)x = n\pi
$$

Cancel $\pi$ from both sides and solve for $x$:

$$
\frac{2}{\lambda}x = n
$$

$$
x = \frac{n\lambda}{2}
$$

*Explanation:* The nodes occur at $x = 0$, $x = \frac{\lambda}{2}$, $x = \lambda$, $x = \frac{3\lambda}{2}$, etc. This means there is a dead zone (node) every half-wavelength along the medium.

---

## Final Results Summary

**Equation of the resulting standing wave:**

$$
y(x, t) = 2A \sin(kx) \cos(\omega t)
$$

**Positions of the nodes:**

$$
x = \frac{n\lambda}{2} \quad \text{where } n = 0, 1, 2, \dots
$$
