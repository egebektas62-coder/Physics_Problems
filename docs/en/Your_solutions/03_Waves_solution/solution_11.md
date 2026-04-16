# Animation: Young's Two-Slit Interference

## Necessary Definitions and Formulas

### 1. Young's Double-Slit Experiment
In 1801, Thomas Young demonstrated that light (and sound/water) behaves as a wave. When a single wavefront hits a barrier with two small slits, the slits act as two new, perfectly synchronized (coherent) point sources of waves.

### 2. Path Difference and Interference
The resulting wave pattern on a screen (or in space) depends on the **path difference** ($\Delta r = |r_1 - r_2|$).
* **Constructive Interference:** When the waves arrive "in phase" (peak meets peak), they add up to create a massive wave. This happens when the path difference is a full multiple of the wavelength ($n\lambda$).
* **Destructive Interference:** When the waves arrive "out of phase" (peak meets trough), they cancel each other out completely, creating a "dead zone". This happens when the path difference is a half multiple of the wavelength ($(n + 0.5)\lambda$).

### 3. The Superposition Equation
The total displacement of the wave $u(\vec{r},t)$ at any point is the sum of the partial waves from Slit 1 and Slit 2. Using the $1/r$ attenuation factor for spherical/cylindrical spreading:

$$
u(\vec{r},t) = \frac{A}{|\vec{r}-\vec{r_1}|} \sin(k |\vec{r} - \vec{r_1}| - \omega t) + \frac{A}{|\vec{r}-\vec{r_2}|} \sin(k |\vec{r} - \vec{r_2}| - \omega t)
$$

Where:
* **$\vec{r_1}, \vec{r_2}$**: Position vectors of the two slits.
* **$k$**: Wave number, directly tied to the wavelength by $k = \frac{2\pi}{\lambda}$.
* **$\omega$**: Angular frequency of the wave.

---

## Interactive HTML Engine: Young's Double Slit Simulator

The following HTML/JS engine simulates the two-slit interference pattern in real-time using CPU-based pixel rendering. Use the controls to adjust the physical distance between the slits ($d$) and the wavelength ($\lambda$) to observe how the interference fringes (constructive and destructive lines) change dynamically.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Two-Slit Interference Engine</title>
    <script src="[https://cdn.tailwindcss.com](https://cdn.tailwindcss.com)"></script>
    <style>
        body { background-color: #0f172a; color: white; font-family: monospace; }
        canvas { 
            background-color: #000; 
            border-radius: 8px; 
            border: 1px solid #334155; 
            width: 100%; 
            max-width: 600px; 
            image-rendering: pixelated;
        }
    </style>
</head>
<body class="flex flex-col items-center py-8 px-4">

    <div class="max-w-5xl w-full grid grid-cols-1 md:grid-cols-2 gap-6">
        <!-- Control Panel -->
        <div class="bg-slate-800 p-6 rounded-xl border border-slate-700 flex flex-col gap-4">
            <div>
                <h1 class="text-2xl font-bold text-emerald-400">Two-Slit Interference</h1>
                <p class="text-slate-400 text-sm mt-1">Live Wave Superposition & Fringe Analyzer</p>
            </div>
            
            <!-- Slit Distance Control -->
            <div class="bg-slate-900 p-3 rounded border border-emerald-900">
                <div class="flex justify-between mb-2">
                    <span class="text-slate-300 font-bold">Slit Distance (d): <span id="dValue" class="text-emerald-400">40 px</span></span>
                </div>
                <input type="range" id="dSlider" min="0" max="150" step="1" value="40" class="w-full h-2 bg-slate-600 rounded-lg appearance-none cursor-pointer">
            </div>

            <!-- Wavelength Control -->
            <div class="bg-slate-900 p-3 rounded border border-blue-900">
                <div class="flex justify-between mb-2">
                    <span class="text-slate-300 font-bold">Wavelength (&lambda;): <span id="lambdaValue" class="text-blue-400">15 px</span></span>
                </div>
                <input type="range" id="lambdaSlider" min="5" max="60" step="1" value="15" class="w-full h-2 bg-slate-600 rounded-lg appearance-none cursor-pointer">
            </div>
            
            <div class="text-xs text-slate-400 mt-auto bg-slate-900 p-3 rounded border border-slate-700">
                <strong>Analysis:</strong> 
                <ul class="list-disc pl-4 mt-1">
                    <li>Bright green bands = Constructive Interference (In Phase)</li>
                    <li>Black lines = Destructive Interference (Dead Zones)</li>
                    <li>Wider slit distance (d) creates more tightly packed fringes.</li>
                </ul>
            </div>
        </div>

        <!-- Simulation Canvas -->
        <div class="flex justify-center items-center relative">
            <span class="absolute top-2 left-2 bg-black/60 text-xs px-2 py-1 rounded text-emerald-400 font-mono z-10 border border-emerald-900 pointer-events-none">OPTICAL WAVE TANK</span>
            <!-- Internal resolution 250x250 mapped to larger CSS width -->
            <canvas id="waveCanvas" width="250" height="250"></canvas>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('waveCanvas');
        const ctx = canvas.getContext('2d');
        const dSlider = document.getElementById('dSlider');
        const dValueDisp = document.getElementById('dValue');
        const lambdaSlider = document.getElementById('lambdaSlider');
        const lambdaValueDisp = document.getElementById('lambdaValue');

        // Engine Parameters
        let t = 0;
        const omega = 0.5; // Time speed
        const A = 800;     // Base amplitude (high due to 1/r dropoff)
        
        // Canvas pixel data setup
        const w = canvas.width;
        const h = canvas.height;
        const imgData = ctx.createImageData(w, h);
        const data = imgData.data;

        // Slit Base Coordinates (Left side of the canvas)
        const slitX = 20;
        const centerY = h / 2;

        function renderFrame() {
            // Get user inputs
            let d = parseFloat(dSlider.value);
            let lambda = parseFloat(lambdaSlider.value);
            
            dValueDisp.innerText = d + " px";
            lambdaValueDisp.innerText = lambda + " px";

            // Calculate wave number k = 2*pi / lambda
            let k = (2 * Math.PI) / lambda;
            let currentT = omega * t;

            // Calculate Slit Y positions based on distance d
            let s1y = centerY - (d / 2);
            let s2y = centerY + (d / 2);

            // Loop through every pixel
            for (let y = 0; y < h; y++) {
                for (let x = 0; x < w; x++) {
                    // Calculate distances from pixel to both slits
                    let dx = x - slitX;
                    let dy1 = y - s1y;
                    let dy2 = y - s2y;
                    
                    let r1 = Math.max(Math.sqrt(dx*dx + dy1*dy1), 1); // Max(..., 1) prevents division by zero
                    let r2 = Math.max(Math.sqrt(dx*dx + dy2*dy2), 1);
                    
                    // Superposition Equation
                    let u1 = (A / r1) * Math.sin(k * r1 - currentT);
                    let u2 = (A / r2) * Math.sin(k * r2 - currentT);
                    let uTotal = u1 + u2;

                    // Color mapping (Green for positive/constructive, Dark for destructive)
                    let index = (y * w + x) * 4;
                    let intensity = Math.abs(uTotal) * 12; // Scaler for visibility

                    if (uTotal > 0) {
                        data[index] = 0;                            // R
                        data[index + 1] = Math.min(255, intensity); // G
                        data[index + 2] = Math.min(100, intensity/2); // B
                    } else {
                        data[index] = 0;                            // R
                        data[index + 1] = 0;                        // G
                        data[index + 2] = Math.min(255, intensity); // B
                    }
                    data[index + 3] = 255; // Alpha
                }
            }

            // Draw pixel array
            ctx.putImageData(imgData, 0, 0);

            // Draw Barrier and Slits visually
            ctx.fillStyle = '#64748b'; // Barrier color
            ctx.fillRect(slitX - 4, 0, 8, h); // Full barrier
            
            // "Punch holes" for the slits
            ctx.fillStyle = '#000000';
            ctx.fillRect(slitX - 5, s1y - 3, 10, 6);
            ctx.fillRect(slitX - 5, s2y - 3, 10, 6);

            // Draw bright dots at actual slit origins
            ctx.fillStyle = '#10b981';
            ctx.beginPath(); ctx.arc(slitX, s1y, 2, 0, Math.PI*2); ctx.fill();
            ctx.beginPath(); ctx.arc(slitX, s2y, 2, 0, Math.PI*2); ctx.fill();

            t += 1;
            requestAnimationFrame(renderFrame);
        }

        renderFrame();
    </script>
</body>
</html>
