# 8. Work of a Variable Force: The Spring Force

## Necessary Definitions and Formulas

### 1. Hooke's Law
The force exerted by an ideal spring is directly proportional to its displacement from the equilibrium position, but in the opposite direction. This is a classic example of a **variable force** (a force that changes depending on position).

**Formula:**

$$
F(x) = -kx
$$

Where:
* **$F(x)$**: The restoring force
* **$k$**: The spring constant (stiffness)
* **$x$**: Displacement from equilibrium

### 2. Work Done by a Variable Force
For a force that changes with position, the work done ($W$) cannot be calculated simply by $F \cdot d$. Instead, we must integrate the force over the displacement path.

**Formula:**

$$
W = \int_{x_i}^{x_f} F(x) \,dx
$$

### 3. Potential Energy Relationship
The change in potential energy ($\Delta U$) of a conservative force field is defined as the negative of the work done by that force.

**Formula:**

$$
\Delta U = -W \implies F(x) = -\frac{dU}{dx}
$$

---

## Problem Statement

Given a one-dimensional force:

$$
F(x) = -kx
$$

* Write down the equation of motion and solve it.
* Calculate the work done during the displacement from $0$ to $x_0$.
* Interpret the result as potential energy.
* Verify the relationship $F = -\frac{dU}{dx}$.
* Draw the graph of $F(x)$ and $U(x)$.

---

## Step-by-Step Solution

### Part A: Equation of Motion and its Solution

**Step 1: Write the equation of motion**
Using Newton's Second Law ($F = ma$) and knowing that acceleration $a$ is the second derivative of position $x$ with respect to time $t$ ($a = \frac{d^2x}{dt^2}$):

$$
m\frac{d^2x}{dt^2} = -kx
$$

Rearranging this gives the classic differential equation for Simple Harmonic Motion (SHM):

$$
\frac{d^2x}{dt^2} + \frac{k}{m}x = 0
$$

**Step 2: Solve the differential equation**
We define the angular frequency $\omega$ as:

$$
\omega = \sqrt{\frac{k}{m}}
$$

Substituting this into the equation:

$$
\frac{d^2x}{dt^2} + \omega^2 x = 0
$$

The general solution to this second-order linear differential equation is a sinusoidal function:

$$
x(t) = A \cos(\omega t + \phi)
$$

Where $A$ is the amplitude and $\phi$ is the initial phase angle, both determined by initial conditions.

---

### Part B: Calculate the Work Done

We need to calculate the work done **by the spring force** as the object moves from $x = 0$ to $x = x_0$. 

$$
W = \int_{0}^{x_0} F(x) \,dx
$$

Substitute $F(x) = -kx$:

$$
W = \int_{0}^{x_0} (-kx) \,dx
$$

Evaluate the integral:

$$
W = \left[ -\frac{1}{2}kx^2 \right]_{0}^{x_0}
$$

$$
W = \left( -\frac{1}{2}kx_0^2 \right) - (0)
$$

$$
W = -\frac{1}{2}kx_0^2
$$

*(The work is negative because the force pulls in the opposite direction of the displacement).*

---

### Part C: Interpret as Potential Energy

By definition, the change in potential energy is the negative of the work done by a conservative force:

$$
\Delta U = -W
$$

$$
U(x_0) - U(0) = -\left(-\frac{1}{2}kx_0^2\right)
$$

Assuming the potential energy at equilibrium ($x = 0$) is zero ($U(0) = 0$):

$$
U(x_0) = \frac{1}{2}kx_0^2
$$

This represents the elastic potential energy stored in the spring when it is stretched or compressed to a distance $x_0$.

---

### Part D: Verify the Relationship $F = -\frac{dU}{dx}$

We now have the potential energy function for any arbitrary position $x$:

$$
U(x) = \frac{1}{2}kx^2
$$

Take the negative derivative of $U(x)$ with respect to $x$:

$$
-\frac{dU}{dx} = -\frac{d}{dx}\left(\frac{1}{2}kx^2\right)
$$

Using the power rule for derivatives:

$$
-\frac{dU}{dx} = -\left(\frac{1}{2} \cdot 2kx\right)
$$

$$
-\frac{dU}{dx} = -kx
$$

Since $-kx$ is our original force $F(x)$, the relationship is successfully verified:

$$
F(x) = -\frac{dU}{dx}
$$

---

### Part E: Graph of $F(x)$ and $U(x)$



* **Graph of $F(x) = -kx$:** This is a linear function passing through the origin $(0,0)$. Because $k$ is positive, the slope ($-k$) is negative. It forms a straight line crossing from the second quadrant to the fourth quadrant.
* **Graph of $U(x) = \frac{1}{2}kx^2$:** This is a quadratic function. It forms an upward-opening parabola with its minimum point (vertex) at the origin $(0,0)$. As displacement $x$ increases in either the positive or negative direction, the potential energy $U$ increases quadratically.

---

## Final Results Summary

**Equation of Motion Solution:**

$$
x(t) = A \cos\left(\sqrt{\frac{k}{m}} t + \phi\right)
$$

**Work Done by Force ($0$ to $x_0$):**

$$
W = -\frac{1}{2}kx_0^2
$$

**Potential Energy Function:**

$$
U(x) = \frac{1}{2}kx^2
$$

**Force-Energy Relationship:** Verified successfully.
