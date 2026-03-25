# 2. Range Optimization

## Necessary Definitions and Formulas

### 1. Range Formula
The horizontal range $R$ of a projectile launched from the ground and landing at the same elevation is given by:

$$
R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}
$$

Where:
* **$v_0$**: Initial velocity (constant for this problem)
* **$\theta$**: Launch angle
* **$g$**: Acceleration due to gravity (constant)



### 2. Optimization via Calculus
To find the maximum value of a function $R(\theta)$, we use the first derivative test:
* Find the first derivative with respect to the variable: $R'(\theta) = \frac{dR}{d\theta}$
* Set the derivative equal to zero to find the critical points.
* Use the second derivative test ($R''(\theta) < 0$) to confirm the critical point is a local maximum.

### 3. Chain Rule for Trigonometry
When differentiating trigonometric functions with inner functions, we use the chain rule. For $f(\theta) = \sin(2\theta)$:

$$
\frac{d}{d\theta} [\sin(2\theta)] = \cos(2\theta) \cdot 2 = 2\cos(2\theta)
$$

---

## Problem Statement

For projectile motion, show analytically that the maximum range $R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$ for a given initial velocity is achieved at a launch angle of $45^\circ$.

---

## Step-by-Step Solution

We will prove this using standard calculus optimization techniques.

### Step 1: Define the function to maximize
We treat the initial velocity $v_0$ and gravity $g$ as constants. Our function depends entirely on the launch angle $\theta$:

$$
R(\theta) = \left( \frac{v_0^2}{g} \right) \sin(2\theta)
$$

### Step 2: Find the first derivative
To find the critical points where the range might be at a maximum, we take the derivative of $R$ with respect to $\theta$. Because $\frac{v_0^2}{g}$ is a constant scalar, we only need to differentiate the $\sin(2\theta)$ term:

$$
\frac{dR}{d\theta} = \left( \frac{v_0^2}{g} \right) \cdot \frac{d}{d\theta}[\sin(2\theta)]
$$

Applying the chain rule:

$$
\frac{dR}{d\theta} = \left( \frac{v_0^2}{g} \right) \cdot 2\cos(2\theta)
$$

$$
\frac{dR}{d\theta} = \frac{2v_0^2 \cos(2\theta)}{g}
$$

### Step 3: Find the critical point
To find the angle that maximizes the range, we set the first derivative equal to zero:

$$
\frac{2v_0^2 \cos(2\theta)}{g} = 0
$$

Since $v_0 \neq 0$ (the projectile is moving) and $g \neq 0$, the only way this equation can equal zero is if the cosine term is zero:

$$
\cos(2\theta) = 0
$$

### Step 4: Solve for the launch angle $\theta$
We restrict our physical launch angle $\theta$ to be between $0^\circ$ and $90^\circ$ (the first quadrant). This means $2\theta$ must be between $0^\circ$ and $180^\circ$. 

The cosine of an angle is zero at $90^\circ$ ($\frac{\pi}{2}$ radians). Therefore:

$$
2\theta = 90^\circ
$$

Divide by 2:

$$
\theta = 45^\circ
$$

### Step 5: Verify the maximum using the Second Derivative Test
To formally prove this is a maximum and not a minimum, we find the second derivative of the range function:

$$
\frac{d^2R}{d\theta^2} = \frac{d}{d\theta} \left[ \frac{2v_0^2 \cos(2\theta)}{g} \right]
$$

Applying the chain rule again:

$$
\frac{d^2R}{d\theta^2} = \frac{2v_0^2}{g} \cdot (-\sin(2\theta)) \cdot 2
$$

$$
\frac{d^2R}{d\theta^2} = -\frac{4v_0^2 \sin(2\theta)}{g}
$$

Now, evaluate this second derivative at our critical point $\theta = 45^\circ$:

$$
\frac{d^2R}{d\theta^2} \Bigg|_{\theta=45^\circ} = -\frac{4v_0^2 \sin(90^\circ)}{g} = -\frac{4v_0^2}{g}
$$

Since velocity squared ($v_0^2$) and gravity ($g$) are positive, the entire expression is strictly negative ($< 0$). A negative second derivative confirms that the curve is concave down, meaning $\theta = 45^\circ$ is indeed a **local maximum**.

*(Alternative logical approach: We know the maximum value of the sine function is 1. Therefore, $\sin(2\theta)$ is maximized when $\sin(2\theta) = 1$. The angle whose sine is 1 is $90^\circ$. Setting $2\theta = 90^\circ$ gives $\theta = 45^\circ$.)*

---

## Final Result

By taking the first derivative of the range equation and setting it to zero, we have analytically proven that for any given initial velocity, the maximum horizontal range is achieved precisely at a launch angle of **$45^\circ$**.
