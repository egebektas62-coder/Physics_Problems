# Mixed Circuit: Equivalent Resistance (Diamond Layout)

## Necessary Definitions and Formulas

Although the visual layout is different, analyzing the nodes reveals that this circuit is another classic **Wheatstone Bridge**.

### 1. Resistors in Series
When resistors are in the same path with no junctions in between:

$$
R_{series} = R_1 + R_2
$$

### 2. Resistors in Parallel
When resistors share the same starting and ending nodes:

$$
R_{parallel} = \frac{R_1 \cdot R_2}{R_1 + R_2}
$$

### 3. Balanced Wheatstone Bridge Condition
If the ratio of the resistances on the two parallel legs is equal, the bridge is balanced:

$$
\frac{R_1}{R_4} = \frac{R_2}{R_5}
$$

If balanced, the middle resistor (the "bridge") has zero potential difference across it. Therefore, no current flows through it, and it behaves as an open circuit (it can be removed).

---

## Step-by-Step Solution

Let's label the resistors based on the standard Wheatstone Bridge topology. The problem states that ALL resistors have a resistance of **$10\ \Omega$**:
* $R_1$ (Top-left) = $10\ \Omega$
* $R_2$ (Top-right) = $10\ \Omega$
* $R_3$ (Middle/Bridge) = $10\ \Omega$
* $R_4$ (Bottom-left) = $10\ \Omega$
* $R_5$ (Bottom-right) = $10\ \Omega$

### Step 1: Check if the bridge is balanced
We test the balanced condition using our left and right ratios:

$$
\frac{R_1}{R_4} = \frac{R_2}{R_5}
$$

$$
\frac{10}{10} = \frac{10}{10} \implies 1 = 1
$$

The condition is met. The bridge is perfectly balanced.

### Step 2: Simplify the circuit
Because the bridge is balanced, the voltage at the top junction equals the voltage at the bottom junction. No current flows through the middle resistor ($R_3$). We can virtually remove $R_3$ from our calculations.

The circuit now simplifies to two parallel branches:
* **Top Branch:** $R_1$ and $R_2$ are now in series.
* **Bottom Branch:** $R_4$ and $R_5$ are now in series.

### Step 3: Calculate the resistance of each branch

**Top Branch ($R_{top}$):**

$$
R_{top} = R_1 + R_2
$$

$$
R_{top} = 10 + 10 = 20\ \Omega
$$

**Bottom Branch ($R_{bottom}$):**

$$
R_{bottom} = R_4 + R_5
$$

$$
R_{bottom} = 10 + 10 = 20\ \Omega
$$

### Step 4: Calculate the total equivalent resistance ($R_{eq}$)
Now, we find the equivalent resistance of the $20\ \Omega$ top branch and the $20\ \Omega$ bottom branch, which are in parallel.

$$
R_{eq} = \frac{R_{top} \cdot R_{bottom}}{R_{top} + R_{bottom}}
$$

$$
R_{eq} = \frac{20 \cdot 20}{20 + 20}
$$

$$
R_{eq} = \frac{400}{40}
$$

**$R_{eq} = 10\ \Omega$**
