# Damped Harmonic Oscillator: Analytical and Numerical (RK4) Analysis

## Necessary Definitions and Formulas

### 1. The Differential Equation
A damped harmonic oscillator is subjected to a restoring force ($-kx$) and a damping force ($-bv$) proportional to its velocity. According to Newton's Second Law ($F_{net} = ma$), the equation of motion is:

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0
$$

Where:
* **$m$**: Mass of the oscillator (kg)
* **$b$**: Damping coefficient (N·s/m)
* **$k$**: Spring constant (N/m)

### 2. Standard Form and Parameters
To solve this easily, we divide by $m$ and define two new parameters:
* **Natural Frequency ($\omega_0$):** $\omega_0 = \sqrt{\frac{k}{m}}$
* **Damping Ratio Parameter ($\gamma$):** $\gamma = \frac{b}{2m}$

The differential equation can now be written as:

$$
\frac{d^2 x}{dt^2} + 2\gamma \frac{dx}{dt} + \omega_0^2 x = 0
$$



---

## 1. General Solution

To find the general solution, we assume a solution of the form $x(t) = e^{rt}$. Substituting this into the standard equation yields the **characteristic equation**:

$$
r^2 + 2\gamma r + \omega_0^2 = 0
$$

Using the quadratic formula, the roots are:

$$
r_{1,2} = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}
$$

The behavior of the solution depends entirely on the discriminant ($\Delta = \gamma^2 - \omega_0^2$).

---

## 2. Classification of Cases

Depending on the value of the damping coefficient $b$ relative to $2\sqrt{mk}$ (or $\gamma$ relative to $\omega_0$), the system exhibits three distinct behaviors:

### A) Underdamped Case ($b^2 < 4mk$ or $\gamma < \omega_0$)
The roots are complex conjugates. The system oscillates, but the amplitude decays exponentially over time.
**Solution:** $$
x(t) = A e^{-\gamma t} \cos(\omega_d t + \phi)
$$

*(Where $\omega_d = \sqrt{\omega_0^2 - \gamma^2}$ is the damped frequency).*

### B) Critically Damped Case ($b^2 = 4mk$ or $\gamma = \omega_0$)
The roots are real and repeated. The system returns to equilibrium as fast as possible without oscillating. This is the mathematical boundary.
**Solution:** $$
x(t) = (A + Bt) e^{-\gamma t}
$$

### C) Overdamped Case ($b^2 > 4mk$ or $\gamma > \omega_0$)
The roots are real and distinct. The damping is so strong that the system behaves sluggishly, taking a long time to return to equilibrium without oscillating.
**Solution:** $$
x(t) = A e^{r_1 t} + B e^{r_2 t}
$$

---

## 3. Numerical Solution (Runge-Kutta 4th Order - RK4)

To solve the 2nd-order ODE numerically in our simulation, we must reduce it to a system of two 1st-order ODEs. Let velocity $v = \frac{dx}{dt}$. The system becomes:

1.  $\frac{dx}{dt} = v$
2.  $\frac{dv}{dt} = -\frac{b}{m}v - \frac{k}{m}x$

The RK4 algorithm calculates four slopes ($k_1, k_2, k_3, k_4$) for both $x$ and $v$ at each time step ($dt$) and takes a weighted average to predict the next state. This method is highly stable for oscillatory physics compared to the basic Euler method.

---

## 4, 5 & 6: Interactive HTML Animation (Graphs and Phase Portrait)

Below is the complete, single-file HTML/JS engine that uses the RK4 method to instantly calculate and visualize the motion. 
* **$x(t)$ Graph:** Shows position vs. time.
* **Phase Portrait ($v$ vs $x$):** Shows velocity on the y-axis and position on the x-axis. (Spirals inward for underdamped, forms a direct path to origin for overdamped).

Save the code below as `damped-oscillator.html` and open it in any browser to interact with the $b$ parameter.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Damped Oscillator RK4 Engine</title>
    <script src="[https://cdn.tailwindcss.com](https://cdn.tailwindcss.com)"></script>
    <style>
        body { background-color: #0f172a; color: white; font-family: monospace; }
        canvas { background-color: #1e293b; border-radius: 8px; border: 1px solid #334155; }
    </style>
</head>
<body class="flex flex-col items-center py-8 px-4">

    <div class="max-w-5xl w-full">
        <div class="mb-6 flex justify-between items-end">
            <div>
                <h1 class="text-3xl font-bold text-blue-400">RK4 Damped Oscillator Engine</h1>
                <p class="text-slate-400">Interactive Time-Domain & Phase Space Analysis</p>
            </div>
            <div id="caseLabel" class="bg-blue-900 text-blue-200 px-3 py-1 rounded font-bold uppercase tracking-wider">
                Underdamped
            </div>
        </div>

        <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 mb-6">
            <div class="flex justify-between mb-2">
                <span class="text-slate-300 font-bold">Damping Coefficient (b): <span id="bValue" class="text-yellow-400">1.0</span></span>
                <span class="text-slate-400 text-xs">Mass (m) = 1.0 kg | Spring (k) = 10.0 N/m | b_critical ≈ 6.32</span>
            </div>
            <input type="range" id="bSlider" min="0" max="15" step="0.1" value="1" class="w-full h-2 bg-slate-600 rounded-lg appearance-none cursor-pointer">
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div>
                <h3 class="text-center text-sm text-slate-400 mb-2">Position vs. Time — x(t)</h3>
                <canvas id="xtCanvas" width="500" height="300" class="w-full"></canvas>
            </div>
            
            <div>
                <h3 class="text-center text-sm text-slate-400 mb-2">Phase Portrait — v(t) vs. x(t)</h3>
                <canvas id="phaseCanvas" width="500" height="300" class="w-full"></canvas>
            </div>
        </div>
    </div>

    <script>
        const xtCtx = document.getElementById('xtCanvas').getContext('2d');
        const phaseCtx = document.getElementById('phaseCanvas').getContext('2d');
        const bSlider = document.getElementById('bSlider');
        const bValueLabel = document.getElementById('bValue');
        const caseLabel = document.getElementById('caseLabel');

        // Physics Constants
        const m = 1.0;
        const k = 10.0;
        const x0 = 5.0; // Initial displacement
        const v0 = 0.0; // Initial velocity
        const dt = 0.02; // Time step
        const steps = 1000; // Simulation steps (~20 seconds)
        
        const b_crit = 2 * Math.sqrt(m * k); // ~6.324

        // Runge-Kutta 4th Order Integrator
        function calculateRK4(b) {
            let data = [];
            let x = x0;
            let v = v0;
            let t = 0;

            for (let i = 0; i < steps; i++) {
                data.push({ t, x, v });

                // ODEs: dx/dt = v, dv/dt = -(b/m)v - (k/m)x
                let k1x = v;
                let k1v = (-b * v - k * x) / m;

                let k2x = v + 0.5 * dt * k1v;
                let k2v = (-b * (v + 0.5 * dt * k1v) - k * (x + 0.5 * dt * k1x)) / m;

                let k3x = v + 0.5 * dt * k2v;
                let k3v = (-b * (v + 0.5 * dt * k2v) - k * (x + 0.5 * dt * k2x)) / m;

                let k4x = v + dt * k3v;
                let k4v = (-b * (v + dt * k3v) - k * (x + dt * k3x)) / m;

                x += (dt / 6) * (k1x + 2 * k2x + 2 * k3x + k4x);
                v += (dt / 6) * (k1v + 2 * k2v + 2 * k3v + k4v);
                t += dt;
            }
            return data;
        }

        function drawXTGraph(data) {
            xtCtx.clearRect(0, 0, 500, 300);
            
            // Draw Axis
            xtCtx.strokeStyle = '#475569';
            xtCtx.beginPath();
            xtCtx.moveTo(0, 150); xtCtx.lineTo(500, 150); // t-axis
            xtCtx.moveTo(20, 0); xtCtx.lineTo(20, 300); // x-axis
            xtCtx.stroke();

            // Draw Data
            xtCtx.strokeStyle = '#3b82f6';
            xtCtx.lineWidth = 2;
            xtCtx.beginPath();
            
            data.forEach((pt, i) => {
                let px = 20 + (pt.t / (steps*dt)) * 460;
                let py = 150 - (pt.x / 6) * 100; // Scale x
                if (i === 0) xtCtx.moveTo(px, py);
                else xtCtx.lineTo(px, py);
            });
            xtCtx.stroke();
        }

        function drawPhasePortrait(data) {
            phaseCtx.clearRect(0, 0, 500, 300);
            
            // Draw Axis
            phaseCtx.strokeStyle = '#475569';
            phaseCtx.beginPath();
            phaseCtx.moveTo(0, 150); phaseCtx.lineTo(500, 150); // x-axis
            phaseCtx.moveTo(250, 0); phaseCtx.lineTo(250, 300); // v-axis
            phaseCtx.stroke();
            phaseCtx.fillStyle = '#94a3b8';
            phaseCtx.fillText("+x", 480, 140);
            phaseCtx.fillText("+v", 260, 15);

            // Draw Data
            phaseCtx.strokeStyle = '#ec4899'; // Pink
            phaseCtx.lineWidth = 2;
            phaseCtx.beginPath();
            
            data.forEach((pt, i) => {
                let px = 250 + (pt.x / 6) * 150; // Scale x
                let py = 150 - (pt.v / 15) * 100; // Scale v
                if (i === 0) phaseCtx.moveTo(px, py);
                else phaseCtx.lineTo(px, py);
            });
            xtCtx.stroke();
            phaseCtx.stroke();
            
            // Draw Start Point
            let startPx = 250 + (data[0].x / 6) * 150;
            let startPy = 150 - (data[0].v / 15) * 100;
            phaseCtx.fillStyle = '#10b981';
            phaseCtx.beginPath(); phaseCtx.arc(startPx, startPy, 4, 0, Math.PI*2); phaseCtx.fill();
        }

        function updateSimulation() {
            let b = parseFloat(bSlider.value);
            bValueLabel.innerText = b.toFixed(1);
            
            // Update Classification Label
            if (Math.abs(b - b_crit) < 0.2) {
                caseLabel.innerText = "Critically Damped";
                caseLabel.className = "bg-emerald-900 text-emerald-200 px-3 py-1 rounded font-bold uppercase tracking-wider";
            } else if (b < b_crit) {
                caseLabel.innerText = "Underdamped";
                caseLabel.className = "bg-blue-900 text-blue-200 px-3 py-1 rounded font-bold uppercase tracking-wider";
            } else {
                caseLabel.innerText = "Overdamped";
                caseLabel.className = "bg-orange-900 text-orange-200 px-3 py-1 rounded font-bold uppercase tracking-wider";
            }

            let data = calculateRK4(b);
            drawXTGraph(data);
            drawPhasePortrait(data);
        }

        bSlider.addEventListener('input', updateSimulation);
        updateSimulation(); // Initial draw
    </script>
</body>
</html>
