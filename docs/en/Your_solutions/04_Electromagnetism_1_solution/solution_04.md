# Force Comparison: Electric vs. Gravitational Force

## Necessary Definitions and Constants

To compare the two fundamental forces acting between an electron and a proton, we use Coulomb's Law for the electric force and Newton's Law of Universal Gravitation for the gravitational force.

### 1. Coulomb's Law (Electric Force)
The electric force between two point charges is:

$$
F_e = k \frac{|q_1 q_2|}{r^2}
$$

### 2. Newton's Law of Universal Gravitation (Gravitational Force)
The gravitational force between two masses is:

$$
F_g = G \frac{m_1 m_2}{r^2}
$$

### 3. Fundamental Constants
* **Coulomb's constant ($k$):** $\approx 8.99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$
* **Gravitational constant ($G$):** $\approx 6.674 \times 10^{-11} \text{ N}\cdot\text{m}^2/\text{kg}^2$
* **Elementary charge ($e$):** $\approx 1.602 \times 10^{-19} \text{ C}$
* **Mass of proton ($m_p$):** $\approx 1.672 \times 10^{-27} \text{ kg}$
* **Mass of electron ($m_e$):** $\approx 9.109 \times 10^{-31} \text{ kg}$
* **Distance ($r$):** $5.3 \times 10^{-11} \text{ m}$

---

## Problem Statement

Calculate the magnitude of the electric force and the gravitational force between an electron and a proton in a hydrogen atom (average distance $r \approx 5.3 \times 10^{-11} \text{ m}$). What is the ratio $F_e/F_g$?

---

## Step-by-Step Solution

### Step 1: Calculate the Electric Force ($F_e$)
The proton has a charge of $+e$ and the electron has a charge of $-e$. 

$$
F_e = (8.99 \times 10^9) \frac{(1.602 \times 10^{-19})^2}{(5.3 \times 10^{-11})^2}
$$

Square the charge and distance:

$$
F_e = (8.99 \times 10^9) \frac{2.566 \times 10^{-38}}{2.809 \times 10^{-21}}
$$

Calculate the final value:

$$
F_e \approx 8.22 \times 10^{-8} \text{ N}
$$

### Step 2: Calculate the Gravitational Force ($F_g$)
Now we use the masses of the proton and electron.

$$
F_g = (6.674 \times 10^{-11}) \frac{(1.672 \times 10^{-27}) \cdot (9.109 \times 10^{-31})}{(5.3 \times 10^{-11})^2}
$$

Multiply the masses and square the distance:

$$
F_g = (6.674 \times 10^{-11}) \frac{15.23 \times 10^{-58}}{2.809 \times 10^{-21}}
$$

Calculate the final value:

$$
F_g \approx 3.62 \times 10^{-47} \text{ N}
$$

### Step 3: Calculate the Ratio ($F_e / F_g$)
To find out how many times stronger the electric force is compared to gravity at this scale, we divide $F_e$ by $F_g$.

$$
\text{Ratio} = \frac{8.22 \times 10^{-8}}{3.62 \times 10^{-47}}
$$

$$
\text{Ratio} \approx 2.27 \times 10^{39}
$$

*Explanation:* The electric force is approximately $2 \times 10^{39}$ times stronger than the gravitational force. This number is staggeringly huge (2 followed by 39 zeros), which is why gravity is completely ignored when calculating subatomic and chemical interactions.

---

## Final Results Summary

* **Electric Force ($F_e$):** $\approx 8.22 \times 10^{-8} \text{ N}$
* **Gravitational Force ($F_g$):** $\approx 3.62 \times 10^{-47} \text{ N}$
* **Ratio ($F_e / F_g$):** $\approx 2.27 \times 10^{39}$

---

**Hocaya Karşı Şov Notu (Siber Güvenlikçi Yaklaşımı):**

Eğer hoca *"Ege, madem kütleçekimi bu kadar zayıf, neden formüllerde yerçekimini tamamen silip atmıyoruz da hesaplıyoruz?"* diye sorarsa, yapıştıracağın sistem mühendisi cevabı şudur:

*"Hocam, sinyal işlemede (Signal Processing) ve donanım mimarisinde biz buna 'Noise Floor' (Gürültü Tabanı) deriz. Mikroişlemcilerde veri aktarırken çevresel termal gürültü her zaman vardır, ancak asıl veri sinyalimiz (Signal) gürültüden (Noise) 10^39 kat daha güçlü olduğu için SNR (Signal-to-Noise Ratio) pratikte sonsuz kabul edilir. Atom altı dünyada Elektromanyetizma ana iletişim protokolüyken (TCP/IP), Kütleçekimi sadece arka planda kalan, hesaplamaya katmanın işlemci gücünü (CPU cycle) boşa harcamaktan başka işe yaramayacağı bir parazittir."*
