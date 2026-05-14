# Parallel-Plate Capacitor Analysis

## Necessary Definitions and Formulas

Before we begin the step-by-step solution, here are the core concepts and formulas related to a parallel-plate capacitor with a vacuum (or air) between its plates.

### 1. Capacitance ($C$)
Capacitance describes the ability of a system to store electric charge. For a parallel-plate capacitor, it depends entirely on the physical geometry (Area $S$ and distance $d$) and the permittivity of the material between the plates.

$$
C = \frac{\varepsilon_0 \cdot S}{d}
$$

Where:
* **$\varepsilon_0$**: Vacuum permittivity ($\approx 8.854 \times 10^{-12} \text{ F/m}$).
* **$S$**: Area of one of the plates.
* **$d$**: Separation distance between the plates.

### 2. Energy Stored in a Capacitor ($W$)
The work done to charge a capacitor is stored as potential energy in its electric field. *(Note: To avoid confusion, we will denote the given voltage as $U$ and the stored energy as $W$)*.

$$
W = \frac{1}{2} C U^2
$$

### 3. Electric Field Intensity ($E$)
For parallel plates, the electric field created between them is uniform (constant everywhere between the plates) and is simply the voltage divided by the distance.

$$
E = \frac{U}{d}
$$

### 4. Force of Attraction ($F$)
The two plates carry equal and opposite charges, meaning they attract each other. The electrostatic force between the plates is given by:

$$
F = \frac{1}{2} \varepsilon_0 E^2 S
$$

Alternatively, it can be derived from the stored energy:

$$
F = \frac{W}{d}
$$

---

## Step-by-Step Solution

Let's summarize the given parameters and convert them into standard SI units:
* **Area ($S$):** $0.02 \text{ m}^2$
* **Distance ($d$):** $5 \text{ mm} = 0.005 \text{ m}$
* **Voltage ($U$):** $500 \text{ V}$

### 1. Calculate the capacitance $C$ of the capacitor
Using the geometric formula for parallel-plate capacitance, we plug in the vacuum permittivity constant, the area, and the distance.

$$
C = \frac{8.854 \times 10^{-12} \cdot 0.02}{0.005}
$$

$$
C = 8.854 \times 10^{-12} \cdot 4
$$

**$C = 35.416 \times 10^{-12} \text{ F}$** (or $35.42 \text{ pF}$)

### 2. Calculate the energy stored in the capacitor
Using the capacitance we just found and the given voltage, we calculate the stored potential energy.

$$
W = \frac{1}{2} C U^2
$$

$$
W = \frac{1}{2} \cdot (35.416 \times 10^{-12}) \cdot (500)^2
$$

$$
W = 0.5 \cdot (35.416 \times 10^{-12}) \cdot 250,000
$$

**$W \approx 4.427 \times 10^{-6} \text{ J}$** (or $4.43 \mu\text{J}$)

### 3. Calculate the electric field intensity $E$ between the plates
The uniform electric field is the ratio of the potential difference to the separation distance.

$$
E = \frac{U}{d}
$$

$$
E = \frac{500}{0.005}
$$

**$E = 100,000 \text{ V/m}$** (or $10^5 \text{ V/m}$)

### 4. Calculate the force of attraction $F$ between the plates
We can use the energy-distance relationship ($F = W / d$) for a quick calculation, which is derived directly from the primary force equation.

$$
F = \frac{W}{d}
$$

$$
F = \frac{4.427 \times 10^{-6}}{0.005}
$$

**$F = 8.854 \times 10^{-4} \text{ N}$**

> **Self-check using the primary force formula:**
> $$F = \frac{1}{2} \varepsilon_0 E^2 S$$
> $$F = 0.5 \cdot (8.854 \times 10^{-12}) \cdot (10^5)^2 \cdot 0.02$$
> $$F = 8.854 \times 10^{-4} \text{ N}$$
> 
> *The results match perfectly.*
