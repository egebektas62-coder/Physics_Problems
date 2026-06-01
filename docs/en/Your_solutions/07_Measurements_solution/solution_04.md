## 4. Relative Uncertainty

### Necessary Definitions and Formulas

#### 1. Relative (Percentage) Uncertainty
Relative uncertainty expresses the error as a fraction or percentage of the measured value. The absolute uncertainty ($\Delta x$) can be extracted from a percentage uncertainty using the formula:

$$
\Delta x = x \cdot \left( \frac{\text{Percentage}}{100} \right)
$$

#### 2. Range of the Actual Value
Once the absolute uncertainty is known, the actual value is mathematically bounded by a minimum and maximum limit:

$$
\text{Range} = [x - \Delta x, x + \Delta x]
$$

---

### Step-by-Step Solution

Let's identify the given parameters from the problem:
* Measured Speed ($v$): 60 km/h
* Percentage Uncertainty: 5%

#### Step 1: Calculate the Absolute Uncertainty ($\Delta v$)
Substitute the measured speed and the percentage into the absolute uncertainty formula:

$$
\Delta v = 60 \cdot \left( \frac{5}{100} \right)
$$

$$
\Delta v = 60 \cdot 0.05
$$

$$
\Delta v = 3\text{ km/h}
$$

#### Step 2: Calculate the Range
Now apply the absolute uncertainty to the measured speed to find the lower and upper bounds of the actual speed:

* **Lower Bound:** $60 - 3 = 57\text{ km/h}$
* **Upper Bound:** $60 + 3 = 63\text{ km/h}$

#### Step 3: Significant Figures and Final Rounding
Our absolute uncertainty is $3\text{ km/h}$ (which is correctly at one significant figure). Because this uncertainty is in the "ones" place, our measured value must also be reported to the "ones" place, which perfectly matches our starting value of $60\text{ km/h}$. 

---

### Final Result

The absolute speed and its associated uncertainty is:

$$
v = (60 \pm 3)\text{ km/h}
$$

The range of the car's actual speed is **57 km/h to 63 km/h**.
