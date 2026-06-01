## 1. Propagation of Error I

### Necessary Definitions and Formulas

#### 1. Volume of a Sphere
The volume ($V$) of a sphere is calculated using its radius ($r$):

$$
V = \frac{4}{3}\pi r^3
$$

#### 2. Propagation of Uncertainty (Power Rule)
When a measured quantity is raised to a power, its relative error is multiplied by that power. For the volume of a sphere (which uses $r^3$), the relative uncertainty formula is:

$$
\frac{\Delta V}{V} = 3 \cdot \frac{\Delta r}{r}
$$

Alternatively, using the exact calculus derivative method ($dV/dr$), the absolute uncertainty ($\Delta V$) is calculated as:

$$
\Delta V = \left( 4\pi r^2 \right) \cdot \Delta r
$$

*(Note: Both methods are mathematically identical and will give you the exact same result).*

---

### Step-by-Step Solution

Let's identify the given parameters from the problem:
* Radius ($r$): 6.20 cm
* Uncertainty in radius ($\Delta r$): 0.05 cm

#### Step 1: Calculate the Best Estimate for Volume ($V$)
Substitute the measured radius into the standard volume formula:

$$
V = \frac{4}{3}\pi \cdot (6.20)^3
$$

$$
V = \frac{4}{3}\pi \cdot 238.328
$$

$$
V \approx 998.31\ \text{cm}^3
$$

#### Step 2: Calculate the Absolute Uncertainty ($\Delta V$)
Let's use the calculus derivative formula to find the error in the volume:

$$
\Delta V = 4\pi \cdot (6.20)^2 \cdot 0.05
$$

$$
\Delta V = 4\pi \cdot 38.44 \cdot 0.05
$$

$$
\Delta V = 4\pi \cdot 1.922
$$

$$
\Delta V \approx 24.15\ \text{cm}^3
$$

#### Step 3: Significant Figures and Final Rounding
In error analysis, uncertainties are typically rounded to one or two significant figures. If we round the uncertainty to two significant figures, we get **$24\ \text{cm}^3$**.

The golden rule of error propagation is that your final calculated value must be rounded to match the least precise decimal place of your uncertainty. Since our uncertainty is $24$ (which stops at the "ones" place), we must round our volume ($998.31$) to the ones place as well, which gives us **$998$**.

---

### Final Result

The volume of the sphere and its associated uncertainty is:

$$
V = (998 \pm 24)\ \text{cm}^3
$$
