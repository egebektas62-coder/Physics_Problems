## 12. Transformer Currents

### Necessary Definitions and Formulas

#### 1. Transformer Voltage Equation
The voltage in a transformer scales strictly according to the ratio of the number of turns in the secondary coil ($N_s$) to the primary coil ($N_p$).

$$
V_s = V_p \cdot \left( \frac{N_s}{N_p} \right)
$$

#### 2. Conservation of Energy (Ideal Transformer)
Instead of relying on the inverse current ratio, we apply the fundamental law of physics: Conservation of Energy. In an ideal transformer with zero power loss, the electrical power entering the primary coil ($P_p$) must perfectly equal the power leaving the secondary coil ($P_s$).

$$
P_p = P_s
$$

Since electrical power is the product of voltage and current ($P = V \cdot I$), this gives us:

$$
V_p \cdot I_p = V_s \cdot I_s
$$

---

### Step-by-Step Solution

Let's identify the given parameters from the problem:
* Primary turns ($N_p$): 1000
* Secondary turns ($N_s$): 200
* Primary voltage ($V_p$): 120 V
* Secondary current ($I_s$): 3 A

#### Step 1: Calculate the Secondary Voltage
First, use the turns ratio to find the voltage at the output (secondary coil).

$$
V_s = 120 \cdot \left( \frac{200}{1000} \right)
$$

$$
V_s = 120 \cdot 0.2
$$

$$
V_s = 24\text{ V}
$$

#### Step 2: Calculate the Power in the Secondary Coil
Now that we have both the voltage and the current for the secondary side, we can calculate its total power output in Watts.

$$
P_s = V_s \cdot I_s
$$

$$
P_s = 24 \cdot 3
$$

$$
P_s = 72\text{ W}
$$

#### Step 3: Calculate the Primary Current using Energy Conservation
By the law of conservation of energy, the primary coil must also be drawing exactly 72 W of power from the source ($P_p = 72\text{ W}$). We use the primary voltage to find the primary current.

$$
P_p = V_p \cdot I_p
$$

$$
72 = 120 \cdot I_p
$$

To isolate $I_p$, divide both sides by 120:

$$
I_p = \frac{72}{120}
$$

$$
I_p = 0.6\text{ A}
$$

---

### Final Results Summary

* **Secondary Voltage:** 24 V
* **Primary Current:** 0.6 A

**Conclusion:** By utilizing the conservation of energy, we verified that a step-down transformer decreases the voltage (from 120 V to 24 V) but proportionally increases the current capacity, maintaining a constant power of 72 W across the entire system.
