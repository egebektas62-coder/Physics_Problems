# Parallel-Plate Capacitor Calculations

## Known Variables
* **Area ($S$):** $0.02 \text{ m}^2$
* **Distance ($d$):** $5 \text{ mm} = 5 \times 10^{-3} \text{ m}$
* **Voltage ($U$):** $500 \text{ V}$
* **Vacuum Permittivity ($\varepsilon_0$):** $\approx 8.854 \times 10^{-12} \text{ F/m}$

---

### 1. Capacitance ($C$)
The capacitance of a parallel-plate capacitor is determined by its geometry and the permittivity of the dielectric (vacuum/air in this case):

$$
C = \frac{\varepsilon_0 \cdot S}{d}
$$

$$
C = \frac{(8.854 \times 10^{-12}) \cdot 0.02}{5 \times 10^{-3}}
$$

$$
C = 35.416 \times 10^{-12} \text{ F} \quad (\text{or } 35.42 \text{ pF})
$$

---

### 2. Energy Stored ($W$ or $E_{stored}$)
*(Note: Using $W$ for energy to avoid confusion with the voltage $U$)*
The energy stored in the electric field of the capacitor is:

$$
W = \frac{1}{2} C U^2
$$

$$
W = \frac{1}{2} \cdot (35.416 \times 10^{-12}) \cdot (500)^2
$$

$$
W = 0.5 \cdot (35.416 \times 10^{-12}) \cdot 250,000
$$

$$
W = 4.427 \times 10^{-6} \text{ J} \quad (\text{or } 4.43 \mu\text{J})
$$

---

### 3. Electric Field Intensity ($E$)
The uniform electric field between the two parallel plates is the voltage divided by the distance:

$$
E = \frac{U}{d}
$$

$$
E = \frac{500}{5 \times 10^{-3}}
$$

$$
E = 100,000 \text{ V/m} \quad (\text{or } 1 \times 10^5 \text{ V/m})
$$

---

### 4. Force of Attraction ($F$)
The plates of the capacitor carry opposite charges and attract each other. The electrostatic force is given by:

$$
F = \frac{1}{2} \varepsilon_0 E^2 S
$$

Alternatively, using the stored energy, $F = \frac{W}{d}$:

$$
F = \frac{4.427 \times 10^{-6}}{5 \times 10^{-3}}
$$

$$
F = 8.854 \times 10^{-4} \text{ N}
$$

---

## Final Results Summary
1. **Capacitance ($C$):** $\approx 35.42 \text{ pF}$
2. **Energy Stored ($W$):** $\approx 4.43 \mu\text{J}$
3. **Electric Field Intensity ($E$):** $100,000 \text{ V/m}$
4. **Force of Attraction ($F$):** $\approx 8.85 \times 10^{-4} \text{ N}$
