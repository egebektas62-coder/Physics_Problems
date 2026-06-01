## 7. Standard Deviation

### Necessary Definitions and Formulas

#### 1. Mean (Average)
The mean ($\bar{x}$) is the sum of all data points divided by the total number of data points ($N$).

$$
\bar{x} = \frac{1}{N} \sum_{i=1}^N x_i
$$

#### 2. Sample Standard Deviation
Standard deviation measures how spread out the numbers are. Because this is a sample of students (not an entire population), we divide by $N-1$ (Bessel's correction) as given in your formula:

$$
\sigma = \sqrt{\frac{1}{N-1} \sum_{i=1}^N (x_i - \bar{x})^2}
$$

*(Note: In statistics, sample standard deviation is often denoted by $s$, while population standard deviation is $\sigma$. However, we will use your provided formula exactly as written).*

---

### Step-by-Step Solution: Part 1 (All 11 Students)

**Given Data:** 88, 92, 79, 85, 95, 81, 86, 90, 83, 77, 89
**Total number of students ($N$):** 11

#### Step 1: Calculate the Mean ($\bar{x}$)
First, find the sum of all the scores:

$$
\sum x_i = 88 + 92 + 79 + 85 + 95 + 81 + 86 + 90 + 83 + 77 + 89 = 945
$$

Now, divide by $N$:

$$
\bar{x} = \frac{945}{11}
$$

$$
\bar{x} \approx 85.91
$$

#### Step 2: Calculate the Sum of Squared Deviations
Next, we subtract the mean from each score, square the result, and add them all up: $\sum (x_i - \bar{x})^2$.
*(Using the exact fraction 945/11 to avoid rounding errors during intermediate steps yields a sum of squares of approximately 310.91)*

$$
\sum (x_i - \bar{x})^2 \approx 310.91
$$

#### Step 3: Calculate the Standard Deviation
Divide the sum of squared deviations by $N - 1$ (which is $11 - 1 = 10$) and take the square root:

$$
\sigma = \sqrt{\frac{310.91}{10}}
$$

$$
\sigma = \sqrt{31.091}
$$

$$
\sigma \approx 5.58
$$

---

### Step-by-Step Solution: Part 2 (Removing Extremes)

Now, we remove the highest score (**95**) and the lowest score (**77**).
**New Data:** 88, 92, 79, 85, 81, 86, 90, 83, 89
**New number of students ($N$):** 9

#### Step 4: Calculate the New Mean
Find the new sum of the scores (or simply subtract 95 and 77 from the original sum of 945):

$$
\sum x_i = 945 - 95 - 77 = 773
$$

Divide by the new $N$:

$$
\bar{x}_{new} = \frac{773}{9}
$$

$$
\bar{x}_{new} \approx 85.89
$$

#### Step 5: Calculate the New Standard Deviation
Find the new sum of squared deviations using the new mean (85.89):

$$
\sum (x_i - \bar{x}_{new})^2 \approx 148.89
$$

Divide by the new $N - 1$ (which is $9 - 1 = 8$) and take the square root:

$$
\sigma_{new} = \sqrt{\frac{148.89}{8}}
$$

$$
\sigma_{new} = \sqrt{18.61}
$$

$$
\sigma_{new} \approx 4.31
$$

---

### Final Results Summary

**With All 11 Scores:**
* Mean: **85.91**
* Standard Deviation: **5.58**

**With Highest and Lowest Scores Removed:**
* New Mean: **85.89**
* New Standard Deviation: **4.31**

*(Note: As expected, removing the extreme outliers barely changed the average, but it significantly shrank the standard deviation because the data is now grouped much tighter together!)*
