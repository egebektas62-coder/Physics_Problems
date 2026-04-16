# Waves: Checking Validity using the Wave Equation

## Necessary Definitions and Formulas

### 1. The Classical Wave Equation
In physics, any function $y(x,t)$ that describes a traveling wave must satisfy the one-dimensional linear wave equation. This is a second-order partial differential equation:

$$
\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}
$$

* **$\frac{\partial^2 y}{\partial x^2}$**: The second partial derivative with respect to spatial position $x$ (concavity of the wave).
* **$\frac{\partial^2 y}{\partial t^2}$**: The second partial derivative with respect to time $t$ (acceleration of the wave's particles).
* **$v$**: The speed of the wave propagation.

### 2. D'Alembert's Solution (The Quick Check)
A mathematical shortcut states that any function representing a traveling wave without distortion must be a function of the combined variable $(x - vt)$ for a wave traveling to the right, or $(x + vt)$ for a wave traveling to the left. 

If a function can be written entirely as $f(x \pm vt)$, it will automatically satisfy the wave equation.

---

## Problem Statement

Which of the following functions can describe a traveling wave? Hint: check if it satisfies the wave equation:

$$
\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}
$$

a) $y(x,t) = A \cos(kx^2 - \omega t)$

b) $y(x,t) = A(x-vt)^2$

c) $y(x,t) = A \log(x+vt)$

---

## Step-by-Step Solution

We will test each function by taking its second partial derivative with respect to $x$ and its second partial derivative with respect to $t$, and then checking if they satisfy the wave equation.

### Case a) $y(x,t) = A \cos(kx^2 - \omega t)$

**1. Find the spatial derivatives (w.r.t $x$):**
Using the chain rule, the first derivative is:

$$
\frac{\partial y}{\partial x} = -A \sin(kx^2 - \omega t) \cdot (2kx)
$$

Now apply the product rule for the second derivative:

$$
\frac{\partial^2 y}{\partial x^2} = -2Ak \sin(kx^2 - \omega t) - 4Ak^2x^2 \cos(kx^2 - \omega t)
$$

**2. Find the time derivatives (w.r.t $t$):**
First derivative:

$$
\frac{\partial y}{\partial t} = -A \sin(kx^2 - \omega t) \cdot (-\omega) = A\omega \sin(kx^2 - \omega t)
$$

Second derivative:

$$
\frac{\partial^2 y}{\partial t^2} = -A\omega^2 \cos(kx^2 - \omega t)
$$

**3. Check the equation:**
Comparing $\frac{\partial^2 y}{\partial x^2}$ and $\frac{\partial^2 y}{\partial t^2}$, it is clear that multiplying the time derivative by $1/v^2$ will **never** equal the complex spatial derivative (which contains an extra sine term and an $x^2$ multiplier). 

**Conclusion:** **DOES NOT** describe a traveling wave. *(Notice it doesn't fit the $f(x \pm vt)$ format because $x$ is squared while $t$ is not).*

---

### Case b) $y(x,t) = A(x-vt)^2$

**1. Find the spatial derivatives (w.r.t $x$):**

$$
\frac{\partial y}{\partial x} = 2A(x-vt)
$$

$$
\frac{\partial^2 y}{\partial x^2} = 2A
$$

**2. Find the time derivatives (w.r.t $t$):**
Chain rule pulls out a $(-v)$:

$$
\frac{\partial y}{\partial t} = 2A(x-vt) \cdot (-v) = -2Av(x-vt)
$$

$$
\frac{\partial^2 y}{\partial t^2} = -2Av \cdot (-v) = 2Av^2
$$

**3. Check the equation:**
Plug these into the wave equation:

$$
2A = \frac{1}{v^2} (2Av^2)
$$

$$
2A = 2A
$$

The left side equals the right side!

**Conclusion:** **DOES** describe a traveling wave. *(It represents a parabolic pulse moving to the right).*

---

### Case c) $y(x,t) = A \log(x+vt)$

**1. Find the spatial derivatives (w.r.t $x$):**

$$
\frac{\partial y}{\partial x} = A \frac{1}{x+vt}
$$

$$
\frac{\partial^2 y}{\partial x^2} = -A \frac{1}{(x+vt)^2}
$$

**2. Find the time derivatives (w.r.t $t$):**
Chain rule pulls out a $(v)$:

$$
\frac{\partial y}{\partial t} = A \frac{v}{x+vt}
$$

$$
\frac{\partial^2 y}{\partial t^2} = -A \frac{v \cdot v}{(x+vt)^2} = -A \frac{v^2}{(x+vt)^2}
$$

**3. Check the equation:**
Plug these into the wave equation:

$$
-A \frac{1}{(x+vt)^2} = \frac{1}{v^2} \left( -A \frac{v^2}{(x+vt)^2} \right)
$$

$$
-A \frac{1}{(x+vt)^2} = -A \frac{1}{(x+vt)^2}
$$

The left side perfectly equals the right side!

**Conclusion:** **DOES** describe a traveling wave. *(It represents a logarithmic pulse moving to the left).*

---

## Final Results Summary

* **Function a:** Does **NOT** describe a traveling wave.
* **Function b:** **DOES** describe a traveling wave.
* **Function c:** **DOES** describe a traveling wave.
