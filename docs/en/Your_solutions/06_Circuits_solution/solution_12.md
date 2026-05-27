# Transformer Voltages and Currents

## Necessary Definitions and Formulas

### 1. Transformer Voltage Equation
The ratio of the secondary voltage ($V_s$) to the primary voltage ($V_p$) is equal to the ratio of the number of turns in the secondary coil ($N_s$) to the number of turns in the primary coil ($N_p$).

$$
\frac{V_s}{V_p} = \frac{N_s}{N_p}
$$

### 2. Transformer Current Equation (Ideal Transformer)
Assuming an ideal transformer (no power loss, $100\%$ efficiency), the power in the primary coil equals the power in the secondary coil ($P_p = P_s$, meaning $V_p \cdot I_p = V_s \cdot I_s$). Therefore, the current ratio is the inverse of the turns ratio.

$$
\frac{I_p}{I_s} = \frac{N_s}{N_p}
$$

---

## Step-by-Step Solution

Let's identify the given parameters from the problem:
* **Primary turns ($N_p$):** $1000$
* **Secondary turns ($N_s$):** $200$
* **Primary voltage ($V_p$):** $120\ \text{V}$
* **Secondary current ($I_s$):** $3\ \text{A}$

### Step 1: Calculate the Secondary Voltage ($V_s$)
Using the voltage transformer equation, isolate and solve for $V_s$:

$$
V_s = V_p \cdot \left( \frac{N_s}{N_p} \right)
$$

$$
V_s = 120 \cdot \left( \frac{200}{1000} \right)
$$

$$
V_s = 120 \cdot 0.2
$$

**$V_s = 24\ \text{V}$**

### Step 2: Calculate the Primary Current ($I_p$)
Using the current transformer equation, isolate and solve for $I_p$:

$$
I_p = I_s \cdot \left( \frac{N_s}{N_p} \right)
$$

$$
I_p = 3 \cdot \left( \frac{200}{1000} \right)
$$

$$
I_p = 3 \cdot 0.2
$$

**$I_p = 0.6\ \text{A}$**

---

## Final Results Summary

* **Secondary Voltage ($V_s$):** $24\ \text{V}$
* **Primary Current ($I_p$):** $0.6\ \text{A}$
