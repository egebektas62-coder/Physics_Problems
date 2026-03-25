# 1. Projectile Motion

## Necessary Definitions and Formulas

### 1. Projectile Motion
Projectile motion is a form of motion experienced by an object or particle (a projectile) that is thrown near the Earth's surface and moves along a curved path under the action of gravity only (assuming the effects of air resistance are negligible).



### 2. Newton's Second Law of Motion
The net force acting on an object is equal to the mass of that object multiplied by its acceleration.

$$
\vec{F} = m\vec{a}
$$

### 3. Kinematic Definitions (Calculus)
* **Velocity** is the first derivative of position with respect to time: $\vec{v} = \frac{d\vec{r}}{dt}$
* **Acceleration** is the first derivative of velocity (and second derivative of position) with respect to time: $\vec{a} = \frac{d\vec{v}}{dt} = \frac{d^2\vec{r}}{dt^2}$

### 4. Given Values and Constants
* **Initial velocity ($v_0$)**: **100 m/s**
* **Launch angle ($\theta$)**: **37°**
* **Acceleration due to gravity ($g$)**: Approximately **9.8 m/s²**

*(Note: For classic physics problems, we often use the 3-4-5 right triangle approximations for **37°**, where $\sin(37^\circ) \approx 0.60$ and $\cos(37^\circ) \approx 0.80$. We will use standard decimal values for higher precision, but the calculus method remains the same).*

---

## Step-by-Step Solution

### Part A: Derive the differential equations of motion
Since we are ignoring air resistance, the only force acting on the projectile after it is launched is the downward force of gravity.

**1. Horizontal Direction (x-axis):**
There are no forces acting in the horizontal direction.

$$
F_x = 0
$$

Applying Newton's Second Law ($F = ma$):

$$
m \frac{d^2x}{dt^2} = 0
$$

Dividing by mass ($m$), we get the differential equation for horizontal motion:

$$
\frac{d^2x}{dt^2} = 0
$$

Integrating this once with respect to time ($t$) gives the horizontal velocity. The constant of integration is the initial horizontal velocity, $v_{0x} = v_0 \cos(\theta)$:

$$
v_x(t) = \frac{dx}{dt} = v_0 \cos(\theta)
$$

Integrating a second time gives the horizontal position (assuming initial position $x(0) = 0$):

$$
x(t) = v_0 \cos(\theta) t
$$

**2. Vertical Direction (y-axis):**
The only force is gravity, pulling downwards.

$$
F_y = -mg
$$

Applying Newton's Second Law:

$$
m \frac{d^2y}{dt^2} = -mg
$$

Dividing by mass ($m$), we get the differential equation for vertical motion:

$$
\frac{d^2y}{dt^2} = -g
$$

Integrating once gives the vertical velocity. The constant of integration is the initial vertical velocity, $v_{0y} = v_0 \sin(\theta)$:

$$
v_y(t) = \frac{dy}{dt} = v_0 \sin(\theta) - gt
$$

Integrating a second time gives the vertical position (assuming initial position $y(0) = 0$):

$$
y(t) = v_0 \sin(\theta) t - \frac{1}{2}gt^2
$$

---

### Part B: Determine the time of flight
The time of flight ($T$) is the total time the projectile is in the air. The flight ends when the vertical position is back to zero ($y(T) = 0$).

Set the vertical position equation to zero:

$$
0 = v_0 \sin(\theta) T - \frac{1}{2}gT^2
$$

Factor out $T$:

$$
T \left( v_0 \sin(\theta) - \frac{1}{2}gT \right) = 0
$$

Since $T = 0$ represents the launch time, we solve the other factor for the landing time:

$$
v_0 \sin(\theta) = \frac{1}{2}gT
$$

$$
T = \frac{2v_0 \sin(\theta)}{g}
$$

Now, substitute the given values:

$$
T = \frac{2(100)\sin(37^\circ)}{9.8}
$$

$$
T \approx \frac{200(0.6018)}{9.8} \approx \frac{120.36}{9.8} \approx 12.28 \text{ s}
$$

**Time of flight:** **12.28 seconds**

---

### Part C: Determine the maximum height
Maximum height ($H$) occurs when the projectile stops moving upward and starts falling. At this exact peak, the vertical velocity is zero ($v_y = 0$).

First, find the time it takes to reach the peak ($t_{peak}$):

$$
v_y(t) = v_0 \sin(\theta) - gt_{peak} = 0
$$

$$
t_{peak} = \frac{v_0 \sin(\theta)}{g}
$$

*(Notice this is exactly half the total time of flight).*

Now, plug $t_{peak}$ into the vertical position equation to find $H$:

$$
H = y(t_{peak}) = v_0 \sin(\theta) \left( \frac{v_0 \sin(\theta)}{g} \right) - \frac{1}{2}g \left( \frac{v_0 \sin(\theta)}{g} \right)^2
$$

$$
H = \frac{(v_0 \sin(\theta))^2}{g} - \frac{(v_0 \sin(\theta))^2}{2g}
$$

$$
H = \frac{(v_0 \sin(\theta))^2}{2g}
$$

Substitute the given values:

$$
H = \frac{(100 \times \sin(37^\circ))^2}{2(9.8)}
$$

$$
H \approx \frac{(60.18)^2}{19.6} \approx \frac{3621.63}{19.6} \approx 184.78 \text{ m}
$$

**Maximum height:** **184.78 meters**

---

### Part D: Determine the range
The range ($R$) is the total horizontal distance traveled during the time of flight ($T$).

Plug the time of flight equation ($T$) into the horizontal position equation ($x(t)$):

$$
R = x(T) = v_0 \cos(\theta) \times \left( \frac{2v_0 \sin(\theta)}{g} \right)
$$

$$
R = \frac{v_0^2 (2 \sin(\theta) \cos(\theta))}{g}
$$

Using the trigonometric identity $\sin(2\theta) = 2 \sin(\theta) \cos(\theta)$, we can simplify the range formula:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

Substitute the given values:

$$
R = \frac{(100)^2 \sin(2 \times 37^\circ)}{9.8}
$$

$$
R = \frac{10000 \times \sin(74^\circ)}{9.8}
$$

$$
R \approx \frac{10000 \times 0.9613}{9.8} \approx \frac{9613}{9.8} \approx 980.92 \text{ m}
$$

**Range:** **980.92 meters**
