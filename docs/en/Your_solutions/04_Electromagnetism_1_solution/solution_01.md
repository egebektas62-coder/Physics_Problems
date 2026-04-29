# Coulomb's Law: Electric Force in a Symmetric Configuration

## Necessary Definitions and Formulas

### 1. Coulomb's Law
The magnitude of the electrostatic force of attraction or repulsion between two point charges is directly proportional to the product of the magnitudes of charges and inversely proportional to the square of the distance between them.

$$
F = k \frac{|q_1 q_2|}{r^2}
$$

Where:
* **$F$**: Magnitude of the electric force
* **$k$**: Coulomb's constant ($\approx 8.99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$)
* **$q_1, q_2$**: Magnitudes of the charges
* **$r$**: Distance between the charges

### 2. The Principle of Superposition
If more than two charges are present, the net force on any specific charge is the vector sum of the individual forces exerted on it by all other charges.

$$
\vec{F}_{net} = \vec{F}_1 + \vec{F}_2 + \dots + \vec{F}_n
$$

---

## Problem Statement

Four point charges of +1.0 C each are placed at the corners of a square with sides of 1.0 m. Calculate the magnitude and direction of the electric force on a charge of -2.0 C placed at the center of the square.

---

## Step-by-Step Solution

### Step 1: Analyze the Geometry
Let the square have a side length of $a = 1.0 \text{ m}$. The distance from any corner to the center of the square is half of the diagonal.

The diagonal $d$ of a square is:

$$
d = \sqrt{a^2 + a^2} = a\sqrt{2} = 1.0\sqrt{2} \text{ m}
$$

The distance $r$ from a corner to the center is:

$$
r = \frac{d}{2} = \frac{\sqrt{2}}{2} \text{ m} \approx 0.707 \text{ m}
$$

### Step 2: Calculate the Magnitude of Individual Forces
The center charge is $q_{center} = -2.0 \text{ C}$. Each corner charge is $q_{corner} = +1.0 \text{ C}$.
Because all four corner charges are identical in magnitude and are at the exact same distance $r$ from the center, the magnitude of the force exerted by *each* corner charge on the center charge will be identical.

$$
F_{individual} = k \frac{|q_{corner} \cdot q_{center}|}{r^2}
$$

Substitute the values:

$$
F_{individual} = (8.99 \times 10^9) \frac{|1.0 \cdot (-2.0)|}{\left(\frac{\sqrt{2}}{2}\right)^2}
$$

Square the distance: $\left(\frac{\sqrt{2}}{2}\right)^2 = \frac{2}{4} = 0.5$

$$
F_{individual} = (8.99 \times 10^9) \frac{2}{0.5} = (8.99 \times 10^9) \cdot 4 = 35.96 \times 10^9 \text{ N}
$$

### Step 3: Vector Addition and Symmetry
The center charge is negative ($-2.0 \text{ C}$) and the corner charges are positive ($+1.0 \text{ C}$). Therefore, the center charge is *attracted* to each of the four corners.
    
* The force from the top-left corner pulls the center charge to the top-left.
* The force from the bottom-right corner pulls the center charge to the bottom-right.
    
Since these two forces act along the exact same diagonal line, are in strictly opposite directions, and have the exact same magnitude, they perfectly cancel each other out.
    
Similarly, the force from the top-right corner perfectly cancels the force from the bottom-left corner.

### Step 4: The Net Force
Summing up all the vector components:

$$
\vec{F}_{net} = \vec{F}_{top\_left} + \vec{F}_{bottom\_right} + \vec{F}_{top\_right} + \vec{F}_{bottom\_left} = 0 \text{ N}
$$

*Explanation:* Due to the perfect geometric symmetry of the charge distribution, the massive electrostatic forces pulling the center charge in all four directions perfectly balance each other out, resulting in a state of static equilibrium.

---

## Final Results Summary

* **Magnitude of the electric force ($F_{net}$):** $0 \text{ N}$
* **Direction:** Undefined (or none, as the net force is perfectly balanced to zero)

---

**Hocaya Karşı Şov Notu (Siber Güvenlikçi Yaklaşımı):**

Eğer hoca *"Ege, bu kadar devasa yükler (1 Coulomb fizikte devasa bir yüktür) ortada nasıl 0 N kuvvet yaratıyor?"* diye sorarsa, vereceğin "Mühendis" cevabı şudur:

*"Hocam bu durum, bilgisayar ağlarındaki 'Denial of Service' (DDoS) saldırılarına karşı uygulanan 'Null Routing' (Kara Delik) yönlendirmesi veya simetrik yük dağıtımı (Load Balancing) gibidir. Sistemin merkezine dört bir yandan devasa büyüklükte bir trafik (kuvvet) geliyor. Ancak vektörel topoloji o kadar kusursuz bir simetriye sahip ki, her bir kuvvet vektörü kendi anti-vektörünü sıfırlıyor. Sistemin üzerindeki 'stres' (Tension) milyarlarca Newton olmasına rağmen, sistemin net ivmelenmesi (Net Payload) tam olarak sıfırdır."*
