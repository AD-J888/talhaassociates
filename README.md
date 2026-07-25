
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Talha Associates | Architectural Planning & 3D Interior Design</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        gold: {
                            400: '#E2C044',
                            500: '#D4AF37',
                            600: '#B89628',
                            700: '#997B1E'
                        },
                        navy: {
                            800: '#0B132B',
                            900: '#070B19',
                            950: '#03050D'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Playfair Display', 'serif']
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts & FontAwesome -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,600;0,700;1,400&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #070B19;
            color: #f3f4f6;
        }
        .font-serif {
            font-family: 'Playfair Display', serif;
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #FFF099 0%, #D4AF37 50%, #AA7C11 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-gradient-bg {
            background: linear-gradient(135deg, #D4AF37 0%, #AA7C11 100%);
        }
        .gold-gradient-border {
            border-image: linear-gradient(135deg, #D4AF37, #AA7C11) 1;
        }
        .glass-card {
            background: rgba(15, 23, 42, 0.75);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        .glass-card:hover {
            border-color: rgba(212, 175, 55, 0.6);
            box-shadow: 0 10px 30px -10px rgba(212, 175, 55, 0.25);
        }
        /* Comparison Slider Styles */
        .img-comp-container {
            position: relative;
            height: 450px;
            overflow: hidden;
        }
        .img-comp-img {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        .img-comp-overlay {
            width: 50%;
            border-right: 3px solid #D4AF37;
        }
        .img-comp-slider {
            position: absolute;
            z-index: 9;
            cursor: ew-resize;
            width: 44px;
            height: 44px;
            background-color: #D4AF37;
            opacity: 0.9;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 0 15px rgba(0,0,0,0.5);
            color: #000;
        }
    </style>
</head>
<body class="selection:bg-gold-500 selection:text-black">

    <!-- HEADER / NAVIGATION -->
    <header class="fixed top-0 left-0 right-0 z-50 glass-card transition-all duration-300 py-3 px-4 lg:px-12 border-b border-gold-500/20">
        <div class="max-w-7xl mx-auto flex items-center justify-between">
            <!-- Logo -->
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-lg gold-gradient-bg flex items-center justify-center shadow-lg group-hover:scale-105 transition-transform">
                    <i class="fa-solid fa-building text-black text-xl"></i>
                </div>
                <div>
                    <span class="text-xl lg:text-2xl font-bold tracking-wider block leading-none font-serif text-white">TALHA</span>
                    <span class="text-xs tracking-widest text-gold-500 font-semibold block mt-0.5">ASSOCIATES</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
                <a href="#home" class="hover:text-gold-500 transition-colors">Home</a>
                <a href="#services" class="hover:text-gold-500 transition-colors">Services</a>
                <a href="#portfolio" class="hover:text-gold-500 transition-colors">Portfolio</a>
                <a href="#calculator" class="hover:text-gold-500 transition-colors">Cost Estimator</a>
                <a href="#about" class="hover:text-gold-500 transition-colors">About Us</a>
                <a href="#contact" class="hover:text-gold-500 transition-colors">Contact</a>
            </nav>

            <!-- Header Action Button -->
            <div class="hidden md:flex items-center gap-4">
                <a href="https://wa.me/923237047546?text=Hello%20Talha%20Associates,%20I%20would%20like%20to%20inquire%20about%20your%20building%20planning%20and%20designing%20services." 
                   target="_blank" 
                   class="gold-gradient-bg text-black font-semibold px-5 py-2.5 rounded-full hover:shadow-lg hover:shadow-gold-500/20 transition-all flex items-center gap-2">
                    <i class="fa-brands fa-whatsapp text-lg"></i>
                    <span>Contact Us</span>
                </a>
            </div>

            <!-- Mobile Hamburger Menu Button -->
            <button id="mobile-menu-btn" class="md:hidden text-2xl text-gold-500 focus:outline-none" aria-label="Toggle Navigation">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- Mobile Navigation Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden mt-3 pt-3 border-t border-slate-800 flex flex-col space-y-3 px-2 pb-3">
            <a href="#home" class="mobile-link text-gray-300 hover:text-gold-500 py-1">Home</a>
            <a href="#services" class="mobile-link text-gray-300 hover:text-gold-500 py-1">Services</a>
            <a href="#portfolio" class="mobile-link text-gray-300 hover:text-gold-500 py-1">Portfolio</a>
            <a href="#calculator" class="mobile-link text-gray-300 hover:text-gold-500 py-1">Cost Estimator</a>
            <a href="#about" class="mobile-link text-gray-300 hover:text-gold-500 py-1">About Us</a>
            <a href="#contact" class="mobile-link text-gray-300 hover:text-gold-500 py-1">Contact</a>
            <a href="https://wa.me/923237047546" target="_blank" class="gold-gradient-bg text-black text-center font-bold py-2 rounded-lg mt-2">
                <i class="fa-brands fa-whatsapp mr-2"></i> WhatsApp Inquiry
            </a>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="home" class="relative min-h-screen flex items-center pt-24 pb-16 overflow-hidden">
        <!-- Background Overlay Image with Architectural Vibe -->
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=2000&auto=format&fit=crop" 
                 alt="Architectural Modern Luxury House Elevation" 
                 class="w-full h-full object-cover opacity-20 filter brightness-75">
            <div class="absolute inset-0 bg-gradient-to-t from-navy-900 via-navy-900/80 to-transparent"></div>
            <div class="absolute inset-0 bg-gradient-to-r from-navy-900 via-navy-900/90 to-transparent"></div>
        </div>

        <div class="max-w-7xl mx-auto px-4 lg:px-12 relative z-10 grid md:grid-cols-12 gap-12 items-center">
            <div class="md:col-span-7 space-y-6">
                <!-- Badge -->
                <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full glass-card text-xs md:text-sm font-medium text-gold-400 border-gold-500/30">
                    <span class="w-2 h-2 rounded-full bg-gold-500 animate-ping"></span>
                    <span>Building Planning & 3D Architectural Visuals</span>
                </div>

                <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight font-serif text-white leading-tight">
                    We Build <span class="gold-gradient-text block mt-1">Your Dreams</span>
                </h1>

                <p class="text-gray-300 text-base md:text-lg max-w-2xl leading-relaxed">
                    Transforming your visions into architectural perfection. Specialized in high-precision <strong>2D Floor Planning</strong>, realistic <strong>3D Exterior Elevations</strong>, custom <strong>Interior Designing</strong>, and immersive <strong>Photorealistic 3D Renders</strong>.
                </p>

                <!-- Key Highlights List -->
                <div class="grid grid-cols-2 gap-4 py-2 text-sm text-gray-200">
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-circle-check text-gold-500"></i>
                        <span>2D Planning & Layouts</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-circle-check text-gold-500"></i>
                        <span>3D Exterior Elevation</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-circle-check text-gold-500"></i>
                        <span>Modern Interior Concepts</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-circle-check text-gold-500"></i>
                        <span>Realistic 3D Rendering</span>
                    </div>
                </div>

                <!-- CTA Buttons -->
                <div class="flex flex-wrap items-center gap-4 pt-4">
                    <a href="https://wa.me/923237047546?text=Hi%20Engr.%20Shahid,%20I%20want%20to%20discuss%20a%20new%20building%20plan/design." 
                       target="_blank"
                       class="gold-gradient-bg text-black font-bold px-8 py-4 rounded-xl hover:shadow-xl hover:shadow-gold-500/30 hover:-translate-y-0.5 transition-all text-center flex items-center justify-center gap-3">
                        <i class="fa-brands fa-whatsapp text-xl"></i>
                        <span>Discuss Your Project</span>
                    </a>
                    <a href="#portfolio" class="glass-card hover:bg-slate-800/80 text-white font-semibold px-8 py-4 rounded-xl transition-all text-center border border-slate-700 hover:border-gold-500/50">
                        View Portfolio
                    </a>
                </div>

                <!-- Contact Quick Pill -->
                <div class="pt-6 border-t border-slate-800/80 flex flex-wrap gap-6 text-xs text-gray-400">
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-user-tie text-gold-500"></i>
                        <span><strong>Owner:</strong> Shahid Rafique Janjua</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <i class="fa-solid fa-phone text-gold-500"></i>
                        <span>0323-7047546</span>
                    </div>
                </div>
            </div>

            <!-- Hero Feature Visual Card -->
            <div class="md:col-span-5">
                <div class="relative group">
                    <div class="absolute -inset-1 gold-gradient-bg rounded-2xl opacity-30 blur-lg group-hover:opacity-50 transition duration-500"></div>
                    <div class="relative glass-card rounded-2xl overflow-hidden p-3 border border-gold-500/30">
                        <img src="https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?q=80&w=1000&auto=format&fit=crop" 
                             alt="Modern House Elevation Exterior Render" 
                             class="w-full h-80 object-cover rounded-xl">
                        <div class="p-4 bg-navy-950/90 rounded-xl mt-3 border border-slate-800">
                            <div class="flex items-center justify-between mb-2">
                                <span class="text-xs font-semibold text-gold-400 tracking-wider uppercase">Featured Project Showcase</span>
                                <span class="text-xs text-emerald-400 bg-emerald-950/60 border border-emerald-800/50 px-2 py-0.5 rounded-full">3D Rendered</span>
                            </div>
                            <h3 class="text-lg font-bold text-white font-serif">Modern Luxury Villa Concept</h3>
                            <p class="text-xs text-gray-400 mt-1">Complete 2D Planning & 3D Exterior Visualization designed by Talha Associates.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- STATS COUNTER BAR -->
    <section class="py-10 bg-navy-950 border-y border-gold-500/20">
        <div class="max-w-7xl mx-auto px-4 lg:px-12 grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
            <div class="p-4">
                <div class="text-3xl lg:text-4xl font-extrabold gold-gradient-text font-serif">300+</div>
                <div class="text-xs md:text-sm text-gray-400 mt-1 font-medium">2D Blueprints Planned</div>
            </div>
            <div class="p-4">
                <div class="text-3xl lg:text-4xl font-extrabold gold-gradient-text font-serif">180+</div>
                <div class="text-xs md:text-sm text-gray-400 mt-1 font-medium">3D Exterior Renders</div>
            </div>
            <div class="p-4">
                <div class="text-3xl lg:text-4xl font-extrabold gold-gradient-text font-serif">150+</div>
                <div class="text-xs md:text-sm text-gray-400 mt-1 font-medium">Interior Designs Completed</div>
            </div>
            <div class="p-4">
                <div class="text-3xl lg:text-4xl font-extrabold gold-gradient-text font-serif">100%</div>
                <div class="text-xs md:text-sm text-gray-400 mt-1 font-medium">Client Satisfaction</div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section id="services" class="py-20 relative">
        <div class="max-w-7xl mx-auto px-4 lg:px-12">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="text-xs uppercase font-bold text-gold-500 tracking-widest mb-2">Our Specialized Expertise</h2>
                <h3 class="text-3xl md:text-5xl font-bold font-serif text-white">Comprehensive Architectural & Design Solutions</h3>
                <p class="text-gray-400 text-sm md:text-base mt-4">
                    From raw land measurements to photorealistic 3D interior walkthroughs, we deliver excellence at every step.
                </p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Service 1 -->
                <div class="glass-card p-8 rounded-2xl transition-all duration-300 relative group flex flex-col justify-between">
                    <div>
                        <div class="w-14 h-14 rounded-xl gold-gradient-bg flex items-center justify-center text-black text-2xl font-bold mb-6 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-drafting-compass"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3 font-serif">2D Building Planning</h4>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6">
                            Smart space optimization, structural floor layouts, municipal submission drawings, electric and plumbing mapping tailored to your lot size.
                        </p>
                    </div>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-slate-800 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Floor Layout Maps</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Working Drawings</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Submission Maps</li>
                    </ul>
                </div>

                <!-- Service 2 -->
                <div class="glass-card p-8 rounded-2xl transition-all duration-300 relative group flex flex-col justify-between">
                    <div>
                        <div class="w-14 h-14 rounded-xl gold-gradient-bg flex items-center justify-center text-black text-2xl font-bold mb-6 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-cubes"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3 font-serif">3D Exterior Visualization</h4>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6">
                            See your house front elevation before construction starts. Modern, Spanish, Classic, and Minimalist exterior 3D designs.
                        </p>
                    </div>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-slate-800 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Front Elevation 3D</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Material & Lighting Specs</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Day & Night Views</li>
                    </ul>
                </div>

                <!-- Service 3 -->
                <div class="glass-card p-8 rounded-2xl transition-all duration-300 relative group flex flex-col justify-between">
                    <div>
                        <div class="w-14 h-14 rounded-xl gold-gradient-bg flex items-center justify-center text-black text-2xl font-bold mb-6 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-couch"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3 font-serif">3D Interior Designing</h4>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6">
                            Luxury living rooms, customized TV wall panels, fluted paneling, warm ambient wall lights, modern kitchens, and cozy bedroom layouts.
                        </p>
                    </div>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-slate-800 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> TV Unit & Accent Walls</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> False Ceiling Layouts</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Furniture & Lighting Plan</li>
                    </ul>
                </div>

                <!-- Service 4 -->
                <div class="glass-card p-8 rounded-2xl transition-all duration-300 relative group flex flex-col justify-between">
                    <div>
                        <div class="w-14 h-14 rounded-xl gold-gradient-bg flex items-center justify-center text-black text-2xl font-bold mb-6 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-wand-magic-sparkles"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3 font-serif">Realistic Rendering</h4>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6">
                            Ultra high-definition photorealistic images and 3D architectural animation clips that showcase exact textures, marble finishes, and wood grains.
                        </p>
                    </div>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-slate-800 pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> 4K Ultra HD Renders</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Realistic Materials</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-angle-right text-gold-500"></i> Architectural Walkthrough</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- INTERACTIVE 2D VS 3D SLIDER SECTION -->
    <section class="py-20 bg-navy-950 border-y border-slate-800">
        <div class="max-w-7xl mx-auto px-4 lg:px-12">
            <div class="grid lg:grid-cols-12 gap-12 items-center">
                <div class="lg:col-span-5 space-y-6">
                    <span class="text-xs uppercase font-bold text-gold-500 tracking-widest">Interactive Transformation</span>
                    <h3 class="text-3xl md:text-4xl font-bold font-serif text-white">See 2D Blueprints Become Realistic 3D Dreams</h3>
                    <p class="text-gray-300 text-sm md:text-base leading-relaxed">
                        Drag the slider to compare our precision 2D planning layout with the final realistic 3D exterior visualization. We make sure you know exactly what your building will look like before laying a single brick!
                    </p>

                    <div class="space-y-4 pt-2">
                        <div class="flex items-start gap-4 glass-card p-4 rounded-xl">
                            <div class="w-10 h-10 rounded-lg gold-gradient-bg flex items-center justify-center text-black font-bold shrink-0">1</div>
                            <div>
                                <h4 class="text-white font-semibold text-sm">2D Floor Plan Precision</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Accurate room dimensions, ventilation placement, and door pathways.</p>
                            </div>
                        </div>
                        <div class="flex items-start gap-4 glass-card p-4 rounded-xl">
                            <div class="w-10 h-10 rounded-lg gold-gradient-bg flex items-center justify-center text-black font-bold shrink-0">2</div>
                            <div>
                                <h4 class="text-white font-semibold text-sm">3D Realistic Elevation</h4>
                                <p class="text-xs text-gray-400 mt-0.5">Lifelike materials, lighting reflections, glass windows, and exterior aesthetics.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Interactive Comparison Component -->
                <div class="lg:col-span-7">
                    <div class="glass-card p-3 rounded-2xl border border-gold-500/30">
                        <div class="img-comp-container rounded-xl shadow-2xl relative select-none">
                            <!-- Background (3D Elevation View) -->
                            <div class="img-comp-img">
                                <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=1200&auto=format&fit=crop" 
                                     alt="3D Exterior Elevation" 
                                     class="w-full h-full object-cover">
                                <span class="absolute bottom-4 right-4 bg-navy-950/90 text-gold-400 text-xs font-bold px-3 py-1.5 rounded-md border border-gold-500/30">
                                    3D Realistic Elevation
                                </span>
                            </div>
                            <!-- Overlay (2D Layout View) -->
                            <div class="img-comp-img img-comp-overlay" id="comp-overlay">
                                <img src="https://images.unsplash.com/photo-1600566753376-12c8ab7fb75b?q=80&w=1200&auto=format&fit=crop" 
                                     alt="2D Blueprint Floor Plan Layout" 
                                     class="w-full h-full object-cover filter grayscale contrast-125">
                                <span class="absolute bottom-4 left-4 bg-black/90 text-white text-xs font-bold px-3 py-1.5 rounded-md border border-slate-700">
                                    2D Blueprint Layout
                                </span>
                            </div>
                            <!-- Slider Handle -->
                            <div class="img-comp-slider" id="comp-slider">
                                <i class="fa-solid fa-arrows-left-right text-black font-extrabold text-sm"></i>
                            </div>
                        </div>
                        <p class="text-center text-xs text-gray-400 mt-3 font-medium">
                            <i class="fa-solid fa-hand-pointer text-gold-500 mr-1"></i> Drag the slider left or right to compare 2D Blueprint with 3D Rendering
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PORTFOLIO GALLERY SECTION -->
    <section id="portfolio" class="py-20">
        <div class="max-w-7xl mx-auto px-4 lg:px-12">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <span class="text-xs uppercase font-bold text-gold-500 tracking-widest">Our Work Portfolio</span>
                <h2 class="text-3xl md:text-5xl font-bold font-serif text-white mt-2">Explore Recent Projects</h2>
                <p class="text-gray-400 text-sm md:text-base mt-3">
                    A showcase of our recent 2D blueprints, modern 3D exterior elevations, and cozy interior wall decor designs.
                </p>

                <!-- Category Filters -->
                <div class="flex flex-wrap justify-center gap-3 mt-8" id="portfolio-filters">
                    <button data-filter="all" class="filter-btn active gold-gradient-bg text-black font-semibold text-xs md:text-sm px-5 py-2 rounded-full transition-all">All Projects</button>
                    <button data-filter="exterior" class="filter-btn glass-card hover:border-gold-500 text-gray-300 font-semibold text-xs md:text-sm px-5 py-2 rounded-full transition-all">3D Exterior</button>
                    <button data-filter="interior" class="filter-btn glass-card hover:border-gold-500 text-gray-300 font-semibold text-xs md:text-sm px-5 py-2 rounded-full transition-all">3D Interior</button>
                    <button data-filter="2d" class="filter-btn glass-card hover:border-gold-500 text-gray-300 font-semibold text-xs md:text-sm px-5 py-2 rounded-full transition-all">2D Planning</button>
                </div>
            </div>

            <!-- Portfolio Grid -->
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8" id="portfolio-grid">
                
                <!-- Project Item 1 (Exterior Dark Modern) -->
                <div class="portfolio-item exterior glass-card rounded-2xl overflow-hidden group border border-slate-800 transition-all duration-300">
                    <div class="relative overflow-hidden h-72">
                        <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=800&auto=format&fit=crop" 
                             alt="Modern Dark Exterior Elevation" 
                             class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-950 via-transparent to-transparent opacity-90"></div>
                        <div class="absolute top-4 left-4">
                            <span class="text-xs font-bold bg-gold-500 text-black px-3 py-1 rounded-full">3D Exterior</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white font-serif mb-2">Modern Dark Matte Elevation</h3>
                        <p class="text-gray-400 text-xs mb-4">Kamoke Residential Villa • Striking LED Strip Lighting & Large Glass Panel Façade.</p>
                        <button onclick="openModal('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=1200&auto=format&fit=crop', 'Modern Dark Matte Elevation', 'Complete 3D Exterior Elevation project featuring dark paneling, warm concealed LED lights, glass windows, and architectural framing.')" 
                                class="text-xs font-semibold text-gold-400 hover:text-gold-300 flex items-center gap-2">
                            <span>View HD Render</span> <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

                <!-- Project Item 2 (Classic Luxury Beige Villa Exterior) -->
                <div class="portfolio-item exterior glass-card rounded-2xl overflow-hidden group border border-slate-800 transition-all duration-300">
                    <div class="relative overflow-hidden h-72">
                        <img src="https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?q=80&w=800&auto=format&fit=crop" 
                             alt="Classic Luxury Beige Villa Elevation" 
                             class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-950 via-transparent to-transparent opacity-90"></div>
                        <div class="absolute top-4 left-4">
                            <span class="text-xs font-bold bg-gold-500 text-black px-3 py-1 rounded-full">3D Exterior</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white font-serif mb-2">Classic Arch Windows Villa</h3>
                        <p class="text-gray-400 text-xs mb-4">Gujranwala Client • Double Height Arch Window with Spanish Roof Tile Details.</p>
                        <button onclick="openModal('https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?q=80&w=1200&auto=format&fit=crop', 'Classic Arch Windows Villa', 'Elegant beige theme elevation with grand double-height arched window, warm sconce wall lights, and classical balcony railing.')" 
                                class="text-xs font-semibold text-gold-400 hover:text-gold-300 flex items-center gap-2">
                            <span>View HD Render</span> <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

                <!-- Project Item 3 (Interior TV Wall Unit) -->
                <div class="portfolio-item interior glass-card rounded-2xl overflow-hidden group border border-slate-800 transition-all duration-300">
                    <div class="relative overflow-hidden h-72">
                        <img src="https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?q=80&w=800&auto=format&fit=crop" 
                             alt="Luxury TV Wall Unit Interior Design" 
                             class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-950 via-transparent to-transparent opacity-90"></div>
                        <div class="absolute top-4 left-4">
                            <span class="text-xs font-bold bg-gold-500 text-black px-3 py-1 rounded-full">3D Interior</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white font-serif mb-2">Minimalist Marble & Wood TV Wall</h3>
                        <p class="text-gray-400 text-xs mb-4">Living Room • Fluted Wood Paneling, Floating Console & Warm Ambient Lighting.</p>
                        <button onclick="openModal('https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?q=80&w=1200&auto=format&fit=crop', 'Minimalist Marble & Wood TV Wall', 'Custom TV console interior design showcasing marble texture backing, fluted wooden vertical slats, low profile console, and warm pendant light.')" 
                                class="text-xs font-semibold text-gold-400 hover:text-gold-300 flex items-center gap-2">
                            <span>View HD Render</span> <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

                <!-- Project Item 4 (Interior Window Nook / Seating) -->
                <div class="portfolio-item interior glass-card rounded-2xl overflow-hidden group border border-slate-800 transition-all duration-300">
                    <div class="relative overflow-hidden h-72">
                        <img src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?q=80&w=800&auto=format&fit=crop" 
                             alt="Cozy Window Arch Seat Interior" 
                             class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-950 via-transparent to-transparent opacity-90"></div>
                        <div class="absolute top-4 left-4">
                            <span class="text-xs font-bold bg-gold-500 text-black px-3 py-1 rounded-full">3D Interior</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white font-serif mb-2">Luxury Cozy Window Arch Seat</h3>
                        <p class="text-gray-400 text-xs mb-4">Master Bedroom Interior • Curved Wooden Archway, Custom Fluted Walls & Soft Lighting.</p>
                        <button onclick="openModal('https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?q=80&w=1200&auto=format&fit=crop', 'Luxury Cozy Window Arch Seat', 'Serene bedroom alcove design featuring wooden arch framing, fluted wall panels, warm double wall sconces, and custom cushioned bench.')" 
                                class="text-xs font-semibold text-gold-400 hover:text-gold-300 flex items-center gap-2">
                            <span>View HD Render</span> <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

                <!-- Project Item 5 (Modern Wall Decorative Art Shelf) -->
                <div class="portfolio-item interior glass-card rounded-2xl overflow-hidden group border border-slate-800 transition-all duration-300">
                    <div class="relative overflow-hidden h-72">
                        <img src="https://images.unsplash.com/photo-1513694203232-719a280e022f?q=80&w=800&auto=format&fit=crop" 
                             alt="Modern Decorative Shelf Accent Wall" 
                             class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-950 via-transparent to-transparent opacity-90"></div>
                        <div class="absolute top-4 left-4">
                            <span class="text-xs font-bold bg-gold-500 text-black px-3 py-1 rounded-full">3D Interior</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white font-serif mb-2">Oval Backlit Wall Decor Shelf</h3>
                        <p class="text-gray-400 text-xs mb-4">Foyer Accent Wall • Elliptical Backlit Panel, Fluted Backing & Minimalist Vases.</p>
                        <button onclick="openModal('https://images.unsplash.com/photo-1513694203232-719a280e022f?q=80&w=1200&auto=format&fit=crop', 'Oval Backlit Wall Decor Shelf', 'Contemporary hallway feature wall concept with soft halo illumination, modern vertical groove texture, and decorative vase shelf.')" 
                                class="text-xs font-semibold text-gold-400 hover:text-gold-300 flex items-center gap-2">
                            <span>View HD Render</span> <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

                <!-- Project Item 6 (2D Architectural Plan Blueprint) -->
                <div class="portfolio-item 2d glass-card rounded-2xl overflow-hidden group border border-slate-800 transition-all duration-300">
                    <div class="relative overflow-hidden h-72 bg-slate-900 flex items-center justify-center p-4">
                        <img src="https://images.unsplash.com/photo-1600566753376-12c8ab7fb75b?q=80&w=800&auto=format&fit=crop" 
                             alt="2D Architectural Blueprint Plan Layout" 
                             class="w-full h-full object-cover filter contrast-125 group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-950 via-transparent to-transparent opacity-90"></div>
                        <div class="absolute top-4 left-4">
                            <span class="text-xs font-bold bg-blue-500 text-white px-3 py-1 rounded-full">2D Layout Map</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white font-serif mb-2">5 Marla / 10 Marla House Layout</h3>
                        <p class="text-gray-400 text-xs mb-4">Kamoke Residential • Optimized Floor Plan with Ventilation & Parking space.</p>
                        <button onclick="openModal('https://images.unsplash.com/photo-1600566753376-12c8ab7fb75b?q=80&w=1200&auto=format&fit=crop', '2D Precision Floor Blueprint', 'Comprehensive 2D layout planning including room dimensions, staircase placement, natural light ventilation ducts, and submission standards.')" 
                                class="text-xs font-semibold text-gold-400 hover:text-gold-300 flex items-center gap-2">
                            <span>View HD Blueprint</span> <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- INTERACTIVE PROJECT COST ESTIMATOR CALCULATOR -->
    <section id="calculator" class="py-20 bg-navy-950 border-y border-slate-800">
        <div class="max-w-7xl mx-auto px-4 lg:px-12">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <span class="text-xs uppercase font-bold text-gold-500 tracking-widest">Instant Estimate</span>
                <h2 class="text-3xl md:text-5xl font-bold font-serif text-white mt-2">Project Fee Estimator</h2>
                <p class="text-gray-400 text-sm md:text-base mt-3">
                    Calculate an approximate cost for your 2D planning or 3D architectural rendering service instantly.
                </p>
            </div>

            <div class="max-w-4xl mx-auto glass-card p-6 md:p-10 rounded-2xl border border-gold-500/30">
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <!-- Calculator Inputs -->
                    <div class="space-y-6">
                        <!-- Plot Area Input -->
                        <div>
                            <label class="block text-xs font-semibold uppercase text-gold-400 mb-2">1. Select Plot Size Unit & Area</label>
                            <div class="grid grid-cols-3 gap-2 mb-3">
                                <button type="button" onclick="setUnit('marla')" id="btn-marla" class="unit-btn active gold-gradient-bg text-black font-bold text-xs py-2 rounded-lg">Marla</button>
                                <button type="button" onclick="setUnit('sqft')" id="btn-sqft" class="unit-btn bg-slate-800 text-gray-300 font-bold text-xs py-2 rounded-lg">Sq Ft</button>
                                <button type="button" onclick="setUnit('kanal')" id="btn-kanal" class="unit-btn bg-slate-800 text-gray-300 font-bold text-xs py-2 rounded-lg">Kanal</button>
                            </div>
                            <input type="number" id="plot-size-input" value="5" min="1" max="100000" oninput="calculateEstimate()" 
                                   class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-gold-500 font-bold">
                        </div>

                        <!-- Service Package Selection -->
                        <div>
                            <label class="block text-xs font-semibold uppercase text-gold-400 mb-2">2. Required Design Services</label>
                            <select id="service-package" onchange="calculateEstimate()" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-gold-500 font-medium text-sm">
                                <option value="2d_only">2D Floor Planning & Blueprints Only</option>
                                <option value="3d_ext" selected>2D Floor Plan + 3D Exterior Front Elevation</option>
                                <option value="3d_int">2D Plan + 3D Interior Design Package</option>
                                <option value="full_pkg">Complete Architectural Package (2D + 3D Ext + 3D Interior)</option>
                            </select>
                        </div>

                        <!-- Floor Count -->
                        <div>
                            <label class="block text-xs font-semibold uppercase text-gold-400 mb-2">3. Number of Floors</label>
                            <div class="flex items-center gap-4">
                                <label class="flex items-center gap-2 cursor-pointer text-sm">
                                    <input type="radio" name="floors" value="1" onchange="calculateEstimate()" class="accent-gold-500"> Ground Floor Only
                                </label>
                                <label class="flex items-center gap-2 cursor-pointer text-sm">
                                    <input type="radio" name="floors" value="2" checked onchange="calculateEstimate()" class="accent-gold-500"> Double Story (G+1)
                                </label>
                                <label class="flex items-center gap-2 cursor-pointer text-sm">
                                    <input type="radio" name="floors" value="3" onchange="calculateEstimate()" class="accent-gold-500"> Triple Story
                                </label>
                            </div>
                        </div>
                    </div>

                    <!-- Calculator Output Card -->
                    <div class="bg-navy-950 p-6 rounded-2xl border border-gold-500/40 text-center space-y-6">
                        <span class="text-xs font-bold uppercase text-gray-400 tracking-wider">Estimated Service Cost</span>
                        <div class="py-2">
                            <div class="text-3xl md:text-5xl font-extrabold gold-gradient-text font-serif" id="estimated-cost-display">PKR 15,000 - 25,000</div>
                            <p class="text-xs text-gray-400 mt-2" id="estimate-breakdown-text">Based on 5 Marla Double Story 2D + 3D Front Elevation design.</p>
                        </div>
                        <div class="space-y-3 pt-2">
                            <a id="calc-whatsapp-btn" href="#" target="_blank" class="w-full gold-gradient-bg text-black font-bold py-3.5 px-4 rounded-xl flex items-center justify-center gap-2 hover:shadow-lg transition-all text-sm">
                                <i class="fa-brands fa-whatsapp text-lg"></i>
                                <span>Get Official Quote on WhatsApp</span>
                            </a>
                            <p class="text-[11px] text-gray-400">
                                *Note: Estimates are indicative. Final prices depend on specific client customizations and complex structural details.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT US SECTION -->
    <section id="about" class="py-20 relative">
        <div class="max-w-7xl mx-auto px-4 lg:px-12">
            <div class="grid lg:grid-cols-12 gap-12 items-center">
                
                <!-- Founder Photo / Graphic -->
                <div class="lg:col-span-5">
                    <div class="relative">
                        <div class="absolute -inset-1 gold-gradient-bg rounded-3xl opacity-30 blur-md"></div>
                        <div class="relative glass-card p-4 rounded-3xl border border-gold-500/30">
                            <img src="https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?q=80&w=900&auto=format&fit=crop" 
                                 alt="Talha Associates Office Work" 
                                 class="w-full h-80 object-cover rounded-2xl">
                            
                            <div class="mt-4 p-4 bg-navy-950 rounded-xl border border-slate-800">
                                <div class="flex items-center gap-4">
                                    <div class="w-12 h-12 rounded-full gold-gradient-bg text-black flex items-center justify-center font-bold text-xl">
                                        <i class="fa-solid fa-user-check"></i>
                                    </div>
                                    <div>
                                        <h4 class="text-lg font-bold text-white font-serif">Shahid Rafique Janjua</h4>
                                        <p class="text-xs text-gold-400 font-semibold">Owner & Principal Architect / Planner</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- About Text -->
                <div class="lg:col-span-7 space-y-6">
                    <span class="text-xs uppercase font-bold text-gold-500 tracking-widest">About Talha Associates</span>
                    <h2 class="text-3xl md:text-5xl font-bold font-serif text-white leading-tight">
                        Crafting Architectural Excellence in Kamoke & Gujranwala
                    </h2>
                    <p class="text-gray-300 text-sm md:text-base leading-relaxed">
                        At <strong>Talha Associates</strong>, we believe every home and commercial structure tells a story. Led by <strong>Engr. Shahid Rafique Janjua</strong>, our design office specializes in functional 2D space planning and jaw-dropping 3D architectural rendering.
                    </p>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Whether you are constructing a 3 Marla cozy home or a grand 2 Kanal luxury residence, we provide end-to-end guidance from preliminary floor planning to final interior decoration details.
                    </p>

                    <!-- Feature Pillars -->
                    <div class="grid grid-cols-2 gap-4 pt-2">
                        <div class="p-4 rounded-xl bg-navy-950 border border-slate-800">
                            <i class="fa-solid fa-compass-drafting text-gold-500 text-2xl mb-2"></i>
                            <h4 class="text-white font-bold text-sm">Smart Space Utilization</h4>
                            <p class="text-xs text-gray-400 mt-1">Zero wasted square footage with optimum natural light.</p>
                        </div>
                        <div class="p-4 rounded-xl bg-navy-950 border border-slate-800">
                            <i class="fa-solid fa-eye text-gold-500 text-2xl mb-2"></i>
                            <h4 class="text-white font-bold text-sm">3D Photorealism</h4>
                            <p class="text-xs text-gray-400 mt-1">High-definition renders before construction spend.</p>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="py-20 bg-navy-950 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 lg:px-12">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-xs uppercase font-bold text-gold-500 tracking-widest">Get In Touch</span>
                <h2 class="text-3xl md:text-5xl font-bold font-serif text-white mt-2">Visit Our Office Or Message Us</h2>
                <p class="text-gray-400 text-sm md:text-base mt-3">
                    We are ready to bring your building ideas to life. Reach out via WhatsApp or visit us at our Kamoke office.
                </p>
            </div>

            <div class="grid lg:grid-cols-12 gap-12">
                <!-- Contact Info Cards -->
                <div class="lg:col-span-5 space-y-6">
                    
                    <!-- Card 1: Phone -->
                    <div class="glass-card p-6 rounded-2xl border border-slate-800 flex items-start gap-5">
                        <div class="w-12 h-12 rounded-xl gold-gradient-bg text-black flex items-center justify-center text-xl font-bold shrink-0">
                            <i class="fa-solid fa-phone"></i>
                        </div>
                        <div>
                            <span class="text-xs text-gold-400 font-semibold uppercase">Call or WhatsApp</span>
                            <a href="tel:03237047546" class="block text-xl font-bold text-white hover:text-gold-400 mt-0.5">0323-7047546</a>
                            <p class="text-xs text-gray-400 mt-1">+92 323 7047546 (Shahid Rafique Janjua)</p>
                        </div>
                    </div>

                    <!-- Card 2: Email -->
                    <div class="glass-card p-6 rounded-2xl border border-slate-800 flex items-start gap-5">
                        <div class="w-12 h-12 rounded-xl gold-gradient-bg text-black flex items-center justify-center text-xl font-bold shrink-0">
                            <i class="fa-solid fa-envelope"></i>
                        </div>
                        <div>
                            <span class="text-xs text-gold-400 font-semibold uppercase">Email Address</span>
                            <a href="mailto:Engr.shahidjanjua123@gmail.com" class="block text-base font-bold text-white hover:text-gold-400 mt-0.5 break-all">
                                Engr.shahidjanjua123@gmail.com
                            </a>
                            <p class="text-xs text-gray-400 mt-1">Direct architect mailbox</p>
                        </div>
                    </div>

                    <!-- Card 3: Office Address -->
                    <div class="glass-card p-6 rounded-2xl border border-slate-800 flex items-start gap-5">
                        <div class="w-12 h-12 rounded-xl gold-gradient-bg text-black flex items-center justify-center text-xl font-bold shrink-0">
                            <i class="fa-solid fa-location-dot"></i>
                        </div>
                        <div>
                            <span class="text-xs text-gold-400 font-semibold uppercase">Office Location</span>
                            <h4 class="text-base font-bold text-white mt-0.5 leading-snug">
                                Qila Didar Singh Road, Opposite SDPO Office, Kamoke
                            </h4>
                            <p class="text-xs text-gray-400 mt-1">District Gujranwala, Punjab, Pakistan</p>
                        </div>
                    </div>

                </div>

                <!-- Direct WhatsApp Message Form -->
                <div class="lg:col-span-7">
                    <div class="glass-card p-8 rounded-2xl border border-gold-500/30">
                        <h3 class="text-2xl font-bold text-white font-serif mb-2">Send Us a Direct Message</h3>
                        <p class="text-xs text-gray-400 mb-6">Fill in your requirements to generate an instant WhatsApp message link to Engr. Shahid Janjua.</p>

                        <form id="quick-contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                            <div class="grid md:grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-xs font-medium text-gray-300 mb-1">Your Full Name</label>
                                    <input type="text" id="contact-name" required placeholder="e.g. Muhammad Ali" 
                                           class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white text-sm focus:outline-none focus:border-gold-500">
                                </div>
                                <div>
                                    <label class="block text-xs font-medium text-gray-300 mb-1">Phone Number</label>
                                    <input type="tel" id="contact-phone" required placeholder="0300-1234567" 
                                           class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white text-sm focus:outline-none focus:border-gold-500">
                                </div>
                            </div>

                            <div class="grid md:grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-xs font-medium text-gray-300 mb-1">Plot Location / City</label>
                                    <input type="text" id="contact-location" placeholder="e.g. Kamoke / Gujranwala" 
                                           class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white text-sm focus:outline-none focus:border-gold-500">
                                </div>
                                <div>
                                    <label class="block text-xs font-medium text-gray-300 mb-1">Service Interest</label>
                                    <select id="contact-service" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white text-sm focus:outline-none focus:border-gold-500">
                                        <option value="2D Planning">2D Building Planning</option>
                                        <option value="3D Front Elevation">3D Front Elevation</option>
                                        <option value="3D Interior Design">3D Interior Design</option>
                                        <option value="Full Project Package">Complete Package</option>
                                    </select>
                                </div>
                            </div>

                            <div>
                                <label class="block text-xs font-medium text-gray-300 mb-1">Project Details / Message</label>
                                <textarea id="contact-msg" rows="4" placeholder="Tell us about plot size (e.g. 5 Marla, 10 Marla), number of floors, or design ideas..." 
                                          class="w-full bg-slate-900 border border-slate-700 rounded-xl px-4 py-3 text-white text-sm focus:outline-none focus:border-gold-500"></textarea>
                            </div>

                            <button type="submit" class="w-full gold-gradient-bg text-black font-bold py-4 rounded-xl flex items-center justify-center gap-2 hover:shadow-xl hover:shadow-gold-500/20 transition-all text-base">
                                <i class="fa-brands fa-whatsapp text-xl"></i>
                                <span>Send Inquiry via WhatsApp</span>
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-navy-950 border-t border-slate-900 py-12">
        <div class="max-w-7xl mx-auto px-4 lg:px-12 flex flex-col md:flex-row items-center justify-between gap-6">
            
            <div class="flex items-center gap-3">
                <div class="w-8 h-8 rounded-lg gold-gradient-bg flex items-center justify-center text-black font-bold">
                    <i class="fa-solid fa-building text-sm"></i>
                </div>
                <div>
                    <span class="text-base font-bold tracking-wider font-serif text-white block leading-none">TALHA ASSOCIATES</span>
                    <span class="text-[10px] text-gold-500 tracking-widest font-semibold">WE BUILD YOUR DREAMS</span>
                </div>
            </div>

            <p class="text-xs text-gray-500 text-center">
                &copy; <span id="year"></span> Talha Associates. All rights reserved. | Owner: Engr. Shahid Rafique Janjua
            </p>

            <div class="flex items-center space-x-4">
                <a href="https://wa.me/923237047546" target="_blank" class="w-9 h-9 rounded-full glass-card flex items-center justify-center text-gold-400 hover:text-white hover:border-gold-500 transition-colors">
                    <i class="fa-brands fa-whatsapp"></i>
                </a>
                <a href="tel:03237047546" class="w-9 h-9 rounded-full glass-card flex items-center justify-center text-gold-400 hover:text-white hover:border-gold-500 transition-colors">
                    <i class="fa-solid fa-phone"></i>
                </a>
                <a href="mailto:Engr.shahidjanjua123@gmail.com" class="w-9 h-9 rounded-full glass-card flex items-center justify-center text-gold-400 hover:text-white hover:border-gold-500 transition-colors">
                    <i class="fa-solid fa-envelope"></i>
                </a>
            </div>

        </div>
    </footer>

    <!-- FLOATING WHATSAPP BUTTON -->
    <a href="https://wa.me/923237047546?text=Hello%20Talha%20Associates!%20I%20would%20like%20to%20get%20more%20details%20about%20your%20design%20services." 
       target="_blank" 
       title="Direct WhatsApp Chat"
       class="fixed bottom-6 right-6 z-50 w-14 h-14 bg-emerald-500 text-white rounded-full flex items-center justify-center text-3xl shadow-2xl hover:scale-110 transition-transform animate-bounce">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <!-- LIGHTBOX IMAGE MODAL -->
    <div id="image-modal" class="fixed inset-0 z-50 bg-black/90 backdrop-blur-md hidden flex items-center justify-center p-4">
        <div class="relative max-w-4xl w-full glass-card p-4 rounded-2xl border border-gold-500/40">
            <button onclick="closeModal()" class="absolute -top-4 -right-4 w-10 h-10 rounded-full bg-gold-500 text-black font-extrabold flex items-center justify-center hover:scale-110 transition-transform z-10">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            
            <img id="modal-img" src="" alt="Project Preview" class="w-full max-h-[70vh] object-contain rounded-xl">
            
            <div class="mt-4 p-4 bg-navy-950 rounded-xl border border-slate-800">
                <h3 id="modal-title" class="text-xl font-bold font-serif text-white">Project Title</h3>
                <p id="modal-desc" class="text-xs text-gray-300 mt-1">Project Description...</p>
                <div class="mt-4 flex justify-end">
                    <a href="https://wa.me/923237047546" target="_blank" class="gold-gradient-bg text-black font-bold text-xs px-5 py-2.5 rounded-lg flex items-center gap-2">
                        <i class="fa-brands fa-whatsapp text-sm"></i>
                        <span>Order Design Like This</span>
                    </a>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Set dynamic copyright year
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Navigation Menu Toggle
        const menuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('.mobile-link').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Portfolio Filter Tabs Logic
        const filterBtns = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                filterBtns.forEach(b => {
                    b.classList.remove('gold-gradient-bg', 'text-black', 'active');
                    b.classList.add('glass-card', 'text-gray-300');
                });

                btn.classList.add('gold-gradient-bg', 'text-black', 'active');
                btn.classList.remove('glass-card', 'text-gray-300');

                const filter = btn.getAttribute('data-filter');

                portfolioItems.forEach(item => {
                    if (filter === 'all' || item.classList.contains(filter)) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });

        // Modal Logic
        function openModal(imgSrc, title, desc) {
            document.getElementById('modal-img').src = imgSrc;
            document.getElementById('modal-title').textContent = title;
            document.getElementById('modal-desc').textContent = desc;
            document.getElementById('image-modal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('image-modal').classList.add('hidden');
        }

        // Close Modal on ESC key
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') closeModal();
        });

        // Interactive 2D vs 3D Comparison Slider Logic
        const slider = document.getElementById('comp-slider');
        const overlay = document.getElementById('comp-overlay');
        const container = document.querySelector('.img-comp-container');
        let isDragging = false;

        function slideMove(x) {
            const rect = container.getBoundingClientRect();
            let pos = x - rect.left;
            if (pos < 0) pos = 0;
            if (pos > rect.width) pos = rect.width;
            
            const pct = (pos / rect.width) * 100;
            overlay.style.width = pct + "%";
            slider.style.left = pct + "%";
        }

        slider.addEventListener('mousedown', () => isDragging = true);
        window.addEventListener('mouseup', () => isDragging = false);
        window.addEventListener('mousemove', (e) => {
            if (!isDragging) return;
            slideMove(e.clientX);
        });

        // Touch support for mobile comparison slider
        slider.addEventListener('touchstart', () => isDragging = true);
        window.addEventListener('touchend', () => isDragging = false);
        window.addEventListener('touchmove', (e) => {
            if (!isDragging) return;
            slideMove(e.touches[0].clientX);
        });

        // Cost Estimator Calculator State
        let currentUnit = 'marla';

        function setUnit(unit) {
            currentUnit = unit;
            document.querySelectorAll('.unit-btn').forEach(btn => {
                btn.classList.remove('gold-gradient-bg', 'text-black');
                btn.classList.add('bg-slate-800', 'text-gray-300');
            });

            const activeBtn = document.getElementById(`btn-${unit}`);
            activeBtn.classList.add('gold-gradient-bg', 'text-black');
            activeBtn.classList.remove('bg-slate-800', 'text-gray-300');

            const input = document.getElementById('plot-size-input');
            if (unit === 'marla') input.value = 5;
            else if (unit === 'sqft') input.value = 1125;
            else if (unit === 'kanal') input.value = 1;

            calculateEstimate();
        }

        function calculateEstimate() {
            const sizeVal = parseFloat(document.getElementById('plot-size-input').value) || 0;
            const pkg = document.getElementById('service-package').value;
            const floors = parseInt(document.querySelector('input[name="floors"]:checked').value);

            let marlas = sizeVal;
            if (currentUnit === 'sqft') marlas = sizeVal / 225;
            if (currentUnit === 'kanal') marlas = sizeVal * 20;

            let rateMin = 3000;
            let rateMax = 5000;

            if (pkg === '2d_only') {
                rateMin = 1500;
                rateMax = 2500;
            } else if (pkg === '3d_ext') {
                rateMin = 3000;
                rateMax = 4500;
            } else if (pkg === '3d_int') {
                rateMin = 4000;
                rateMax = 6500;
            } else if (pkg === 'full_pkg') {
                rateMin = 6000;
                rateMax = 9500;
            }

            const multiplier = 1 + (floors - 1) * 0.4;
            let totalMin = Math.round(marlas * rateMin * multiplier);
            let totalMax = Math.round(marlas * rateMax * multiplier);

            // Minimum baseline fee check
            if (totalMin < 8000) totalMin = 8000;
            if (totalMax < 12000) totalMax = 12000;

            const formatPKR = (num) => "PKR " + num.toLocaleString();
            document.getElementById('estimated-cost-display').textContent = `${formatPKR(totalMin)} - ${formatPKR(totalMax)}`;

            const breakdown = `Estimate for ${sizeVal} ${currentUnit.toUpperCase()} (${floors} floor${floors > 1 ? 's' : ''}).`;
            document.getElementById('estimate-breakdown-text').textContent = breakdown;

            // Update direct WhatsApp link
            const waMsg = encodeURIComponent(`Hi Engr. Shahid Janjua, I calculated an estimate on your website for a ${sizeVal} ${currentUnit} plot (${floors} floor/s) with package: ${pkg}. Estimated quote: ${formatPKR(totalMin)} - ${formatPKR(totalMax)}. Please contact me.`);
            document.getElementById('calc-whatsapp-btn').href = `https://wa.me/923237047546?text=${waMsg}`;
        }

        // Quick Contact Form Handler
        function handleFormSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('contact-name').value;
            const phone = document.getElementById('contact-phone').value;
            const loc = document.getElementById('contact-location').value;
            const service = document.getElementById('contact-service').value;
            const msg = document.getElementById('contact-msg').value;

            const fullMsg = `Hello Engr. Shahid Janjua (Talha Associates),\n\nName: ${name}\nPhone: ${phone}\nLocation: ${loc}\nService Needed: ${service}\nMessage/Details: ${msg}`;
            
            window.open(`https://wa.me/923237047546?text=${encodeURIComponent(fullMsg)}`, '_blank');
        }

        // Initialize default calculator value
        calculateEstimate();
    </script>
</body>
</html>
