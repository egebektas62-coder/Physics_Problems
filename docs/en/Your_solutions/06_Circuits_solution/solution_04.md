## 4. Mixed Circuit

Calculate the equivalent resistance for the circuit shown in the figure. All resistors have a resistance of $10\ \Omega$.

---

### Necessary Definitions and Formulas

To solve this circuit, we break it down into simpler sections using the fundamental rules for series and parallel resistors.

#### 1. Resistors in Series
When resistors are connected end-to-end along a single path, their equivalent resistance is the sum of their individual values:

$$
R_{series} = R_1 + R_2 + \dots
$$

#### 2. Resistors in Parallel
When two resistors are connected across the exact same two electrical nodes, their equivalent resistance is calculated as:

$$
R_{parallel} = \frac{R_1 \cdot R_2}{R_1 + R_2}
$$

---

### Step-by-Step Solution

Let's break the circuit down into distinct sections. The input splits into a **Top Branch** and a **Bottom Branch** which then rejoin at a common node, followed by a **Final Resistor** at the output.

#### Step 1: Analyze the Top Branch
The top branch contains exactly two resistors connected in series. 

$$
R_{top} = 10 + 10 = 20\ \Omega
$$

#### Step 2: Analyze the Bottom Branch
The bottom branch contains one resistor in series with a parallel pair of resistors.
First, calculate the equivalent resistance of the parallel pair:

$$
R_{pair} = \frac{10 \cdot 10}{10 + 10} = \frac{100}{20} = 5\ \Omega
$$

Now, add the first resistor of the bottom branch, which is in series with this pair:

$$
R_{bottom} = 10 + 5 = 15\ \Omega
$$

#### Step 3: Combine the Top and Bottom Branches
The entire Top Branch ($20\ \Omega$) is in parallel with the entire Bottom Branch ($15\ \Omega$). Let's find the equivalent resistance of this central parallel block ($R_{block}$):

$$
R_{block} = \frac{R_{top} \cdot R_{bottom}}{R_{top} + R_{bottom}}
$$

$$
R_{block} = \frac{20 \cdot 15}{20 + 15}
$$

$$
R_{block} = \frac{300}{35} = \frac{60}{7}\ \Omega
$$

#### Step 4: Calculate the Final Equivalent Resistance ($R_{eq}$)
The entire parallel block we just calculated is connected in series with the final rightmost resistor ($10\ \Omega$). We add them together to find the total equivalent resistance of the circuit:

$$
R_{eq} = R_{block} + 10
$$

$$
R_{eq} = \frac{60}{7} + \frac{70}{7}
$$

$$
R_{eq} = \frac{130}{7}\ \Omega
$$

---

### Final Result
**$R_{eq} = \frac{130}{7}\ \Omega$** (or approximately **$18.57\ \Omega$**)
