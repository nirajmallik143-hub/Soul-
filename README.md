<!DOCTYPE html>
<html lang="en" class="h-full">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D README Showcase // Soul- (nirajmallik143-hub)</title>
    <!-- Tailwind CSS for sleek glassmorphism and modern UI styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Three.js for 3D Quantum Particle / Floating Cube simulation -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;900&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .font-mono { font-family: 'JetBrains Mono', monospace; }
        .glass-card {
            background: rgba(15, 23, 42, 0.75);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(56, 189, 248, 0.2);
            box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.5);
        }
        .glass-panel {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        canvas { display: block; }
        /* Custom scrollbar */
        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: #090d16; }
        ::-webkit-scrollbar-thumb { background: #1e293b; border-radius: 3px; }
        ::-webkit-scrollbar-thumb:hover { background: #38bdf8; }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 h-full overflow-x-hidden flex flex-col relative">

    <!-- 3D Canvas Background Container -->
    <div id="canvas-container" class="fixed inset-0 z-0 pointer-events-auto"></div>

    <!-- Header Navigation -->
    <header class="relative z-20 border-b border-slate-800/80 bg-slate-950/80 backdrop-blur-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="w-9 h-9 rounded-xl bg-gradient-to-tr from-cyan-500 to-indigo-600 flex items-center justify-center shadow-lg shadow-cyan-500/30">
                    <span class="text-white font-black text-lg">⚛</span>
                </div>
                <div>
                    <a href="https://github.com/nirajmallik143-hub/Soul-" target="_blank" class="font-bold text-slate-100 hover:text-cyan-400 transition tracking-tight flex items-center space-x-2">
                        <span>nirajmallik143-hub / Soul-</span>
                        <span class="text-[10px] bg-cyan-500/20 text-cyan-300 px-2 py-0.5 rounded-full border border-cyan-500/30 font-mono">PUBLIC</span>
                    </a>
                    <p class="text-[11px] text-slate-400">LiveLife OS // MAX Generation 3D Interactive README</p>
                </div>
            </div>
            <div class="flex items-center space-x-3">
                <button id="btnToggleQuantum" class="hidden sm:flex items-center space-x-2 bg-slate-900 hover:bg-slate-800 text-cyan-400 text-xs px-3 py-1.5 rounded-lg border border-slate-700 transition font-mono">
                    <span>⚡ <span id="modeText">QUANTUM WAVE: ON</span></span>
                </button>
                <a href="https://github.com/nirajmallik143-hub/Soul-" target="_blank" class="bg-cyan-500 hover:bg-cyan-400 text-slate-950 font-bold px-4 py-2 rounded-xl text-xs transition shadow-lg shadow-cyan-500/20 flex items-center space-x-1.5">
                    <span>⭐ Star on GitHub</span>
                </a>
            </div>
        </div>
    </header>

    <!-- Main Showcase Layout -->
    <main class="relative z-10 flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-8">

        <!-- Hero Section -->
        <section class="glass-card rounded-3xl p-6 sm:p-10 relative overflow-hidden">
            <div class="absolute -right-20 -top-20 w-80 h-80 bg-cyan-500/10 rounded-full blur-3xl pointer-events-none"></div>
            <div class="absolute -left-20 -bottom-20 w-80 h-80 bg-indigo-500/10 rounded-full blur-3xl pointer-events-none"></div>

            <div class="max-w-3xl relative z-10">
                <div class="inline-flex items-center space-x-2 bg-cyan-500/10 text-cyan-300 border border-cyan-500/30 px-3 py-1 rounded-full text-xs font-mono mb-4">
                    <span>🚀 IMMERSIVE 3D REPOSITORY SHOWCASE</span>
                </div>
                <h1 class="text-3xl sm:text-5xl font-black text-white tracking-tight leading-tight">
                    Welcome to <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 via-indigo-400 to-purple-400">Soul-</span>
                </h1>
                <p class="mt-4 text-slate-300 text-sm sm:text-base leading-relaxed">
                    A quantum-inspired life management and execution system. This interactive 3D showcase renders the core probability waves of <strong class="text-cyan-300 font-mono">LiveLife OS // MAX Generation</strong>, offering live code inspection, repository statistics, and instant Markdown embedding.
                </p>

                <div class="mt-8 flex flex-wrap items-center gap-4">
                    <a href="#codeExplorer" class="px-6 py-3 bg-gradient-to-r from-cyan-500 to-indigo-600 hover:from-cyan-400 hover:to-indigo-500 text-slate-950 font-bold rounded-xl text-xs uppercase tracking-wider transition shadow-lg shadow-cyan-500/25 flex items-center space-x-2">
                        <span>📂 Explore Repository Files</span>
                    </a>
                    <a href="#markdownGenerator" class="px-6 py-3 bg-slate-900 hover:bg-slate-800 text-cyan-300 border border-slate-700 font-bold rounded-xl text-xs uppercase tracking-wider transition flex items-center space-x-2 font-mono">
                        <span>📋 Get 3D Markdown Embed</span>
                    </a>
                </div>
            </div>

            <!-- Quick Repository Stats Grid -->
            <div class="mt-10 grid grid-cols-2 sm:grid-cols-4 gap-4 pt-6 border-t border-slate-800/80">
                <div class="glass-panel p-4 rounded-2xl">
                    <div class="text-[11px] font-mono text-slate-400 uppercase">Primary Language</div>
                    <div class="text-lg font-bold text-cyan-400 mt-1 flex items-center space-x-2">
                        <span class="w-3 h-3 rounded-full bg-orange-400 inline-block"></span>
                        <span>HTML5 / JS</span>
                    </div>
                </div>
                <div class="glass-panel p-4 rounded-2xl">
                    <div class="text-[11px] font-mono text-slate-400 uppercase">License</div>
                    <div class="text-lg font-bold text-indigo-400 mt-1">MIT License</div>
                </div>
                <div class="glass-panel p-4 rounded-2xl">
                    <div class="text-[11px] font-mono text-slate-400 uppercase">QKD Coherence</div>
                    <div class="text-lg font-bold text-emerald-400 mt-1 font-mono">99.98%</div>
                </div>
                <div class="glass-panel p-4 rounded-2xl">
                    <div class="text-[11px] font-mono text-slate-400 uppercase">Superposition States</div>
                    <div class="text-lg font-bold text-amber-400 mt-1 font-mono">1.04M+</div>
                </div>
            </div>
        </section>

        <!-- Live Code Explorer Section -->
        <section id="codeExplorer" class="glass-card rounded-3xl p-6 sm:p-8">
            <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 mb-6">
                <div>
                    <h2 class="text-xl font-bold text-white flex items-center space-x-2">
                        <span>📄 Repository File Explorer</span>
                    </h2>
                    <p class="text-xs text-slate-400 mt-1">Inspect live source code for index.html and LICENSE right here in the browser.</p>
                </div>
                <div class="flex items-center space-x-2 bg-slate-900 p-1.5 rounded-xl border border-slate-800">
                    <button id="tabIndexHtml" onclick="switchTab('index')" class="px-4 py-2 rounded-lg text-xs font-mono font-bold transition bg-cyan-500 text-slate-950 shadow">
                        index.html
                    </button>
                    <button id="tabLicense" onclick="switchTab('license')" class="px-4 py-2 rounded-lg text-xs font-mono font-bold transition text-slate-400 hover:text-white">
                        LICENSE
                    </button>
                </div>
            </div>

            <!-- Code Viewer Container -->
            <div class="bg-slate-950 rounded-2xl border border-slate-800 overflow-hidden shadow-2xl">
                <div class="bg-slate-900/90 px-4 py-3 border-b border-slate-800 flex items-center justify-between">
                    <div class="flex items-center space-x-2">
                        <span class="w-3 h-3 rounded-full bg-red-500/80 inline-block"></span>
                        <span class="w-3 h-3 rounded-full bg-amber-500/80 inline-block"></span>
                        <span class="w-3 h-3 rounded-full bg-emerald-500/80 inline-block"></span>
                        <span id="codeFileName" class="ml-2 font-mono text-xs text-slate-300 font-semibold">index.html</span>
                    </div>
                    <button onclick="copyCode()" class="text-xs font-mono text-cyan-400 hover:text-cyan-300 bg-cyan-500/10 hover:bg-cyan-500/20 px-3 py-1.5 rounded-lg border border-cyan-500/30 transition flex items-center space-x-1.5">
                        <span id="copyText">📋 Copy Code</span>
                    </button>
                </div>
                <div class="p-4 sm:p-6 max-h-96 overflow-y-auto font-mono text-xs text-slate-300 leading-relaxed">
                    <pre id="codeContent" class="whitespace-pre-wrap"></pre>
                </div>
            </div>
        </section>

        <!-- Markdown Embedding & Generator Section -->
        <section id="markdownGenerator" class="glass-card rounded-3xl p-6 sm:p-8">
            <div class="max-w-2xl mb-6">
                <h2 class="text-xl font-bold text-white">📋 GitHub 3D README Markdown Generator</h2>
                <p class="text-xs text-slate-400 mt-1">Copy the Markdown snippet below to feature this interactive 3D README showcase directly on your GitHub profile or repository page.</p>
            </div>

            <div class="bg-slate-950 rounded-2xl border border-slate-800 p-4 sm:p-6 relative">
                <div class="flex items-center justify-between mb-3 pb-3 border-b border-slate-800">
                    <span class="font-mono text-xs text-cyan-400 font-semibold">README.md Badge & Embed Snippet</span>
                    <button onclick="copyMarkdown()" class="bg-indigo-600 hover:bg-indigo-500 text-white font-mono text-xs px-4 py-2 rounded-xl transition shadow-lg shadow-indigo-600/30 flex items-center space-x-1.5">
                        <span id="copyMarkdownText">📋 Copy Markdown</span>
                    </button>
                </div>
                <pre class="font-mono text-xs text-slate-300 bg-slate-900/80 p-4 rounded-xl border border-slate-800 overflow-x-auto select-all" id="markdownSnippet">[![Soul- 3D README Showcase](https://img.shields.io/badge/Soul--%203D%20README-Interactive-cyan?style=for-the-badge&logo=github)](https://nirajmallik143-hub.github.io/Soul-/)

### ⚛ Soul- // LiveLife OS MAX Generation
Explore the live 3D quantum life management platform:
👉 **[View Live Interactive 3D Showcase](https://nirajmallik143-hub.github.io/Soul-/)**</pre>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="relative z-10 bg-slate-950 border-t border-slate-900 py-6 mt-12 text-center text-xs text-slate-500">
        <p>Soul- Repository Showcase • Built with Three.js & Tailwind CSS for Niraj Mallik (<span class="font-mono text-slate-400">nirajmallik143-hub</span>)</p>
    </footer>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-20 opacity-0 transition-all duration-300 bg-cyan-500 text-slate-950 font-bold px-6 py-3 rounded-2xl shadow-2xl flex items-center space-x-2 text-xs font-mono">
        <span>✨ Copied to clipboard successfully!</span>
    </div>

    <!-- Application JavaScript -->
    <script>
        // --- 1. Three.js Interactive Quantum Particle & Floating Cube Background ---
        let scene, camera, renderer, particles, cubes = [], waveMesh;
        let mouseX = 0, mouseY = 0;
        let windowHalfX = window.innerWidth / 2;
        let windowHalfY = window.innerHeight / 2;
        let quantumActive = true;

        function initThree() {
            const container = document.getElementById('canvas-container');
            
            scene = new THREE.Scene();
            scene.fog = new THREE.FogExp2(0x090d16, 0.002);

            camera = new THREE.PerspectiveCamera(60, window.innerWidth / window.innerHeight, 1, 1000);
            camera.position.z = 400;

            renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
            container.appendChild(renderer.domElement);

            // Particle Field
            const particleCount = 1200;
            const geometry = new THREE.BufferGeometry();
            const positions = new Float32Array(particleCount * 3);
            const colors = new Float32Array(particleCount * 3);

            const colorCyan = new THREE.Color(0x06b6d4);
            const colorIndigo = new THREE.Color(0x6366f1);

            for (let i = 0; i < particleCount * 3; i += 3) {
                positions[i] = (Math.random() - 0.5) * 1000;
                positions[i + 1] = (Math.random() - 0.5) * 1000;
                positions[i + 2] = (Math.random() - 0.5) * 1000;

                const mixedColor = Math.random() > 0.5 ? colorCyan : colorIndigo;
                colors[i] = mixedColor.r;
                colors[i + 1] = mixedColor.g;
                colors[i + 2] = mixedColor.b;
            }

            geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));
            geometry.setAttribute('color', new THREE.BufferAttribute(colors, 3));

            const material = new THREE.PointsMaterial({
                size: 3.5,
                vertexColors: true,
                transparent: true,
                opacity: 0.8,
                blending: THREE.AdditiveBlending
            });

            particles = new THREE.Points(geometry, material);
            scene.add(particles);

            // Floating Quantum Cubes
            const cubeGeo = new THREE.BoxGeometry(18, 18, 18);
            for (let i = 0; i < 15; i++) {
                const cubeMat = new THREE.MeshBasicMaterial({
                    color: i % 2 === 0 ? 0x06b6d4 : 0x6366f1,
                    wireframe: true,
                    transparent: true,
                    opacity: 0.35
                });
                const cube = new THREE.Mesh(cubeGeo, cubeMat);
                cube.position.set(
                    (Math.random() - 0.5) * 600,
                    (Math.random() - 0.5) * 600,
                    (Math.random() - 0.5) * 400
                );
                cube.rotation.set(Math.random() * Math.PI, Math.random() * Math.PI, 0);
                scene.add(cube);
                cubes.push({ mesh: cube, rotSpeedX: (Math.random() - 0.5) * 0.01, rotSpeedY: (Math.random() - 0.5) * 0.01 });
            }

            window.addEventListener('resize', onWindowResize);
            document.addEventListener('mousemove', onDocumentMouseMove);
        }

        function onWindowResize() {
            windowHalfX = window.innerWidth / 2;
            windowHalfY = window.innerHeight / 2;
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        }

        function onDocumentMouseMove(event) {
            mouseX = (event.clientX - windowHalfX) * 0.2;
            mouseY = (event.clientY - windowHalfY) * 0.2;
        }

        function animateThree() {
            requestAnimationFrame(animateThree);

            if (quantumActive) {
                const time = Date.now() * 0.001;
                particles.rotation.y = time * 0.05;
                particles.rotation.x = time * 0.02;

                cubes.forEach((item) => {
                    item.mesh.rotation.x += item.rotSpeedX;
                    item.mesh.rotation.y += item.rotSpeedY;
                });

                camera.position.x += (mouseX - camera.position.x) * 0.05;
                camera.position.y += (-mouseY - camera.position.y) * 0.05;
                camera.lookAt(scene.position);
            }

            renderer.render(scene, camera);
        }

        window.onload = function () {
            initThree();
            animateThree();
            loadCodeContent('index');
        };

        // --- 2. Code Viewer Data & Switching ---
        const indexHtmlCode = `<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LiveLife OS // MAX Generation</title>
    <!-- Quantum Superposition Engine & QKD Security Vault -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body class="bg-slate-50 text-slate-800 font-sans">
    <!-- LiveLife OS MAX Generation v4.0 Application Root -->
    <header class="bg-slate-900 text-white p-4">
        <h1 class="text-2xl text-cyan-400 font-bold">⚛ LiveLife OS // MAX Generation</h1>
    </header>
    <!-- Main Quantum Superposition Console & Visualizers -->
</body>
</html>`;

        const licenseCode = `MIT License

Copyright (c) 2026 Niraj Mallik (nirajmallik143-hub)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.`;

        let currentActiveTab = 'index';

        function switchTab(tab) {
            currentActiveTab = tab;
            const btnIndex = document.getElementById('tabIndexHtml');
            const btnLicense = document.getElementById('tabLicense');
            const fileName = document.getElementById('codeFileName');

            if (tab === 'index') {
                btnIndex.className = 'px-4 py-2 rounded-lg text-xs font-mono font-bold transition bg-cyan-500 text-slate-950 shadow';
                btnLicense.className = 'px-4 py-2 rounded-lg text-xs font-mono font-bold transition text-slate-400 hover:text-white';
                fileName.textContent = 'index.html';
                loadCodeContent('index');
            } else {
                btnLicense.className = 'px-4 py-2 rounded-lg text-xs font-mono font-bold transition bg-indigo-600 text-white shadow';
                btnIndex.className = 'px-4 py-2 rounded-lg text-xs font-mono font-bold transition text-slate-400 hover:text-white';
                fileName.textContent = 'LICENSE';
                loadCodeContent('license');
            }
        }

        function loadCodeContent(type) {
            const pre = document.getElementById('codeContent');
            pre.textContent = type === 'index' ? indexHtmlCode : licenseCode;
        }

        // --- 3. Clipboard Utilities & Toast ---
        function showToast() {
            const toast = document.getElementById('toast');
            toast.classList.remove('translate-y-20', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');
            setTimeout(() => {
                toast.classList.remove('translate-y-0', 'opacity-100');
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 2500);
        }

        function copyCode() {
            const textToCopy = currentActiveTab === 'index' ? indexHtmlCode : licenseCode;
            const textArea = document.createElement('textarea');
            textArea.value = textToCopy;
            document.body.appendChild(textArea);
            textArea.select();
            document.execCommand('copy');
            document.body.removeChild(textArea);

            const copyText = document.getElementById('copyText');
            copyText.textContent = '✨ Copied!';
            showToast();
            setTimeout(() => { copyText.textContent = '📋 Copy Code'; }, 2000);
        }

        function copyMarkdown() {
            const markdownSnippet = document.getElementById('markdownSnippet').textContent;
            const textArea = document.createElement('textarea');
            textArea.value = markdownSnippet;
            document.body.appendChild(textArea);
            textArea.select();
            document.execCommand('copy');
            document.body.removeChild(textArea);

            const copyBtn = document.getElementById('copyMarkdownText');
            copyBtn.textContent = '✨ Copied!';
            showToast();
            setTimeout(() => { copyBtn.textContent = '📋 Copy Markdown'; }, 2000);
        }

        // Quantum Toggle Button Handler
        const btnToggleQuantum = document.getElementById('btnToggleQuantum');
        const modeText = document.getElementById('modeText');
        btnToggleQuantum.addEventListener('click', () => {
            quantumActive = !quantumActive;
            if (quantumActive) {
                modeText.textContent = 'QUANTUM WAVE: ON';
                btnToggleQuantum.classList.replace('border-red-700', 'border-slate-700');
            } else {
                modeText.textContent = 'QUANTUM WAVE: PAUSED';
                btnToggleQuantum.classList.replace('border-slate-700', 'border-red-700');
            }
        });
    </script>
</body>
</html>
