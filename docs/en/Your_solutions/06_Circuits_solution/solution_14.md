# RLC Circuit and Damped Harmonic Oscillator Analogy

## 1. Differential Equation for the Series RLC Circuit

According to Kirchhoff's Voltage Law (KVL), the sum of the instantaneous voltage drops across the inductor (V_L), resistor (V_R), and capacitor (V_C) must equal the applied voltage source V(t):

$$
V_L(t) + V_R(t) + V_C(t) = V(t)
$$

Using the given variables, we know the voltage across the inductor is proportional to the rate of change of current, and the voltage across the resistor is proportional to the current itself. Substituting these into KVL gives:

$$
L \frac{dI(t)}{dt} + R \cdot I(t) + V_C(t) = V(t)
$$

To form a proper second-order differential equation that directly compares to a mechanical oscillator, we express both I(t) and V_C(t) in terms of the electrical charge Q(t). We know that current is the rate of change of charge and capacitor voltage is proportional to charge.

Substituting the derivatives into our KVL equation yields the fundamental second-order differential equation:

$$
L \frac{d^2Q(t)}{dt^2} + R \frac{dQ(t)}{dt} + \frac{1}{C} Q(t) = V(t)
$$

*(Note: If strictly keeping the prompt's exact variables without converting to charge Q, the system is written as an integro-differential equation):*

$$
L \frac{dI(t)}{dt} + R \cdot I(t) + \frac{1}{C} \int I(t) dt = V(t)
$$

---

## 2. Differential Equation for a Damped Harmonic Oscillator

For a mechanical damped harmonic oscillator, Newton's Second Law yields:

$$
m \frac{d^2x(t)}{dt^2} + b \frac{dx(t)}{dt} + k \cdot x(t) = F(t)
$$

Where:
* m = mass
* b = damping coefficient
* k = spring constant
* x(t) = displacement
* F(t) = external driving force

---

## 3. Analogies Between the Systems

By comparing the two second-order differential equations side-by-side, we see a perfect mathematical parallel. The right side of both equations represents the external driving excitation directly.

| Mechanical Quantity | Electrical Quantity | Physical Role in the System |
| :--- | :--- | :--- |
| **Displacement**, x | **Charge**, Q | The primary state variable responding to the system's dynamics. |
| **Velocity**, v | **Current**, I | The rate of flow or movement in the system. |
| **Mass**, m | **Inductance**, L | **Inertia:** Opposes sudden changes in the state variable. |
| **Damping Constant**, b | **Resistance**, R | **Dissipation:** Removes energy from the system (mechanical friction / electrical heat). |
| **Spring Constant**, k | **Inverse Capacitance**, 1/C | **Restoring Force:** Determines the strength of the system's tendency to return to equilibrium. |
| **Driving Force**, F(t) | **Voltage Source**, V(t) | The external excitation driving the system. |
