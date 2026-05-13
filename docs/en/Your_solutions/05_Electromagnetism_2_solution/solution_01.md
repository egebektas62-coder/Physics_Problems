# Gauss's Law: Electric Flux Through a Closed Surface

## Necessary Definitions and Formulas

### 1. Gauss's Law
Gauss's Law states that the total electric flux ($\Phi_E$) outward through any closed surface is equal to the net electric charge enclosed within that surface ($q_{enc}$) divided by the vacuum permittivity ($\varepsilon_0$).

$$
\Phi_E = \oint \vec{E} \cdot d\vec{A} = \frac{q_{enc}}{\varepsilon_0}
$$

### 2. The Irrelevance of Radius
A critical conceptual point of Gauss's Law is that the total flux through a closed surface depends **only** on the enclosed charge. The size (radius) or shape of the enclosing surface does not change the total number of electric field lines passing through it. 

* **Vacuum permittivity ($\varepsilon_0$):** $\approx 8.854 \times 10^{-12} \text{ C}^2/(\text{N}\cdot\text{m}^2)$

---

## Problem Statement

A point charge of $+2 \text{ C}$ is located at the origin. Calculate the electric flux through a spherical surface of radius $1 \text{ m}$ centered at the origin.

---

## Step-by-Step Solution

### Step 1: Identify the Known Variables
* **Enclosed Charge ($q_{enc}$):** $+2 \text{ C}$
* **Radius of the sphere ($r$):** $1 \text{ m}$ *(This is a distractor! We don't need it to find the total flux).*
* **Permittivity of free space ($\varepsilon_0$):** $8.854 \times 10^{-12} \text{ C}^2/(\text{N}\cdot\text{m}^2)$

### Step 2: Apply Gauss's Law
Since we need the total electric flux through the entire spherical surface, we can completely bypass the complex surface integral ($\oint \vec{E} \cdot d\vec{A}$) and directly use the enclosed charge:

$$
\Phi_E = \frac{q_{enc}}{\varepsilon_0}
$$

### Step 3: Calculate the Flux
Substitute the known values into the equation:

$$
\Phi_E = \frac{2}{8.854 \times 10^{-12}}
$$

$$
\Phi_E \approx 2.259 \times 10^{11} \text{ N}\cdot\text{m}^2/\text{C}
$$

*Explanation:* An enormous amount of electric flux is radiating outward through the sphere. Notice that if the radius of the sphere were 10 meters, or 100 meters, the total flux would remain exactly exactly the same. The field gets weaker as it spreads out, but the total surface area increases by the exact same proportion, perfectly canceling out the difference.

---

## Final Results Summary

* **Total Electric Flux ($\Phi_E$):** $\approx 2.259 \times 10^{11} \text{ N}\cdot\text{m}^2/\text{C}$

---
