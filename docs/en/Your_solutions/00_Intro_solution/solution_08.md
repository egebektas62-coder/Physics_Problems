# 8. Definite Integrals: Area Under a Curve

## Necessary Definitions and Formulas

### 1. Definite Integral and Area
The definite integral of a continuous, non-negative function $f(x)$ from $x = a$ to $x = b$ represents the exact area under the curve of the graph of $f(x)$ and above the x-axis between those two vertical lines.



The notation for a definite integral is:

$$
\int_{a}^{b} f(x) \,dx
$$

### 2. Fundamental Theorem of Calculus
To evaluate a definite integral, we use the Fundamental Theorem of Calculus:

$$
\int_{a}^{b} f(x) \,dx = F(b) - F(a)
$$

Where $F(x)$ is the antiderivative of $f(x)$.

### 3. Antiderivative of Sine
The antiderivative (or indefinite integral) of $\sin(x)$ is $-\cos(x)$. 

$$
\int \sin(x) \,dx = -\cos(x) + C
$$

### 4. Key Trigonometric Values
To evaluate this specific integral, we need the cosine values at our boundaries (in radians):
* $\cos(0) = 1$
* $\cos(\pi) = -1$

---

## Problem Statement

Calculate the area under the curve of the function $f(x) = \sin(x)$ from $x=0$ to $x=\pi$.

---

## Step-by-Step Solution

### Step 1: Set up the definite integral
We want to find the area under $f(x) = \sin(x)$ between the lower limit $a = 0$ and the upper limit $b = \pi$. This is written as:

$$
\text{Area} = \int_{0}^{\pi} \sin(x) \,dx
$$

### Step 2: Find the antiderivative
Using our formulas, we find the antiderivative of the function $\sin(x)$. We drop the constant of integration ($C$) because it cancels out when calculating a definite integral.

$$
F(x) = -\cos(x)
$$

### Step 3: Evaluate the bounds
Now, apply the Fundamental Theorem of Calculus by evaluating $F(x)$ at the upper bound ($\pi$) and subtracting the value of $F(x)$ at the lower bound ($0$).

$$
\int_{0}^{\pi} \sin(x) \,dx = \left[ -\cos(x) \right]_{0}^{\pi}
$$

$$
= (-\cos(\pi)) - (-\cos(0))
$$

### Step 4: Substitute the trigonometric values
Plug in the known values for $\cos(\pi)$ and $\cos(0)$:

$$
= (-(-1)) - (-1)
$$

Simplify the signs:

$$
= 1 + 1
$$

$$
= 2
$$

---

## Final Result

The exact area under the curve of $f(x) = \sin(x)$ from $x = 0$ to $x = \pi$ is **$2$** square units.
