# Mixed Circuit: Equivalent Resistance

## Necessary Definitions and Formulas

Before diving into the math, we need to recognize the specific layout of this circuit. It is a classic **Wheatstone Bridge**.

### 1. Resistors in Series
When resistors are connected end-to-end, their total resistance adds up:

$$
R_{series} = R_1 + R_2
$$

### 2. Resistors in Parallel
When resistors are connected across the same two nodes, the equivalent resistance is calculated as:

$$
R_{parallel} = \frac{R_1 \cdot R_2}{R_1 + R_2}
$$

### 3. Balanced Wheatstone Bridge
If a circuit has a bridge-like structure (as in the given figure), we must check the ratio of the opposing arms. If the ratios are equal, the bridge is **balanced**:

$$
\frac{R_1}{R_4} = \frac{R_2}{R_5}
$$

**Crucial Rule:** In a balanced Wheatstone bridge, the electrical potential (voltage) on both sides of the middle resistor ($R_3$) is identical. Since there is no potential difference, **no current flows through the middle resistor**. Therefore, $R_3$ acts like an open circuit and can be completely removed from our calculations!

---

## Step-by-Step Solution

Let's extract our known variables. The problem states that ALL resistors have a resistance of **$5\ \Omega$**:
* $R_1 = 5\ \Omega$
* $R_2 = 5\ \Omega$
* $R_3 = 5\ \Omega$
* $R_4 = 5\ \Omega$
* $R_5 = 5\ \Omega$

### Step 1: Check if the bridge is balanced
We test the condition for a balanced Wheatstone bridge using our values:

$$
\frac{R_1}{R_4} = \frac{R_2}{R_5}
$$

$$
\frac{5}{5} = \frac{5}{5} \implies 1 = 1
$$

Because the ratios are perfectly equal, the bridge is balanced.

### Step 2: Redraw/Simplify the circuit (Remove $R_3$)
Since the bridge is balanced, the voltage at the top node (between $R_1$ and $R_2$) equals the voltage at the bottom node (between $R_4$ and $R_5$). No current passes through $R_3$. We virtually "cut" $R_3$ out of the circuit.

Now, the simplified circuit consists of:
* A top branch with $R_1$ and $R_2$ in series.
* A bottom branch with $R_4$ and $R_5$ in series.
* These two branches are in parallel with each other.

### Step 3: Calculate the resistance of the branches
Calculate the equivalent resistance for the top branch ($R_{top}$) and bottom branch ($R_{bottom}$).

**Top Branch:**

$$
R_{top} = R_1 + R_2
$$

$$
R_{top} = 5 + 5 = 10\ \Omega
$$

**Bottom Branch:**

$$
R_{bottom} = R_4 + R_5
$$

$$
R_{bottom} = 5 + 5 = 10\ \Omega
$$

### Step 4: Calculate the total equivalent resistance ($R_{eq}$)
Finally, we find the equivalent resistance of $R_{top}$ and $R_{bottom}$ which are now in parallel.

$$
R_{eq} = \frac{R_{top} \cdot R_{bottom}}{R_{top} + R_{bottom}}
$$

$$
R_{eq} = \frac{10 \cdot 10}{10 + 10}
$$

$$
R_{eq} = \frac{100}{20}
$$

**$R_{eq} = 5\ \Omega$**
