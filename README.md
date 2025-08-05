
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Laiba Amjad | Futuristic Web Artisan</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vanta@latest/dist/vanta.net.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700&family=Montserrat:wght@300;400;600&display=swap');
        
        body {
            font-family: 'Montserrat', sans-serif;
            overflow-x: hidden;
        }
        
        .orbitron {
            font-family: 'Orbitron', sans-serif;
        }
        
        .gradient-text {
            background: linear-gradient(90deg, #00dbde, #fc00ff, #00dbde);
            background-size: 200% auto;
            color: transparent;
            -webkit-background-clip: text;
            background-clip: text;
            animation: gradient 3s linear infinite;
        }
        
        @keyframes gradient {
            0% { background-position: 0% center; }
            100% { background-position: 200% center; }
        }
        
        .card-hover {
            transition: all 0.3s ease;
            transform-style: preserve-3d;
        }
        
        .card-hover:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 25px 50px -12px rgba(236, 72, 153, 0.25);
        }
        
        .floating {
            animation: floating 6s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .glow {
            box-shadow: 0 0 15px rgba(236, 72, 153, 0.7);
        }
        
        .neon-border {
            border: 1px solid transparent;
            background: linear-gradient(#0f172a, #0f172a) padding-box,
                        linear-gradient(90deg, #00dbde, #fc00ff) border-box;
        }
        
        .code-block {
            font-family: 'Courier New', monospace;
            background: rgba(15, 23, 42, 0.7);
            border-left: 3px solid #fc00ff;
        }
    </style>
</head>
<body class="bg-slate-900 text-white min-h-screen">
    <div id="vanta-bg" class="fixed inset-0 -z-10"></div>
    
    <!-- Floating Particles -->
    <div class="fixed inset-0 overflow-hidden pointer-events-none">
        <div id="particles-js" class="absolute inset-0"></div>
    </div>
    
    <!-- Main Container -->
    <div class="container mx-auto px-4 py-12 relative z-10">
        <!-- Header -->
        <header class="flex justify-between items-center mb-20">
            <div class="text-2xl orbitron gradient-text">LAIBA AMJAD</div>
            <nav class="hidden md:flex space-x-8">
                <a href="#about" class="hover:text-pink-400 transition-colors">About</a>
                <a href="#skills" class="hover:text-pink-400 transition-colors">Skills</a>
                <a href="#experience" class="hover:text-pink-400 transition-colors">Experience</a>
                <a href="#contact" class="hover:text-pink-400 transition-colors">Contact</a>
            </nav>
            <button class="md:hidden text-2xl">☰</button>
        </header>
        
        <!-- Hero Section -->
        <section class="flex flex-col md:flex-row items-center justify-between mb-32">
            <div class="md:w-1/2 mb-12 md:mb-0">
                <h1 class="text-5xl md:text-7xl font-bold mb-6 orbitron">
                    <span class="gradient-text">Crafting Digital</span><br>
                    <span class="text-white">Masterpieces</span>
                </h1>
                <p class="text-xl mb-8 text-gray-300 leading-relaxed">
                    I transform ideas into immersive web experiences with cutting-edge HTML, CSS, and JavaScript.
                </p>
                <div class="flex space-x-4">
                    <a href="#contact" class="px-8 py-3 bg-gradient-to-r from-cyan-500 to-pink-500 rounded-full font-bold hover:opacity-90 transition-opacity">
                        Get in Touch
                    </a>
                    <a href="#experience" class="px-8 py-3 border border-pink-500 rounded-full font-bold hover:bg-pink-500 hover:bg-opacity-10 transition-colors">
                        My Work
                    </a>
                </div>
            </div>
            <div class="md:w-1/2 flex justify-center">
                <div id="3d-vector-container" class="w-64 h-64 md:w-80 md:h-80">
                    <canvas id="3d-canvas" class="w-full h-full"></canvas>
                </div>
            </div>
        </section>
        
        <!-- About Section -->
        <section id="about" class="mb-32">
            <h2 class="text-4xl font-bold mb-12 orbitron text-center">
                <span class="gradient-text">About Me</span>
            </h2>
            <div class="flex flex-col md:flex-row gap-8">
                <div class="md:w-1/2 bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <h3 class="text-2xl font-bold mb-4 orbitron">The Artisan</h3>
                    <p class="text-gray-300 mb-6 leading-relaxed">
                        With a passion for pixel-perfect designs and seamless user experiences, I craft websites that are not just functional but tell a story. My approach combines aesthetic elegance with technical precision.
                    </p>
                    <p class="text-gray-300 leading-relaxed">
                        Every line of code I write is a brushstroke in the digital canvas, creating immersive experiences that captivate and engage users from the first interaction.
                    </p>
                </div>
                <div class="md:w-1/2 bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <h3 class="text-2xl font-bold mb-4 orbitron">The Vision</h3>
                    <p class="text-gray-300 mb-6 leading-relaxed">
                        In a world where digital presence is paramount, I believe in creating websites that stand out - not just visually, but in their ability to communicate brand essence and user value.
                    </p>
                    <div class="code-block p-4 rounded-lg my-4">
                        <span class="text-pink-400">/* My Philosophy */</span><br>
                        <span class="text-cyan-400">function</span> <span class="text-white">createWebsite</span>() {<br>
                        &nbsp;&nbsp;<span class="text-gray-400">// Blend beauty with functionality</span><br>
                        &nbsp;&nbsp;<span class="text-cyan-400">return</span> <span class="text-yellow-300">design</span> + <span class="text-yellow-300">code</span> + <span class="text-yellow-300">soul</span>;<br>
                        }
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Skills Section -->
        <section id="skills" class="mb-32">
            <h2 class="text-4xl font-bold mb-12 orbitron text-center">
                <span class="gradient-text">Technical Arsenal</span>
            </h2>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <!-- Skill Cards -->
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-xl p-6 text-center neon-border card-hover">
                    <div class="text-5xl mb-4">🖥️</div>
                    <h3 class="text-xl font-bold mb-2 orbitron">HTML5</h3>
                    <p class="text-gray-300 text-sm">Semantic, Accessible, Modern</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-cyan-500 to-pink-500 rounded-full"></div>
                </div>
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-xl p-6 text-center neon-border card-hover">
                    <div class="text-5xl mb-4">🎨</div>
                    <h3 class="text-xl font-bold mb-2 orbitron">CSS3</h3>
                    <p class="text-gray-300 text-sm">Animations, Grid, Flexbox</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-cyan-500 to-pink-500 rounded-full"></div>
                </div>
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-xl p-6 text-center neon-border card-hover">
                    <div class="text-5xl mb-4">⚡</div>
                    <h3 class="text-xl font-bold mb-2 orbitron">JavaScript</h3>
                    <p class="text-gray-300 text-sm">ES6+, DOM Manipulation</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-cyan-500 to-pink-500 rounded-full"></div>
                </div>
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-xl p-6 text-center neon-border card-hover">
                    <div class="text-5xl mb-4">🌀</div>
                    <h3 class="text-xl font-bold mb-2 orbitron">Tailwind</h3>
                    <p class="text-gray-300 text-sm">Utility-First CSS</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-cyan-500 to-pink-500 rounded-full"></div>
                </div>
            </div>
            
            <!-- Additional Skills -->
            <div class="mt-12 bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border">
                <h3 class="text-2xl font-bold mb-6 orbitron">Specialized Expertise</h3>
                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
                    <div class="flex items-center space-x-2">
                        <div class="w-2 h-2 rounded-full bg-pink-500"></div>
                        <span>Responsive Design</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <div class="w-2 h-2 rounded-full bg-pink-500"></div>
                        <span>CSS Animations</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <div class="w-2 h-2 rounded-full bg-pink-500"></div>
                        <span>3D Web Elements</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <div class="w-2 h-2 rounded-full bg-pink-500"></div>
                        <span>Performance Optimization</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <div class="w-2 h-2 rounded-full bg-pink-500"></div>
                        <span>Cross-Browser Compatibility</span>
                    </div>
                    <div class="flex items-center space-x-2">
                        <div class="w-2 h-2 rounded-full bg-pink-500"></div>
                        <span>UI/UX Principles</span>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Experience Section -->
        <section id="experience" class="mb-32">
            <h2 class="text-4xl font-bold mb-12 orbitron text-center">
                <span class="gradient-text">Professional Journey</span>
            </h2>
            
            <div class="space-y-8">
                <!-- Experience 1 -->
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4">
                        <h3 class="text-2xl font-bold orbitron">Senior Frontend Developer</h3>
                        <div class="text-pink-400 orbitron">2021 - Present</div>
                    </div>
                    <div class="text-xl text-cyan-400 mb-4">Digital Innovations Inc.</div>
                    <p class="text-gray-300 mb-4">
                        Lead the frontend development team in creating immersive web experiences for Fortune 500 clients. Spearheaded the adoption of modern CSS techniques that reduced development time by 40%.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">HTML5</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">CSS3</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">JavaScript</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">Tailwind</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">WebGL</span>
                    </div>
                </div>
                
                <!-- Experience 2 -->
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4">
                        <h3 class="text-2xl font-bold orbitron">UI/UX Specialist</h3>
                        <div class="text-pink-400 orbitron">2019 - 2021</div>
                    </div>
                    <div class="text-xl text-cyan-400 mb-4">Creative Web Solutions</div>
                    <p class="text-gray-300 mb-4">
                        Designed and implemented responsive user interfaces for diverse clients across industries. Developed a CSS framework that improved consistency across projects and reduced client approval time by 35%.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">HTML5</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">CSS3</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">SASS</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">Bootstrap</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">Figma</span>
                    </div>
                </div>
                
                <!-- Experience 3 -->
                <div class="bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4">
                        <h3 class="text-2xl font-bold orbitron">Frontend Developer</h3>
                        <div class="text-pink-400 orbitron">2017 - 2019</div>
                    </div>
                    <div class="text-xl text-cyan-400 mb-4">TechStart Ventures</div>
                    <p class="text-gray-300 mb-4">
                        Built responsive websites and web applications for startups. Introduced modern CSS techniques that enhanced visual appeal while maintaining performance standards.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">HTML5</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">CSS3</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">JavaScript</span>
                        <span class="px-3 py-1 bg-slate-700 rounded-full text-sm">jQuery</span>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section id="contact" class="mb-20">
            <h2 class="text-4xl font-bold mb-12 orbitron text-center">
                <span class="gradient-text">Let's Collaborate</span>
            </h2>
            
            <div class="flex flex-col md:flex-row gap-8">
                <div class="md:w-1/2 bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <h3 class="text-2xl font-bold mb-6 orbitron">Get in Touch</h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start space-x-4">
                            <div class="text-2xl">📧</div>
                            <div>
                                <h4 class="font-bold orbitron">Email</h4>
                                <a href="mailto:abeerahamjad12@gmail.com" class="text-cyan-400 hover:underline">abeerahamjad12@gmail.com</a>
                            </div>
                        </div>
                        
                        <div class="flex items-start space-x-4">
                            <div class="text-2xl">📱</div>
                            <div>
                                <h4 class="font-bold orbitron">WhatsApp</h4>
                                <a href="https://wa.me/923214595311" class="text-cyan-400 hover:underline">+92 321 4595311</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Live Contact Form -->
                    <form class="mt-8 space-y-4">
                        <div>
                            <label for="name" class="block mb-2">Your Name</label>
                            <input type="text" id="name" class="w-full bg-slate-700 bg-opacity-50 border border-slate-600 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-pink-500">
                        </div>
                        <div>
                            <label for="email" class="block mb-2">Your Email</label>
                            <input type="email" id="email" class="w-full bg-slate-700 bg-opacity-50 border border-slate-600 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-pink-500">
                        </div>
                        <div>
                            <label for="message" class="block mb-2">Your Message</label>
                            <textarea id="message" rows="4" class="w-full bg-slate-700 bg-opacity-50 border border-slate-600 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-pink-500"></textarea>
                        </div>
                        <button type="submit" class="w-full py-3 bg-gradient-to-r from-cyan-500 to-pink-500 rounded-lg font-bold hover:opacity-90 transition-opacity">
                            Send Message
                        </button>
                    </form>
                </div>
                
                <div class="md:w-1/2 bg-slate-800 bg-opacity-50 backdrop-blur-lg rounded-2xl p-8 neon-border card-hover">
                    <h3 class="text-2xl font-bold mb-6 orbitron">Current Availability</h3>
                    
                    <div class="flex items-center space-x-4 mb-6">
                        <div class="w-4 h-4 rounded-full bg-green-500 animate-pulse"></div>
                        <span class="text-lg">Available for select projects</span>
                    </div>
                    
                    <div class="space-y-6">
                        <div>
                            <h4 class="font-bold orbitron mb-2">Project Types</h4>
                            <ul class="space-y-2">
                                <li class="flex items-center space-x-2">
                                    <span>✔️</span>
                                    <span>Custom Website Development</span>
                                </li>
                                <li class="flex items-center space-x-2">
                                    <span>✔️</span>
                                    <span>UI/UX Overhauls</span>
                                </li>
                                <li class="flex items-center space-x-2">
                                    <span>✔️</span>
                                    <span>CSS Architecture</span>
                                </li>
                                <li class="flex items-center space-x-2">
                                    <span>✔️</span>
                                    <span>Interactive Web Elements</span>
                                </li>
                            </ul>
                        </div>
                        
                        <div>
                            <h4 class="font-bold orbitron mb-2">Response Time</h4>
                            <div class="bg-slate-700 bg-opacity-50 rounded-lg p-4">
                                <div class="flex justify-between mb-2">
                                    <span>Email:</span>
                                    <span class="text-cyan-400">Within 24 hours</span>
                                </div>
                                <div class="flex justify-between">
                                    <span>WhatsApp:</span>
                                    <span class="text-cyan-400">Within 12 hours</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 3D Interactive Element -->
                    <div class="mt-8 h-48 bg-slate-700 bg-opacity-30 rounded-xl flex items-center justify-center border border-dashed border-cyan-400 border-opacity-30">
                        <div class="text-center">
                            <div class="text-3xl mb-2">🌐</div>
                            <p class="text-sm text-gray-400">Interactive Web Experience</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Footer -->
        <footer class="text-center py-8 border-t border-slate-800">
            <div class="orbitron text-xl mb-4 gradient-text">LAIBA AMJAD</div>
            <p class="text-gray-400">© 2023 All Rights Reserved</p>
        </footer>
    </div>
    
    <!-- Floating Elements -->
    <div class="fixed top-1/4 left-10 w-4 h-4 rounded-full bg-pink-500 opacity-20 blur-md floating" style="animation-delay: 0s;"></div>
    <div class="fixed top-1/3 right-20 w-6 h-6 rounded-full bg-cyan-500 opacity-20 blur-md floating" style="animation-delay: 1s;"></div>
    <div class="fixed bottom-1/4 left-1/4 w-8 h-8 rounded-full bg-purple-500 opacity-20 blur-lg floating" style="animation-delay: 2s;"></div>
    
    <script>
        // Initialize Vanta.js background
        VANTA.NET({
            el: "#vanta-bg",
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            minHeight: 200.00,
            minWidth: 200.00,
            scale: 1.00,
            scaleMobile: 1.00,
            color: 0x3f82ff,
            backgroundColor: 0x111827,
            points: 12.00,
            maxDistance: 22.00,
            spacing: 18.00
        });
        
        // Initialize Three.js 3D vector
        const container = document.getElementById('3d-vector-container');
        const canvas = document.getElementById('3d-canvas');
        
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, 1, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({
            canvas: canvas,
            alpha: true,
            antialias: true
        });
        renderer.setSize(canvas.clientWidth, canvas.clientHeight);
        
        // Create a floating torus knot
        const geometry = new THREE.TorusKnotGeometry(1, 0.4, 100, 16);
        const material = new THREE.MeshPhongMaterial({
            color: 0xfc00ff,
            emissive: 0x00dbde,
            emissiveIntensity: 0.5,
            shininess: 100,
            wireframe: false
        });
        const knot = new THREE.Mesh(geometry, material);
        scene.add(knot);
        
        // Add lights
        const ambientLight = new THREE.AmbientLight(0x404040);
        scene.add(ambientLight);
        
        const directionalLight = new THREE.DirectionalLight(0xffffff, 1);
        directionalLight.position.set(1, 1, 1);
        scene.add(directionalLight);
        
        camera.position.z = 3;
        
        // Animation loop
        function animate() {
            requestAnimationFrame(animate);
            knot.rotation.x += 0.005;
            knot.rotation.y += 0.01;
            renderer.render(scene, camera);
        }
        animate();
        
        // Handle window resize
        window.addEventListener('resize', () => {
            camera.aspect = 1;
            camera.updateProjectionMatrix();
            renderer.setSize(canvas.clientWidth, canvas.clientHeight);
        });
        
        // Simple form submission handler
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });
        
        // Mobile menu toggle
        document.querySelector('button').addEventListener('click', function() {
            const nav = document.querySelector('nav');
            nav.classList.toggle('hidden');
            nav.classList.toggle('flex');
            nav.classList.toggle('flex-col');
            nav.classList.toggle('absolute');
            nav.classList.toggle('top-20');
            nav.classList.toggle('right-4');
            nav.classList.toggle('bg-slate-900');
            nav.classList.toggle('p-4');
            nav.classList.toggle('rounded-lg');
            nav.classList.toggle('space-y-4');
            nav.classList.toggle('space-x-0');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
