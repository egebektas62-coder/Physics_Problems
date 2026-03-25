
# 5. Relative Velocity: Crossing a River

## Necessary Definitions and Formulas

### 1. Relative Velocity
Relative velocity describes how the velocity of one object appears from the perspective of another moving object or reference frame. The fundamental vector equation for relative velocity is:

$$
\vec{v}_{A/C} = \vec{v}_{A/B} + \vec{v}_{B/C}
$$

For this specific problem:
* **$\vec{v}_{b/e}$**: Velocity of the boat relative to the Earth (the true path)
* **$\vec{v}_{b/r}$**: Velocity of the boat relative to the river (the heading in still water)
* **$\vec{v}_{r/e}$**: Velocity of the river relative to the Earth (the current)

This gives us the vector addition equation:

$$
\vec{v}_{b/e} = \vec{v}_{b/r} + \vec{v}_{r/e}
$$



### 2. Trigonometry for Right Triangles
When vectors form a right triangle, we can use basic trigonometric ratios (SOH CAH TOA) and the Pythagorean theorem:
* $\sin(\theta) = \frac{\text{Opposite}}{\text{Hypotenuse}}$
* $\cos(\theta) = \frac{\text{Adjacent}}{\text{Hypotenuse}}$
* $a^2 + b^2 = c^2$

### 3. Constant Velocity Kinematics
For an object moving at a constant speed, the time $t$ it takes to travel a distance $d$ is:

$$
t = \frac{d}{v}
$$

---

## Problem Statement

A river flows east at **2 m/s**. A boat that can travel at **5 m/s** in still water wants to go directly north across the river. In what direction (angle) should it head? How long will it take to cross the river if it's **200 meters** wide?

---

## Step-by-Step Solution

### Step 1: Define the vector components and goal
* The river flows East: $\vec{v}_{r/e} =$ **2 m/s** (x-direction)
* The boat's speed relative to the water is the hypotenuse: $|\vec{v}_{b/r}| =$ **5 m/s**
* The goal is for the true path ($\vec{v}_{b/e}$) to be *strictly North*. 

Because the river pushes the boat East, the boat must aim West of North to counteract the current. The Eastward component of the river and the Westward component of the boat's heading must perfectly cancel each other out.

### Step 2: Calculate the heading angle ($\theta$)
Let $\theta$ be the angle the boat must point West of North. 

The horizontal (Westward) component of the boat's velocity must equal the river's speed (Eastward):

$$
|\vec{v}_{b/r}| \sin(\theta) = |\vec{v}_{r/e}|
$$

Substitute the known speeds:

$$
5 \sin(\theta) = 2
$$

Isolate $\sin(\theta)$:

$$
\sin(\theta) = \frac{2}{5} = 0.4
$$

Take the inverse sine ($\arcsin$) to find the angle:

$$
\theta = \arcsin(0.4) \approx 23.58^\circ
$$

### Step 3: Calculate the resultant northward velocity
To find out how long the trip takes, we need to know the actual speed the boat travels strictly North across the river. This is the vertical component of the boat's velocity, which forms the adjacent side of our right triangle.

We can find this using the Pythagorean theorem:

$$
v_{North}^2 + v_{East}^2 = v_{Hypotenuse}^2
$$

$$
v_{North}^2 + 2^2 = 5^2
$$

$$
v_{North}^2 + 4 = 25
$$

$$
v_{North}^2 = 21
$$

$$
v_{North} = \sqrt{21} \approx 4.58 \text{ m/s}
$$

*(Alternatively, you could use $v_{North} = 5 \cos(23.58^\circ)$, which yields the same result).*

### Step 4: Calculate the time to cross
Now that we have the northward velocity ($v_{North} = \sqrt{21}$ m/s) and the straight-line northward distance across the river ($d =$ **200 m**), we can find the time $t$.

$$
t = \frac{d}{v_{North}}
$$

Substitute the values:

$$
t = \frac{200}{\sqrt{21}}
$$

$$
t \approx \frac{200}{4.58} \approx 43.64 \text{ s}
$$

---

## Final Result

* **Direction (Angle)**: The boat should head approximately **23.58° West of North** to travel directly across the river.
* **Time to Cross**: It will take exactly **$\frac{200}{\sqrt{21}}$ seconds**, which is approximately **43.64 seconds**.
