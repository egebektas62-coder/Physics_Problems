# 9. Vertical Throw with Drag Force

## Necessary Definitions and Formulas

### 1. Drag Force (Air Resistance)
In classical mechanics, when an object moves through a fluid (like air), it experiences a drag force that opposes its motion. For relatively low speeds, this drag force is often modeled as directly proportional to the velocity.

**Formula:**

$$
F_d = -kv
$$

Where:
* **$k$**: The drag coefficient (depends on the object's shape and fluid density)
* **$v$**: The velocity of the object



### 2. Terminal Velocity ($v_t$)
When an object falls, it eventually reaches a speed where the upward drag force exactly balances the downward gravitational force, resulting in zero net acceleration. This constant speed is the terminal velocity.

**Formula:**

$$
v_t = \frac{mg}{k}
$$

---

## Problem Statement

We have the equation of motion:

$$
m\frac{dv}{dt} = -mg - kv
$$

with initial conditions $v(0)=v_0$, $x(0)=10$.

* Solve the equation by analytical methods.
* Determine the maximum height.
* Compare with the case without drag.
* Perform a numerical simulation using Python.

---

## Step-by-Step Solution

### Part A: Analytical Solution for Velocity and Position

**Step 1: Solve for Velocity $v(t)$ using Separation of Variables**
We start with the given differential equation:

$$
m\frac{dv}{dt} = -mg - kv
$$

Divide by $m$:

$$
\frac{dv}{dt} = -g - \frac{k}{m}v = -\frac{k}{m} \left( \frac{mg}{k} + v \right)
$$

Separate the variables $v$ and $t$:

$$
\frac{dv}{v + \frac{mg}{k}} = -\frac{k}{m}dt
$$

Integrate both sides:

$$
\int \frac{1}{v + \frac{mg}{k}} \,dv = \int -\frac{k}{m} \,dt
$$

$$
\ln\left|v + \frac{mg}{k}\right| = -\frac{k}{m}t + C_1
$$

Apply the initial condition $v(0) = v_0$ to find the constant $C_1$:

$$
\ln\left(v_0 + \frac{mg}{k}\right) = C_1
$$

Substitute $C_1$ back and solve for $v(t)$:

$$
\ln\left( \frac{v + \frac{mg}{k}}{v_0 + \frac{mg}{k}} \right) = -\frac{k}{m}t
$$

Exponentiate both sides:

$$
v(t) + \frac{mg}{k} = \left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t}
$$

$$
v(t) = \left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t} - \frac{mg}{k}
$$

**Step 2: Solve for Position $x(t)$**
Since $v(t) = \frac{dx}{dt}$, we integrate the velocity function to find position:

$$
x(t) = \int \left[ \left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t} - \frac{mg}{k} \right] \,dt
$$

$$
x(t) = -\frac{m}{k}\left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t} - \frac{mg}{k}t + C_2
$$

Apply the initial condition $x(0) = 10$ to find $C_2$:

$$
10 = -\frac{m}{k}\left(v_0 + \frac{mg}{k}\right)e^0 - 0 + C_2
$$

$$
C_2 = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)
$$

Substitute $C_2$ back to get the final position equation:

$$
x(t) = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)\left(1 - e^{-\frac{k}{m}t}\right) - \frac{mg}{k}t
$$

---

### Part B: Determine Maximum Height ($H_{max}$)

The maximum height occurs when the velocity becomes zero ($v(t_{max}) = 0$).

**Step 1: Find the time to reach maximum height ($t_{max}$)**
Set the velocity equation to 0:

$$
0 = \left(v_0 + \frac{mg}{k}\right)e^{-\frac{k}{m}t_{max}} - \frac{mg}{k}
$$

$$
e^{-\frac{k}{m}t_{max}} = \frac{\frac{mg}{k}}{v_0 + \frac{mg}{k}} = \frac{mg}{kv_0 + mg}
$$

Take the natural log of both sides:

$$
-\frac{k}{m}t_{max} = \ln\left( \frac{mg}{kv_0 + mg} \right) = -\ln\left( 1 + \frac{kv_0}{mg} \right)
$$

$$
t_{max} = \frac{m}{k} \ln\left( 1 + \frac{kv_0}{mg} \right)
$$

**Step 2: Substitute $t_{max}$ into the position equation**
To find $H_{max}$, substitute $t_{max}$ and $e^{-\frac{k}{m}t_{max}}$ into $x(t)$:

$$
H_{max} = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)\left(1 - \frac{mg}{kv_0 + mg}\right) - \frac{mg}{k} \left[ \frac{m}{k} \ln\left( 1 + \frac{kv_0}{mg} \right) \right]
$$

Simplifying the algebraic term yields the final maximum height:

$$
H_{max} = 10 + \frac{mv_0}{k} - \frac{m^2g}{k^2}\ln\left(1 + \frac{kv_0}{mg}\right)
$$

---

### Part C: Comparison with the Case Without Drag

If there is no air resistance ($k = 0$), mechanical energy is conserved. The maximum height without drag is simply derived from kinematics ($v_f^2 = v_i^2 - 2g\Delta x$):

$$
H_{no\_drag} = 10 + \frac{v_0^2}{2g}
$$

**Comparison:**
The maximum height **with drag** is strictly **less than** the maximum height without drag. This is because the non-conservative drag force does negative work on the object as it rises, dissipating some of its initial kinetic energy into heat before it can be converted into gravitational potential energy.

---

### Part D: Numerical Simulation (Python)

You can run this Python script using `scipy` and `matplotlib` to numerically integrate the differential equation and visualize the difference between the drag and no-drag scenarios.

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import solve_ivp

# System parameters
m = 1.0      # Mass (kg)
g = 9.81     # Gravity (m/s^2)
k = 0.2      # Drag coefficient (kg/s)
v0 = 20.0    # Initial velocity (m/s)
x0 = 10.0    # Initial position (m)
t_max = 5.0  # Simulation time (s)

# Differential equation function for solve_ivp
def motion_with_drag(t, y):
    x, v = y
    dxdt = v
    dvdt = -g - (k/m)*v
    return [dxdt, dvdt]

# Solve the numerical integration
t_eval = np.linspace(0, t_max, 500)
sol = solve_ivp(motion_with_drag, [0, t_max], [x0, v0], t_eval=t_eval)

# Theoretical no-drag trajectory for comparison
x_no_drag = x0 + v0*t_eval - 0.5*g*t_eval**2

# Plotting the results
plt.figure(figsize=(10, 6))
plt.plot(sol.t, sol.y[0], label='With Drag ($k=0.2$)', color='red', linewidth=2)
plt.plot(t_eval, x_no_drag, label='No Drag ($k=0$)', color='blue', linestyle='--')

# Formatting
plt.axhline(0, color='black', linewidth=1) # Ground level
plt.ylim(0, max(x_no_drag) + 5)
plt.title('Vertical Throw: Drag vs No Drag')
plt.xlabel('Time (s)')
plt.ylabel('Height (m)')
plt.legend()
plt.grid(True)
plt.show()
