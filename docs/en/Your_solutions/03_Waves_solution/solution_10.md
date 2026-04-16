# Animation: Wave Sources and Superposition

## Necessary Definitions and Formulas

### 1. 2D Wave Equation from a Point Source
A wave originating from a specific point $\vec{r_0}$ spreads outwards in concentric circles. The wave's displacement $u(\vec{r},t)$ at any point $\vec{r}$ in space and time $t$ depends on the magnitude of the distance from the source:

$$
d = |\vec{r} - \vec{r_0}| = \sqrt{(x - x_0)^2 + (y - y_0)^2}
$$

### 2. Attenuation (Damping Coefficient, $\alpha$)
Real-world waves lose energy as they spread, causing their amplitude to decrease (attenuate). The problem provides a specific equation for this:

$$
u(\vec{r},t) = \frac{A}{|\vec{r}-\vec{r_0}|^\alpha} \sin(k |\vec{r} - \vec{r_0}| - \omega t)
$$

* **$\alpha = 0$**: No attenuation. The wave has constant amplitude forever.
* **$\alpha = 0.5$**: Attenuation typical of surface ripples on water.
* **$\alpha = 1.0$**: Attenuation typical of sound waves spreading spherically in 3D air.

### 3. The Principle of Superposition
When multiple waves exist in the same space, the resultant total displacement $U_{total}$ is the algebraic sum of the individual displacements from each wave source:

$$
U_{total}(\vec{r}, t) = \sum_{i=1}^{N} u_i(\vec{r}, t)
$$

---

## Problem Statement

Write an HTML animation in which it is possible to place dots that will serve as sources of waves described by the equation:

$$
u(\vec{r},t) = \frac{A}{|\vec{r}-\vec{r_0}|^\alpha} \sin(k |\vec{r} - \vec{r_0}| - \omega t)
$$

where $\vec{r_0}$ is the position of the dot, and $\alpha$ is a parameter that can be set within the range $[0, 2]$. The animation should show the superposition of waves from all dots.

---

## Step-by-Step Solution

To achieve a high-quality, pixel-perfect animation of wave superposition, we must use the HTML5 Canvas API and perform raw pixel manipulation on every frame.

### Step 1: Initialize the Canvas and Parameters
Define the canvas resolution, simulation clock (`t`), base amplitude (`A`), wave number (`k`), and angular frequency (`omega`). We'll create an array (`sources[]`) to store the $(x, y)$ coordinates of each placed dot.

### Step 2: Implement User Interaction
Add a mouse event listener to the canvas. When the user clicks, calculate the $(x, y)$ coordinate relative to the canvas and push this new source into the `sources[]` array.

### Step 3: Implement the Numerical Integration (Superposition Loop)
On every animation frame:
1. Access the raw RGBA pixel array.
2. Run nested `for` loops through every pixel $(x, y)$ on the canvas.
3. For *each* pixel, iterate through all active `sources[]` to calculate the individual wave displacement $u_i$ using the given attenuation formula.
4. Sum all $u_i$ values to find the $U_{total}$ for that pixel.



### Step 4: Map Displacement to Colors (The Shader)
Convert $U_{total}$ into visual colors:
* Positive displacement maps to Cyan/Blue (constructive interference).
* Negative displacement maps to Dark Purple/Black (destructive interference).

---

## Interactive HTML Engine

Save the code below as an `index.html` file and open it in any browser to interact with the system. Click on the canvas to add wave sources and use the slider to adjust the attenuation parameter.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wave Superposition Engine</title>
    <style>
        body { background-color: #0f172a; color: white; font-family: monospace; display: flex; flex-direction: column; align-items: center; padding: 20px; }
        canvas { background-color: #000; border-radius: 8px; border: 1px solid #334155; width: 100%; max-width: 500px; image-rendering: pixelated; cursor: crosshair; }
        .panel { background-color: #1e293b; padding: 20px; border-radius: 8px; margin-bottom: 20px; width: 100%; max-width: 500px; border: 1px solid #475569;}
        input[type=range] { width: 100%; margin: 10px 0; }
        button { padding: 8px 16px; background: #ef4444; color: white; border: none; border-radius: 4px; cursor: pointer; font-weight: bold; }
        button:hover { background: #dc2626; }
    </style>
</head>
<body>
    <div class="panel">
        <h2 style="margin-top: 0; color: #22d3ee;">Wave Superposition Engine</h2>
        <p style="color: #94a3b8;">Click on the canvas below to place wave sources.</p>
        <label style="font-weight: bold;">Attenuation (&alpha;): <span id="alphaValue" style="color: #22d3ee;">0.5</span></label>
        <input type="range" id="alphaSlider" min="0" max="2" step="0.1" value="0.5">
        <button onclick="clearSources()">Clear All Sources</button>
    </div>

    <canvas id="waveCanvas" width="200" height="200"></canvas>

    <script>
        const canvas = document.getElementById('waveCanvas');
        const ctx = canvas.getContext('2d');
        const alphaSlider = document.getElementById('alphaSlider');
        const alphaValueDisp = document.getElementById('alphaValue');

        let sources = [];
        let t = 0;
        const A = 50;     
        const k = 0.3;    
        const omega = 0.5; 
        
        const w = canvas.width;
        const h = canvas.height;
        const imgData = ctx.createImageData(w, h);
        const data = imgData.data;

        canvas.addEventListener('mousedown', (e) => {
            const rect = canvas.getBoundingClientRect();
            const scaleX = canvas.width / rect.width;
            const scaleY = canvas.height / rect.height;
            sources.push({
                x: (e.clientX - rect.left) * scaleX,
                y: (e.clientY - rect.top) * scaleY
            });
        });

        function clearSources() {
            sources = [];
        }

        function renderFrame() {
            let alpha = parseFloat(alphaSlider.value);
            alphaValueDisp.innerText = alpha.toFixed(1);
            const currentT = omega * t;

            for (let y = 0; y < h; y++) {
                for (let x = 0; x < w; x++) {
                    let totalU = 0;
                    for (let i = 0; i < sources.length; i++) {
                        let dx = x - sources[i].x;
                        let dy = y - sources[i].y;
                        let distance = Math.max(Math.sqrt(dx * dx + dy * dy), 1); 
                        
                        let attenuation = 1 / Math.pow(distance, alpha);
                        totalU += A * attenuation * Math.sin(k * distance - currentT);
                    }

                    let index = (y * w + x) * 4;
                    let brightness = Math.min(255, Math.abs(totalU) * 5); 
                    
                    if (totalU > 0) {
                        data[index] = 0; 
                        data[index+1] = brightness; 
                        data[index+2] = brightness; 
                    } else {
                        data[index] = brightness * 0.5; 
                        data[index+1] = 0; 
                        data[index+2] = brightness;
                    }
                    data[index + 3] = 255; 
                }
            }
            ctx.putImageData(imgData, 0, 0);

            ctx.fillStyle = '#ef4444';
            for (let i = 0; i < sources.length; i++) {
                ctx.beginPath(); 
                ctx.arc(sources[i].x, sources[i].y, 2, 0, Math.PI * 2); 
                ctx.fill();
            }

            t += 1;
            requestAnimationFrame(renderFrame);
        }
        renderFrame();
    </script>
</body>
</html>
