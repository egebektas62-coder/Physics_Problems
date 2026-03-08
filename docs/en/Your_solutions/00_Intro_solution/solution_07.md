# 7. Logic & Series: The Fly and the Bicycle

## Necessary Definitions and Formulas

### 1. Kinematic Equation for Constant Velocity
When an object moves at a constant speed, the relationship between distance ($d$), velocity ($v$), and time ($t$) is straightforward. 

$$
d = v \cdot t
$$

This can be rearranged to solve for time:

$$
t = \frac{d}{v}
$$

### 2. The Logical Insight (Time-Based Approach)
This is a classic trick problem. You could calculate the distance of the fly's first trip to the wall, then the distance back to the bicycle (which has moved forward), then back to the wall, creating an infinite geometric series. 

However, the **logical shortcut** is to realize that the fly is in continuous motion exactly for the duration it takes the bicycle to reach the wall. If you know the total time the bicycle travels, you know the total time the fly travels.



---

## Problem Statement

A bicycle is 10 meters from a wall and moves towards it at a constant speed of $1 \text{ m/s}$. A fly starts from the bicycle's front wheel and flies towards the wall at $2 \text{ m/s}$. When it hits the wall, it instantly turns back and flies to the bicycle, and so on. What is the total distance the fly travels before being crushed?

---

## Step-by-Step Solution

### Step 1: Calculate the time the bicycle takes to reach the wall
The problem ends when the bicycle hits the wall. We need to find out how long this takes. We know the bicycle's initial distance from the wall ($d_b$) and its speed ($v_b$).

* Distance $d_b = 10 \text{ m}$
* Speed $v_b = 1 \text{ m/s}$

Using the time formula:

$$
t = \frac{d_b}{v_b}
$$

$$
t = \frac{10}{1}
$$

$$
t = 10 \text{ seconds}
$$

The bicycle will hit the wall in exactly 10 seconds.

### Step 2: Determine the fly's total flight time
Because the fly is flying continuously back and forth from the moment the bicycle starts moving until the bicycle hits the wall, the fly is in the air for exactly 10 seconds.

* Fly's time $t = 10 \text{ seconds}$

### Step 3: Calculate the total distance traveled by the fly
Now that we have the fly's total travel time and its constant speed ($v_f = 2 \text{ m/s}$), we can calculate the total distance the fly covers using the constant velocity formula.

$$
d_f = v_f \cdot t
$$

Substitute the known values:

$$
d_f = 2 \cdot 10
$$

$$
d_f = 20 \text{ meters}
$$

---

## Final Result

By focusing on time rather than the infinite back-and-forth segments, we find that the fly travels a total distance of **20 meters** before being crushed.
