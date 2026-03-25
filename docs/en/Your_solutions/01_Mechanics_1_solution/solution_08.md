# 8. Circular Motion: Centripetal Acceleration

## Necessary Definitions and Formulas

### 1. Uniform Circular Motion
When an object moves in a circular path at a constant speed, it is in uniform circular motion. Even though the speed is constant, the velocity is constantly changing because the *direction* of motion is always changing.

### 2. Centripetal Acceleration ($a_c$)
Because the velocity vector is changing direction, there must be an acceleration. This acceleration always points directly toward the center of the circular path and is called **centripetal acceleration**.



The standard formulas for centripetal acceleration are:

**Using linear velocity ($v$):**

$$
a_c = \frac{v^2}{R}
$$

**Using angular velocity ($\omega$):**

$$
a_c = \omega^2 R
$$

### 3. Angular Velocity ($\omega$) and Period ($T$)
Angular velocity measures how fast the angle changes over time (in radians per second). It relates to the time it takes to complete one full rotation, known as the **Period ($T$)**.

$$
\omega = \frac{2\pi}{T}
$$

---

## Problem Statement

Calculate the centripetal acceleration of a person standing on the Earth's equator. The Earth's radius is approximately 6378 km.

---

## Step-by-Step Solution

### Step 1: Identify given values and convert to standard SI units
To get our final acceleration in meters per second squared ($\text{m/s}^2$), we must convert all our values to meters and seconds.

**Radius of the Earth ($R$):**

$$
R = 6378 \text{ km} = 6,378,000 \text{ meters}
$$

**Period of Earth's rotation ($T$):**
The Earth completes one full rotation roughly every 24 hours. Let's convert this to seconds:

$$
T = 24 \text{ hours} \times 60 \text{ minutes/hour} \times 60 \text{ seconds/minute}
$$

$$
T = 86,400 \text{ seconds}
$$

### Step 2: Calculate the angular velocity ($\omega$)
Using the period, we can find the Earth's angular velocity.

$$
\omega = \frac{2\pi}{T}
$$

$$
\omega = \frac{2\pi}{86400} \text{ rad/s}
$$

$$
\omega \approx 7.272 \times 10^{-5} \text{ rad/s}
$$

### Step 3: Calculate the centripetal acceleration ($a_c$)
Now we substitute both $\omega$ and $R$ into the centripetal acceleration formula:

$$
a_c = \omega^2 R
$$

$$
a_c = \left( \frac{2\pi}{86400} \right)^2 \times 6,378,000
$$

Calculate the squared term first:

$$
a_c \approx (5.288 \times 10^{-9}) \times 6,378,000
$$

$$
a_c \approx 0.0337 \text{ m/s}^2
$$

---

## Final Results Summary

**Earth's Radius in meters ($R$):**

$$
R = 6,378,000 \text{ m}
$$

**Earth's Rotational Period in seconds ($T$):**

$$
T = 86,400 \text{ s}
$$

**Angular Velocity ($\omega$):**

$$
\omega \approx 7.272 \times 10^{-5} \text{ rad/s}
$$

**Centripetal Acceleration ($a_c$):**

$$
a_c \approx 0.0337 \text{ m/s}^2
$$

*(Note: This means the Earth's rotation reduces the effective acceleration due to gravity by about $0.0337 \text{ m/s}^2$ at the equator!)*
