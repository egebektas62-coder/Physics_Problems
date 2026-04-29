# Vector Lorentz Force: 3D Cross Product Application

## Necessary Definitions and Formulas

### 1. The Vector Lorentz Force Equation
When a charge $q$ moves with a velocity vector $\vec{v}$ through a magnetic field vector $\vec{B}$, the resulting magnetic force vector $\vec{F}_B$ is found using the cross product:

$$
\vec{F}_B = q(\vec{v} \times \vec{B})
$$

### 2. The Cross Product (Determinant Method)
The cross product of two 3D vectors $\vec{v} = \langle v_x, v_y, v_z \rangle$ and $\vec{B} = \langle B_x, B_y, B_z \rangle$ results in a new vector that is entirely perpendicular to both original vectors. It is calculated using a matrix determinant:

$$
\vec{v} \times \vec{B} = \begin{vmatrix} 
\hat{i} & \hat{j} & \hat{k} \\ 
v_x & v_y & v_z \\ 
B_x & B_y & B_z 
\end{vmatrix}
$$

### 3. Magnitude of a 3D Vector
Once the force vector components are found ($\vec{F} = F_x\hat{i} + F_y\hat{j} + F_z\hat{k}$), its magnitude is calculated using the 3D Pythagorean theorem:

$$
|\vec{F}| = \sqrt{F_x^2 + F_y^2 + F_z^2}
$$

---

## Problem Statement

A proton moves with a velocity $\vec{v} = (2\hat{i} - 4\hat{j} + \hat{k}) \text{ m/s}$ in a region where the magnetic field is $\vec{B} = (\hat{i} + 2\hat{j} - \hat{k}) \text{ T}$. What is the magnitude of the magnetic force this charge experiences?

---

## Step-by-Step Solution

### Step 1: Identify the Knowns
* **Charge of a proton ($q$):** $1.6 \times 10^{-19} \text{ C}$
* **Velocity ($\vec{v}$):** $\langle 2, -4, 1 \rangle \text{ m/s}$
* **Magnetic Field ($\vec{B}$):** $\langle 1, 2, -1 \rangle \text{ T}$

### Step 2: Calculate the Cross Product ($\vec{v} \times \vec{B}$)
Set up the determinant matrix:

$$
\vec{v} \times \vec{B} = \begin{vmatrix} 
\hat{i} & \hat{j} & \hat{k} \\ 
2 & -4 & 1 \\ 
1 & 2 & -1 
\end{vmatrix}
$$

Expand the determinant along the top row ($\hat{i}, \hat{j}, \hat{k}$):

* **For $\hat{i}$:** $((-4)(-1) - (1)(2)) = (4 - 2) = 2$
* **For $\hat{j}$:** $-((2)(-1) - (1)(1)) = -(-2 - 1) = 3$
* **For $\hat{k}$:** $((-2)(2) - (-4)(1)) \dots \text{ Wait, correction: } ((2)(2) - (-4)(1)) = (4 - (-4)) = 8$

Combine the components:

$$
\vec{v} \times \vec{B} = 2\hat{i} + 3\hat{j} + 8\hat{k}
$$

### Step 3: Calculate the Magnitude of the Cross Product
Find the magnitude of the resulting vector $\langle 2, 3, 8 \rangle$:

$$
|\vec{v} \times \vec{B}| = \sqrt{2^2 + 3^2 + 8^2}
$$

$$
|\vec{v} \times \vec{B}| = \sqrt{4 + 9 + 64} = \sqrt{77}
$$

$$
|\vec{v} \times \vec{B}| \approx 8.775
$$

### Step 4: Calculate the Magnitude of the Magnetic Force
Multiply the magnitude of the cross product by the charge of the proton ($q$).

$$
|\vec{F}_B| = q |\vec{v} \times \vec{B}|
$$

$$
|\vec{F}_B| = (1.6 \times 10^{-19}) \times \sqrt{77}
$$

$$
|\vec{F}_B| \approx 1.404 \times 10^{-18} \text{ N}
$$

---

## Final Results Summary

* **Cross Product Vector ($\vec{v} \times \vec{B}$):** $2\hat{i} + 3\hat{j} + 8\hat{k}$
* **Magnitude of Magnetic Force ($|\vec{F}_B|$):** $\approx 1.404 \times 10^{-18} \text{ N}$
