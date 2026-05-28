## 3. Mixed Circuit

Calculate the equivalent resistance for the circuit shown in the figure. All resistors have a resistance of $5\ \Omega$.

---

### Topology Analysis & Node Identification

To solve this circuit accurately, we must identify the electrical nodes (represented by the thick black dots) and count every distinct resistor block drawn. There are exactly **8 resistors** in this diagram. 

Let's label the three main junctions (nodes):
* **Node L (Left Input):** The dot on the bottom-left. It connects the input terminal, the upward left branch, and the inner rightward branch.
* **Node T (Top Center):** The dot on the top wire. It connects the upper-left branch, the inner vertical branch, and the rightward branch.
* **Node R (Right Output):** The dot on the bottom-right. It connects the bottom wire, the right vertical branch, and the output terminal.

### Step-by-Step Solution

#### Step 1: Analyze the paths from Node L to Node T
There are two separate paths operating in parallel between the Left Node and the Top Node.

1.  **Outer Top-Left Branch:** The current goes up through one vertical resistor, turns the corner, and goes right through one horizontal resistor.
    * These 2 resistors are in series.
    * $R_{branch1} = 5 + 5 = 10\ \Omega$

2.  **Inner "L" Branch:** The current goes right through one horizontal resistor, turns the corner, and goes up through **two** distinct vertical resistors.
    * These 3 resistors are in series.
    * $R_{branch2} = 5 + 5 + 5 = 15\ \Omega$

Now, we calculate the equivalent resistance of these two parallel branches ($R_{LT}$):

$$
R_{LT} = \frac{R_{branch1} \cdot R_{branch2}}{R_{branch1} + R_{branch2}}
$$

$$
R_{LT} = \frac{10 \cdot 15}{10 + 15} = \frac{150}{25} = 6\ \Omega
$$

#### Step 2: Analyze the path from Node T to Node R
From the Top Node, the current travels to the Right Node through the far-right vertical branch.
* This branch contains **two** vertical resistors in series.
* $R_{TR} = 5 + 5 = 10\ \Omega$

#### Step 3: Calculate the total upper network resistance
The entire upper section of the circuit forces current to flow from Node L, through Node T, to Node R. Therefore, the equivalent resistance $R_{LT}$ is in series with $R_{TR}$:

$$
R_{upper} = R_{LT} + R_{TR} = 6 + 10 = 16\ \Omega
$$

#### Step 4: Calculate the final Equivalent Resistance ($R_{eq}$)
Finally, the entire upper network ($16\ \Omega$) is in parallel with the very bottom wire that directly connects Node L to Node R.
* The bottom wire contains **one** horizontal resistor: $R_{bottom} = 5\ \Omega$

We combine $R_{upper}$ and $R_{bottom}$ in parallel to find the total equivalent resistance of the circuit:

$$
R_{eq} = \frac{R_{upper} \cdot R_{bottom}}{R_{upper} + R_{bottom}}
$$

$$
R_{eq} = \frac{16 \cdot 5}{16 + 5}
$$

$$
R_{eq} = \frac{80}{21}\ \Omega \approx
