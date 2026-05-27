# Equivalent Resistance of a Resistor Cube

## Necessary Definitions and Concepts

### Symmetry and Equipotential Nodes
In a highly symmetrical circuit like a cube with identical resistors on each edge, nodes that are structurally equivalent relative to the input and output terminals will be at the exact same electrical potential. Instead of complex Kirchhoff equations, we can solve this by tracking how the total current splits at each junction based on pure symmetry.

### Ohm's Law
The total equivalent resistance ($R_{eq}$) is the ratio of the total voltage drop ($V_{total}$) across the entire cube to the total current ($I$) entering it:

$$
V_{total} = I \cdot R_{eq}
$$

---

## Step-by-Step Solution

Let's inject a total theoretical current $I$ into one corner of the cube (let's call it the Input Node) and extract it from the diagonally opposite corner (the Output Node). All 12 edges have a resistance of $R$. We will trace a single continuous path from the input to the output.

### Step 1: The First Split (Leaving the Input Node)
When the total current $I$ enters the Input Node, it faces three identical edges connecting to three adjacent corners. Because the resistors are identical and the geometry to the output is perfectly symmetrical, the current splits equally three ways.
* **Current in each of the first 3 edges:** $\frac{I}{3}$
* **Voltage drop across this first segment:** $V_1 = \left(\frac{I}{3}\right) \cdot R$

### Step 2: The Second Split (The Middle Edges)
Each of those three $\frac{I}{3}$ currents arrives at a new node. From each of these intermediate nodes, there are two geometrically identical paths leading forward toward the exit. The current splits equally in half again. 
* **Current in each of these 6 middle edges:** $\frac{1}{2} \cdot \left(\frac{I}{3}\right) = \frac{I}{6}$
* **Voltage drop across this middle segment:** $V_2 = \left(\frac{I}{6}\right) \cdot R$

### Step 3: The Recombination (Approaching the Output Node)
These six middle paths now converge into the three nodes adjacent to the Output Node. At each of these three nodes, two $\frac{I}{6}$ currents combine to form a $\frac{I}{3}$ current, which then travels along the final edge to exit the cube.
* **Current in each of the final 3 edges:** $\frac{I}{6} + \frac{I}{6} = \frac{I}{3}$
* **Voltage drop across this final segment:** $V_3 = \left(\frac{I}{3}\right) \cdot R$

### Step 4: Calculate Total Voltage and Equivalent Resistance
The total voltage drop ($V_{total}$) from the Input Node to the Output Node along *any* chosen path is the sum of the voltage drops across the three segments we just traced:

$$
V_{total} = V_1 + V_2 + V_3
$$

$$
V_{total} = \left(\frac{I}{3}\right)R + \left(\frac{I}{6}\right)R + \left(\frac{I}{3}\right)R
$$

Find a common denominator (6) to add the fractions:

$$
V_{total} = \left(\frac{2I}{6}\right)R + \left(\frac{1I}{6}\right)R + \left(\frac{2I}{6}\right)R
$$

$$
V_{total} = \frac{5}{6} I \cdot R
$$

Finally, isolate $R_{eq}$ using Ohm's Law ($R_{eq} = \frac{V_{total}}{I}$):

$$
R_{eq} = \frac{\frac{5}{6} I \cdot R}{I}
$$

---

## Final Result

The equivalent resistance between two diagonally opposite corners of the cube is:
**$$R_{eq} = \frac{5}{6} R$$**
