# Kirchhoff's Laws: Two-Loop Circuit

## Necessary Definitions and Formulas

To solve complex circuits with multiple voltage sources, we use Kirchhoff's Circuit Laws:

### 1. Kirchhoff's Current Law (KCL)
The total current entering a junction (node) must equal the total current leaving the junction.

$$
\sum I_{in} = \sum I_{out}
$$

### 2. Kirchhoff's Voltage Law (KVL)
The directed sum of all voltages around any closed loop in a circuit must be zero.

$$
\sum \Delta V = 0
$$

**Sign Convention for KVL:**
*   Crossing a battery from the short line ($-$) to the long line ($+$) is a voltage **gain** ($+\mathcal{E}$).
*   Crossing a resistor in the same direction as the assumed current is a voltage **drop** ($-I \cdot R$).

---

## Step-by-Step Solution

### Step 1: Define Current Directions and Loops
First, we assign arbitrary directions for the currents in each branch. If a calculated current turns out negative, it simply means its actual direction is opposite to our initial assumption.
*   **$I_1$ (Left Branch):** Assumed to flow **clockwise** (up the left wire, right through $R_1$, toward the top node).
*   **$I_3$ (Right Branch):** Assumed to flow **counter-clockwise** (up the right wire through $\mathcal{E}_2$ and $r_w$, left toward the top node).
*   **$I_2$ (Middle Branch):** Assumed to flow **downward** through $R_2$ (from the top node to the bottom node).

### Step 2: Apply KCL at the Top Node
Currents $I_1$ and $I_3$ are entering the top node, and $I_2$ is leaving it.

$$
I_1 + I_3 = I_2
$$

Which can be rearranged as:

$$
I_3 = I_2 - I_1
$$

### Step 3: Apply KVL to the Loops

**Left Loop (Clockwise path):**
Starting at the bottom-left and moving clockwise:
1. Go right through $R_1$: $-20 I_1$
2. Go down through $R_2$: $-10 I_2$
3. Go left through the bottom wire, crossing the battery $\mathcal{E}_1$ from $-$ to $+$ (short to long line): $+4.5\ \text{V}$
4. Go left through internal resistance $r_w$: $-1 I_1$

$$
-20I_1 - 10I_2 + 4.5 - 1I_1 = 0
$$

Simplify the Left Loop equation:

$$
21I_1 + 10I_2 = 4.5 \quad \text{--- (Equation 1)}
$$

**Right Loop (Counter-clockwise path):**
Starting at the bottom-right and moving counter-clockwise:
1. Go up through the battery $\mathcal{E}_2$ from $-$ to $+$: $+9\ \text{V}$
2. Go up through internal resistance $r_w$: $-1 I_3$
3. Go down through the shared middle branch $R_2$: $-10 I_2$

$$
9 - 1I_3 - 10I_2 = 0
$$

Simplify the Right Loop equation:

$$
I_3 + 10I_2 = 9 \quad \text{--- (Equation 2)}
$$

### Step 4: Solve the System of Equations
Substitute $I_3$ from the KCL equation ($I_3 = I_2 - I_1$) into Equation 2:

$$
(I_2 - I_1) + 10I_2 = 9
$$

$$
-I_1 + 11I_2 = 9
$$

Isolate $I_1$:

$$
I_1 = 11I_2 - 9
$$

Now, substitute this expression for $I_1$ into Equation 1:

$$
21(11I_2 - 9) + 10I_2 = 4.5
$$

$$
231I_2 - 189 + 10I_2 = 4.5
$$

$$
241I_2 = 193.5
$$

$$
I_2 = \frac{193.5}{241} \approx 0.803\ \text{A}
$$

Now substitute $I_2$ back to find $I_1$:

$$
I_1 = 11 \left(\frac{193.5}{241}\right) - 9
$$

$$
I_1 = \frac{2128.5}{241} - \frac{2169}{241}
$$

$$
I_1 = \frac{-40.5}{241} \approx -0.168\ \text{A}
$$

*(The negative sign means $I_1$ actually flows counter-clockwise in the left loop, not clockwise).*

Finally, calculate $I_3$:

$$
I_3 = I_2 - I_1
$$

$$
I_3 = \frac{193.5}{241} - \left(\frac{-40.5}{241}\right)
$$

$$
I_3 = \frac{234}{241} \approx 0.971\ \text{A}
$$

---

## Final Results Summary

*   **$I_1$ (Left branch current):** $\approx -0.168\ \text{A}$ (Flows outward from the top node to the left)
*   **$I_2$ (Middle branch current):** $\approx 0.803\ \text{A}$ (Flows downward)
*   **$I_3$ (Right branch current):** $\approx 0.971\ \text{A}$ (Flows inward from the right to the top node)
