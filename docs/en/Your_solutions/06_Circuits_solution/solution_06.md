# Kirchhoff's Laws: Current Through an Ammeter

## Necessary Definitions and Formulas

### 1. Kirchhoff's Current Law (KCL)
The sum of all currents entering a junction must equal the sum of all currents leaving the junction.

$$
\sum I_{in} = \sum I_{out}
$$

### 2. Kirchhoff's Voltage Law (KVL)
The algebraic sum of all voltage changes around any closed loop in a circuit must be zero.

$$
\sum \Delta V = 0
$$

---

## Step-by-Step Solution

Based on the circuit diagram, let's identify the components and assign arbitrary current directions. 
* **Left Branch:** Battery $\mathcal{E}_1 = 6\ \text{V}$, Resistor $R_1 = 2\ \Omega$. Let current $I_1$ flow **upwards** (clockwise in the left loop).
* **Right Branch:** Battery $\mathcal{E}_2 = 4\ \text{V}$, Resistor $R_3 = 2\ \Omega$. Let current $I_3$ flow **upwards** (counter-clockwise in the right loop).
* **Middle Branch:** Ammeter, Resistor $R_2 = 2\ \Omega$. Let current $I_2$ flow **downwards** from the top node to the bottom node.

### Step 1: Apply Kirchhoff's Current Law (KCL)
At the top junction, currents $I_1$ and $I_3$ enter the node, and $I_2$ leaves the node:

$$
I_1 + I_3 = I_2
$$

*(Equation 1)*

### Step 2: Apply Kirchhoff's Voltage Law (KVL) to the Loops

**Left Loop (Clockwise):**
Starting from the bottom-left corner and moving clockwise:
* Gain potential across the battery $\mathcal{E}_1$: $+6\ \text{V}$
* Drop across resistor $R_1$: $-2 \cdot I_1$
* Drop across resistor $R_2$: $-2 \cdot I_2$

$$
6 - 2 I_1 - 2 I_2 = 0
$$

Divide the entire equation by 2 to simplify:

$$
3 - I_1 - I_2 = 0 \implies I_1 = 3 - I_2
$$

*(Equation 2)*

**Right Loop (Counter-Clockwise):**
Starting from the bottom-right corner and moving counter-clockwise:
* Gain potential across the battery $\mathcal{E}_2$: $+4\ \text{V}$
* Drop across resistor $R_3$: $-2 \cdot I_3$
* Drop across resistor $R_2$: $-2 \cdot I_2$

$$
4 - 2 I_3 - 2 I_2 = 0
$$

Divide the entire equation by 2 to simplify:

$$
2 - I_3 - I_2 = 0 \implies I_3 = 2 - I_2
$$

*(Equation 3)*

### Step 3: Solve for the Ammeter Current ($I_2$)
We want to find $I_2$, which is the current passing through the ammeter in the middle branch. Substitute the expressions for $I_1$ (Equation 2) and $I_3$ (Equation 3) into our KCL node equation (Equation 1):

$$
(3 - I_2) + (2 - I_2) = I_2
$$

Combine the constant terms and the $I_2$ terms on the left side:

$$
5 - 2 I_2 = I_2
$$

Add $2 I_2$ to both sides of the equation:

$$
5 = 3 I_2
$$

Solve for $I_2$:

$$
I_2 = \frac{5}{3}\ \text{A}
$$

$$
I_2 \approx 1.67\ \text{A}
$$

---

## Final Result

The current flowing through the ammeter is **$1.67\ \text{A}$** (or exactly $5/3\ \text{A}$), flowing downwards through the middle branch.
