# Electrostatic Equilibrium: Finding the Balance Point

## Necessary Definitions and Formulas

### 1. Electrostatic Equilibrium
A point charge is in electrostatic equilibrium when the net electric force acting on it is exactly zero. This means the vector sum of all individual Coulomb forces pulling or pushing the charge completely cancels out.

$$
\vec{F}_{net} = 0 \implies |\vec{F}_{left}| = |\vec{F}_{right}|
$$

### 2. Coulomb's Law
The force between two point charges is calculated as:

$$
F = k \frac{|q_1 q_2|}{r^2}
$$

Where:
* **$F$**: Magnitude of the electric force
* **$k$**: Coulomb's constant
* **$q_1, q_2$**: Magnitudes of the interacting charges
* **$r$**: Distance between the two charges

---

## Problem Statement

Find the equilibrium position for a charge $q_3 = +1\text{C}$ placed on the line between a charge $q_1 = +4\text{C}$ and a charge $q_2 = +9\text{C}$, which are separated by a distance of 2 m.

---

## Step-by-Step Solution

### Step 1: Set Up the Coordinate System
Let's place the first charge, $q_1 = +4\text{C}$, at the origin ($x = 0$). 
The second charge, $q_2 = +9\text{C}$, is placed at distance $d = 2 \text{ m}$ ($x = 2$).
Let the third charge, $q_3 = +1\text{C}$, be placed at an unknown distance $x$ from $q_1$. 
Consequently, the distance from $q_3$ to $q_2$ will be $(2 - x)$.

### Step 2: Apply the Equilibrium Condition
Since $q_1$, $q_2$, and $q_3$ are all positive charges, $q_1$ pushes $q_3$ to the right (Force $F_{13}$), and $q_2$ pushes $q_3$ to the left (Force $F_{23}$). For $q_3$ to be in equilibrium, these two repulsive forces must be equal in magnitude.

$$
F_{13} = F_{23}
$$

Substitute Coulomb's Law for both sides:

$$
k \frac{q_1 q_3}{x^2} = k \frac{q_2 q_3}{(2 - x)^2}
$$

### Step 3: Simplify the Equation
Notice that Coulomb's constant ($k$) and the test charge ($q_3$) appear on both sides of the equation. They cancel each other out entirely. *(This proves that the equilibrium position is independent of the magnitude or sign of the third charge!)*

$$
\frac{q_1}{x^2} = \frac{q_2}{(2 - x)^2}
$$

Substitute the known values for $q_1$ and $q_2$:

$$
\frac{4}{x^2} = \frac{9}{(2 - x)^2}
$$

### Step 4: Solve for $x$
To solve this easily without using the quadratic formula, take the square root of both sides. (Since $q_3$ must be *between* the charges to balance the opposing forces, we only consider the positive roots representing physical distances).

$$
\sqrt{\frac{4}{x^2}} = \sqrt{\frac{9}{(2 - x)^2}}
$$

$$
\frac{2}{x} = \frac{3}{2 - x}
$$

Now, cross-multiply to solve for $x$:

$$
2(2 - x) = 3x
$$

$$
4 - 2x = 3x
$$

Add $2x$ to both sides:

$$
4 = 5x
$$

$$
x = \frac{4}{5} = 0.8 \text{ m}
$$

*Explanation:* The balance point is exactly 0.8 meters away from the +4C charge. It is closer to the smaller charge (+4C) because the larger charge (+9C) exerts a stronger force over distance. To perfectly balance them, the test charge must "hide" closer to the weaker source.

---

## Final Results Summary

* **Distance from $q_1$ (+4C):** $0.8 \text{ m}$
* **Distance from $q_2$ (+9C):** $1.2 \text{ m}$

---

**Hocaya Karşı Şov Notu (Siber Güvenlikçi Yaklaşımı):**

Eğer hoca *"Ege, formüldeki $q_3$ yükü (+1C) neden sadeleşti, oraya +1C yerine -100C koysaydık denge noktası (0.8 m) değişir miydi?"* diye sorarsa:

*"Hocam kesinlikle değişmezdi. Çünkü 'Elektrostatik Denge Noktası' (Lagrange Point gibi), test yükünün kendi büyüklüğüne veya işaretine değil, etraftaki 'Kaynak Yüklerin' (Source Nodes) yarattığı Elektrik Alan (Electric Field) topolojisine bağlıdır. Her iki taraftaki elektrik alanın ($E_1$ ve $E_2$) vektörel olarak birbirini sıfırladığı o kör nokta (Blind Spot / Null Zone), uzayın statik bir özelliğidir. Oraya artı yük de koysak, eksi yük de koysak kuvvetler dengelenir, sadece çekme/itme yönleri kendi içinde tersine döner."*
