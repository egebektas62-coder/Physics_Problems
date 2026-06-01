## 3. Propagation of Error III

### Necessary Definitions and Formulas

#### 1. Ohm's Law (Resistance)
Resistance ($R$) is calculated by dividing Voltage ($V$) by Current ($I$):

$$
R = \frac{V}{I}
$$

#### 2. Propagation of Uncertainty (Division)
When one measured quantity is divided by another, the maximum bound of uncertainty is found by adding their relative (fractional) uncertainties together. 

$$
\frac{\Delta R}{R} = \frac{\Delta V}{V} + \frac{\Delta I}{I}
$$

By rearranging this to solve for the absolute uncertainty ($\Delta R$), we get:

$$
\Delta R = R \cdot \left( \frac{\Delta V}{V} + \frac{\Delta I}{I} \right)
$$

(Note: If your lab uses the "Quadrature" / "Root-Sum-Square" method for independent random errors, the formula is:

$$
\Delta R = R \cdot \sqrt{\left(\frac{\Delta V}{V}\right)^2 + \left(\frac{\Delta I}{I}\right)^2}
$$

We will stick to the standard maximum error bound method here, keeping consistent with the previous solutions).

---

### Step-by-Step Solution

Let's identify the given parameters from the problem:
* Voltage ($V$): $10.0\text{ V}$
* Uncertainty in Voltage ($\Delta V$): $0.2\text{ V}$
* Current ($I$): $2.00\text{ A}$
* Uncertainty in Current ($\Delta I$): $0.05\text{ A}$

#### Step 1: Calculate the Best Estimate for Resistance ($R$)
Substitute the measured voltage and current into Ohm's Law:

$$
R = \frac{10.0}{2.00}
$$

$$
R = 5.00\ \Omega
$$

#### Step 2: Calculate the Absolute Uncertainty ($\Delta R$)
Using the maximum error bound formula, we plug in our fractional values:

$$
\Delta R = 5.00 \cdot \left( \frac{0.2}{10.0} + \frac{0.05}{2.00} \right)
$$

$$
\Delta R = 5.00 \cdot \left( 0.02 + 0.025 \right)
$$

$$
\Delta R = 5.00 \cdot (0.045)
$$

$$
\Delta R = 0.225\ \Omega
$$

#### Step 3: Significant Figures and Final Rounding
We follow standard academic rounding rules:
1. Round the uncertainty ($\Delta R$) to one significant figure: $0.225$ rounds to **$0.2\ \Omega$**.
2. Because our rounded uncertainty stops at the "tenths" decimal place, we must also round our calculated resistance ($5.00$) to the "tenths" place: $5.00$ rounds to **$5.0\ \Omega$**.

---

### Final Result

The calculated resistance and its associated uncertainty is:

$$
R = (5.0 \pm 0.2)\ \Omega
$$
