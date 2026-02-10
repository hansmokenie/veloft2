<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Veloft — Future-Proofing Your Digital Presence</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Space Grotesk', 'sans-serif'],
                    },
                    colors: {
                        veloft: {
                            dark: '#0a0a0b',
                            card: '#141416',
                            accent: '#3b82f6',
                            glow: '#60a5fa',
                        }
                    },
                    animation: {
                        'fade-up': 'fadeUp 0.8s ease-out forwards',
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    },
                    keyframes: {
                        fadeUp: {
                            '0%': { opacity: '0', transform: 'translateY(30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        }
                    }
                }
            }
        }
    </script>
    
    <style>
        body {
            background-color: #0a0a0b;
            color: #fafafa;
            overflow-x: hidden;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #fff 0%, #94a3b8 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .hero-gradient {
            background: radial-gradient(ellipse at center, rgba(59, 130, 246, 0.15) 0%, transparent 70%);
        }
        
        .noise {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 50;
            opacity: 0.03;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
        }
        
        .scroll-reveal {
            opacity: 0;
            transform: translateY(24px);
            transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }
        
        .scroll-reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
        
        .feature-card {
            background: linear-gradient(145deg, rgba(20, 20, 22, 0.8) 0%, rgba(10, 10, 11, 0.9) 100%);
            border: 1px solid rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
        }
        
        .glow-border {
            position: relative;
        }
        
        .glow-border::before {
            content: '';
            position: absolute;
            inset: -1px;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.5), transparent, rgba(59, 130, 246, 0.3));
            border-radius: inherit;
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .glow-border:hover::before {
            opacity: 1;
        }
        
        .parallax-layer {
            will-change: transform;
        }
        
        .nav-blur {
            backdrop-filter: blur(20px);
            background: rgba(10, 10, 11, 0.8);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .price-highlight {
            background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            box-shadow: 0 0 40px rgba(59, 130, 246, 0.3);
        }
    </style>
</head>
<body class="antialiased selection:bg-blue-500 selection:text-white">

    <!-- Noise Overlay -->
    <div class="noise"></div>

    <!-- Navigation -->
    <nav class="fixed top-0 left-0 right-0 z-40 nav-blur transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <!-- Logo Placeholder -->
                <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-blue-700 rounded-lg flex items-center justify-center font-display font-bold text-xl">
                    V
                </div>
                <span class="font-display font-semibold text-xl tracking-tight">Veloft</span>
            </div>
            
            <div class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-400">
                <a href="#problem" class="hover:text-white transition-colors">The Problem</a>
                <a href="#solution" class="hover:text-white transition-colors">Solution</a>
                <a href="#process" class="hover:text-white transition-colors">Process</a>
                <a href="#pricing" class="hover:text-white transition-colors">Pricing</a>
            </div>
            
            <button onclick="scrollToContact()" class="px-6 py-2.5 bg-white text-black font-medium rounded-full hover:bg-gray-200 transition-all transform hover:scale-105 text-sm">
                Get Started
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden pt-20">
        <!-- Background Elements -->
        <div class="absolute inset-0 hero-gradient"></div>
        <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-blue-500/20 rounded-full blur-[128px] animate-pulse-slow"></div>
        <div class="absolute bottom-1/4 right-1/4 w-64 h-64 bg-purple-500/10 rounded-full blur-[96px]"></div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-6 text-center">
            <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full border border-white/10 bg-white/5 mb-8 animate-fade-up" style="animation-delay: 0.1s">
                <span class="w-2 h-2 bg-green-400 rounded-full animate-pulse"></span>
                <span class="text-sm text-gray-300">Available for new projects</span>
            </div>
            
            <h1 class="font-display text-5xl md:text-7xl lg:text-8xl font-medium leading-tight mb-6 animate-fade-up" style="animation-delay: 0.2s">
                <span class="gradient-text">Future-Proofing</span><br>
                <span class="text-white">Your Digital Presence</span>
            </h1>
            
            <p class="text-xl md:text-2xl text-gray-400 max-w-2xl mx-auto mb-12 font-light animate-fade-up" style="animation-delay: 0.3s">
                Premium websites built in <span class="text-white font-medium">7 days or less</span>. 
                No outdated designs. No technical headaches. Just results.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center animate-fade-up" style="animation-delay: 0.4s">
                <button onclick="scrollToContact()" class="group px-8 py-4 bg-blue-600 hover:bg-blue-700 text-white rounded-full font-medium transition-all flex items-center gap-2">
                    Start Your Project
                    <i data-lucide="arrow-right" class="w-4 h-4 group-hover:translate-x-1 transition-transform"></i>
                </button>
                <button onclick="document.getElementById('problem').scrollIntoView({behavior: 'smooth'})" class="px-8 py-4 border border-white/20 hover:border-white/40 text-white rounded-full font-medium transition-all">
                    Learn More
                </button>
            </div>
            
            <!-- Stats -->
            <div class="grid grid-cols-3 gap-8 max-w-2xl mx-auto mt-20 pt-10 border-t border-white/10 animate-fade-up" style="animation-delay: 0.5s">
                <div>
                    <div class="text-3xl font-display font-semibold text-white">7 Days</div>
                    <div class="text-sm text-gray-500 mt-1">Delivery Time</div>
                </div>
                <div>
                    <div class="text-3xl font-display font-semibold text-white">$500</div>
                    <div class="text-sm text-gray-500 mt-1">Starting Price</div>
                </div>
                <div>
                    <div class="text-3xl font-display font-semibold text-white">100%</div>
                    <div class="text-sm text-gray-500 mt-1">Satisfaction</div>
                </div>
            </div>
        </div>
        
        <!-- Scroll Indicator -->
        <div class="absolute bottom-10 left-1/2 -translate-x-1/2 animate-bounce">
            <i data-lucide="chevron-down" class="w-6 h-6 text-gray-500"></i>
        </div>
    </section>

    <!-- Problem Section -->
    <section id="problem" class="py-32 relative">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div class="scroll-reveal">
                    <h2 class="font-display text-4xl md:text-5xl font-medium mb-6">
                        The Silent Killer of<br>
                        <span class="text-gray-500">Modern Business</span>
                    </h2>
                    <p class="text-lg text-gray-400 mb-6 leading-relaxed">
                        In 2025, your website isn't just a digital brochure—it's your first impression, your 24/7 salesperson, and your credibility validator. Yet most businesses are stuck with:
                    </p>
                    <ul class="space-y-4">
                        <li class="flex items-start gap-3">
                            <i data-lucide="x-circle" class="w-6 h-6 text-red-500 flex-shrink-0 mt-0.5"></i>
                            <span class="text-gray-300">Websites that look like they're from 2012</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <i data-lucide="x-circle" class="w-6 h-6 text-red-500 flex-shrink-0 mt-0.5"></i>
                            <span class="text-gray-300">Broken mobile experiences that drive customers away</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <i data-lucide="x-circle" class="w-6 h-6 text-red-500 flex-shrink-0 mt-0.5"></i>
                            <span class="text-gray-300">DIY builders that look DIY (and not in a good way)</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <i data-lucide="x-circle" class="w-6 h-6 text-red-500 flex-shrink-0 mt-0.5"></i>
                            <span class="text-gray-300">Agencies charging $5k+ for what should cost $500</span>
                        </li>
                    </ul>
                </div>
                
                <div class="relative scroll-reveal">
                    <div class="aspect-[4/3] rounded-2xl overflow-hidden bg-gray-900 border border-white/10 relative group">
                        <div class="absolute inset-0 bg-gradient-to-br from-gray-800 to-gray-900"></div>
                        <div class="absolute inset-0 flex items-center justify-center">
                            <div class="text-center p-8">
                                <i data-lucide="alert-triangle" class="w-16 h-16 text-yellow-500/50 mx-auto mb-4"></i>
                                <p class="text-gray-500 font-mono text-sm">Website Last Updated: 2014</p>
                            </div>
                        </div>
                        <!-- Glitch Effect Overlay -->
                        <div class="absolute inset-0 bg-red-500/10 opacity-0 group-hover:opacity-100 transition-opacity"></div>
                    </div>
                    <div class="absolute -bottom-6 -right-6 w-48 h-48 bg-blue-500/10 rounded-full blur-3xl"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Solution Section -->
    <section id="solution" class="py-32 bg-veloft-card/30 relative overflow-hidden">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-blue-900/10 via-transparent to-transparent"></div>
        
        <div class="max-w-7xl mx-auto px-6 relative z-10">
            <div class="text-center max-w-3xl mx-auto mb-20 scroll-reveal">
                <h2 class="font-display text-4xl md:text-5xl font-medium mb-6">
                    Built for Speed.<br>
                    <span class="text-blue-400">Designed for Results.</span>
                </h2>
                <p class="text-xl text-gray-400">
                    Veloft bridges the gap between expensive agencies and DIY disasters. Professional websites, rapid turnaround, fair pricing.
                </p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-6">
                <!-- Feature 1 -->
                <div class="feature-card glow-border rounded-2xl p-8 scroll-reveal group hover:border-blue-500/30 transition-all">
                    <div class="w-12 h-12 bg-blue-500/10 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="zap" class="w-6 h-6 text-blue-400"></i>
                    </div>
                    <h3 class="font-display text-xl font-semibold mb-3">7-Day Delivery</h3>
                    <p class="text-gray-400 leading-relaxed">
                        From concept to launch in a week. No endless revision cycles. No month-long delays. Just rapid, professional execution.
                    </p>
                </div>
                
                <!-- Feature 2 -->
                <div class="feature-card glow-border rounded-2xl p-8 scroll-reveal group hover:border-blue-500/30 transition-all" style="transition-delay: 0.1s">
                    <div class="w-12 h-12 bg-purple-500/10 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="smartphone" class="w-6 h-6 text-purple-400"></i>
                    </div>
                    <h3 class="font-display text-xl font-semibold mb-3">Mobile-First Design</h3>
                    <p class="text-gray-400 leading-relaxed">
                        60%+ of traffic is mobile. Every Veloft site is crafted for thumb-scrolling perfection before desktop even enters the conversation.
                    </p>
                </div>
                
                <!-- Feature 3 -->
                <div class="feature-card glow-border rounded-2xl p-8 scroll-reveal group hover:border-blue-500/30 transition-all" style="transition-delay: 0.2s">
                    <div class="w-12 h-12 bg-green-500/10 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="trending-up" class="w-6 h-6 text-green-400"></i>
                    </div>
                    <h3 class="font-display text-xl font-semibold mb-3">Conversion Optimized</h3>
                    <p class="text-gray-400 leading-relaxed">
                        Pretty isn't enough. Strategic layouts, clear CTAs, and psychological triggers that turn visitors into customers.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Process Section -->
    <section id="process" class="py-32">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-16 items-start">
                <div class="sticky top-32 scroll-reveal">
                    <h2 class="font-display text-4xl md:text-5xl font-medium mb-6">
                        Simple Process.<br>
                        <span class="text-gray-500">Serious Results.</span>
                    </h2>
                    <p class="text-lg text-gray-400 mb-8">
                        No discovery meetings that could've been emails. No confusing jargon. Just three steps to your new digital home.
                    </p>
                    <button onclick="scrollToContact()" class="px-8 py-4 bg-white text-black rounded-full font-medium hover:bg-gray-200 transition-all">
                        Start Now
                    </button>
                </div>
                
                <div class="space-y-8">
                    <!-- Step 1 -->
                    <div class="feature-card rounded-2xl p-8 scroll-reveal border-l-4 border-blue-500">
                        <div class="flex items-start justify-between mb-4">
                            <span class="text-5xl font-display font-bold text-white/10">01</span>
                            <span class="px-3 py-1 bg-blue-500/10 text-blue-400 text-xs rounded-full">Day 1</span>
                        </div>
                        <h3 class="font-display text-2xl font-semibold mb-3">Discovery & Strategy</h3>
                        <p class="text-gray-400">
                            You fill out a brief questionnaire. We hop on a 15-minute call to align on vision, goals, and brand voice. Then we start designing.
                        </p>
                    </div>
                    
                    <!-- Step 2 -->
                    <div class="feature-card rounded-2xl p-8 scroll-reveal border-l-4 border-purple-500" style="transition-delay: 0.1s">
                        <div class="flex items-start justify-between mb-4">
                            <span class="text-5xl font-display font-bold text-white/10">02</span>
                            <span class="px-3 py-1 bg-purple-500/10 text-purple-400 text-xs rounded-full">Days 2-5</span>
                        </div>
                        <h3 class="font-display text-2xl font-semibold mb-3">Design & Build</h3>
                        <p class="text-gray-400">
                            We craft your site with modern frameworks, responsive layouts, and lightning-fast performance. You get daily updates via WhatsApp or email.
                        </p>
                    </div>
                    
                    <!-- Step 3 -->
                    <div class="feature-card rounded-2xl p-8 scroll-reveal border-l-4 border-green-500" style="transition-delay: 0.2s">
                        <div class="flex items-start justify-between mb-4">
                            <span class="text-5xl font-display font-bold text-white/10">03</span>
                            <span class="px-3 py-1 bg-green-500/10 text-green-400 text-xs rounded-full">Days 6-7</span>
                        </div>
                        <h3 class="font-display text-2xl font-semibold mb-3">Launch & Handover</h3>
                        <p class="text-gray-400">
                            Final revisions, domain connection, and deployment. We hand over the keys with a quick tutorial video so you can make small edits yourself.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="py-32 bg-veloft-card/30 relative">
        <div class="max-w-5xl mx-auto px-6">
            <div class="text-center mb-16 scroll-reveal">
                <h2 class="font-display text-4xl md:text-5xl font-medium mb-6">
                    Investment That Makes Sense
                </h2>
                <p class="text-xl text-gray-400">
                    Premium quality without the premium price tag. Transparent pricing, no hidden fees.
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <!-- Standard -->
                <div class="feature-card rounded-3xl p-8 border border-white/10 scroll-reveal">
                    <div class="mb-6">
                        <h3 class="font-display text-xl font-medium text-gray-400 mb-2">Standard</h3>
                        <div class="flex items-baseline gap-1">
                            <span class="text-5xl font-display font-bold text-white">$500</span>
                            <span class="text-gray-500">/project</span>
                        </div>
                    </div>
                    
                    <ul class="space-y-4 mb-8">
                        <li class="flex items-center gap-3 text-gray-300">
                            <i data-lucide="check" class="w-5 h-5 text-blue-500"></i>
                            <span>5-Page Website</span>
                        </li>
                        <li class="flex items-center gap-3 text-gray-300">
                            <i data-lucide="check" class="w-5 h-5 text-blue-500"></i>
                            <span>Mobile Responsive</span>
                        </li>
                        <li class="flex items-center gap-3 text-gray-300">
                            <i data-lucide="check" class="w-5 h-5 text-blue-500"></i>
                            <span>Contact Form Integration</span>
                        </li>
                        <li class="flex items-center gap-3 text-gray-300">
                            <i data-lucide="check" class="w-5 h-5 text-blue-500"></i>
                            <span>Basic SEO Setup</span>
                        </li>
                        <li class="flex items-center gap-3 text-gray-300">
                            <i data-lucide="check" class="w-5 h-5 text-blue-500"></i>
                            <span>7-Day Delivery</span>
                        </li>
                    </ul>
                    
                    <button onclick="scrollToContact()" class="w-full py-4 border border-white/20 hover:border-white/40 text-white rounded-full font-medium transition-all">
                        Get Started
                    </button>
                </div>
                
                <!-- Pro -->
                <div class="price-highlight rounded-3xl p-8 relative overflow-hidden scroll-reveal" style="transition-delay: 0.1s">
                    <div class="absolute top-4 right-4 px-3 py-1 bg-white/20 text-white text-xs rounded-full font-medium">
                        Most Popular
                    </div>
                    
                    <div class="mb-6">
                        <h3 class="font-display text-xl font-medium text-blue-100 mb-2">Pro</h3>
                        <div class="flex items-baseline gap-1">
                            <span class="text-5xl font-display font-bold text-white">$800</span>
                            <span class="text-blue-200">/project</span>
                        </div>
                    </div>
                    
                    <ul class="space-y-4 mb-8">
                        <li class="flex items-center gap-3 text-white">
                            <i data-lucide="check" class="w-5 h-5 text-white"></i>
                            <span>Everything in Standard</span>
                        </li>
                        <li class="flex items-center gap-3 text-white">
                            <i data-lucide="check" class="w-5 h-5 text-white"></i>
                            <span>Up to 10 Pages</span>
                        </li>
                        <li class="flex items-center gap-3 text-white">
                            <i data-lucide="check" class="w-5 h-5 text-white"></i>
                            <span>Custom Animations</span>
                        </li>
                        <li class="flex items-center gap-3 text-white">
                            <i data-lucide="check" class="w-5 h-5 text-white"></i>
                            <span>Blog Setup</span>
                        </li>
                        <li class="flex items-center gap-3 text-white">
                            <i data-lucide="check" class="w-5 h-5 text-white"></i>
                            <span>Priority Support (30 Days)</span>
                        </li>
                    </ul>
                    
                    <button onclick="scrollToContact()" class="w-full py-4 bg-white text-blue-600 hover:bg-gray-100 rounded-full font-medium transition-all">
                        Get Started
                    </button>
                </div>
            </div>
            
            <p class="text-center text-gray-500 mt-8 text-sm">
                Need something custom? Let's talk. Prices may vary based on complexity.
            </p>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-32 relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-blue-900/20 to-transparent"></div>
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] bg-blue-500/10 rounded-full blur-[120px]"></div>
        
        <div class="max-w-4xl mx-auto px-6 text-center relative z-10 scroll-reveal">
            <h2 class="font-display text-5xl md:text-6xl font-medium mb-6">
                Ready for a Website<br>That Actually Works?
            </h2>
            <p class="text-xl text-gray-400 mb-10 max-w-2xl mx-auto">
                Stop losing customers to outdated design. Get a modern, fast, conversion-focused website in 7 days.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                <button onclick="scrollToContact()" class="px-10 py-5 bg-blue-600 hover:bg-blue-700 text-white rounded-full font-medium text-lg transition-all flex items-center gap-2 group">
                    Start Your Project Now
                    <i data-lucide="arrow-right" class="w-5 h-5 group-hover:translate-x-1 transition-transform"></i>
                </button>
            </div>
            
            <p class="text-gray-500 mt-6 text-sm">Average response time: 2 hours</p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-32 bg-veloft-card/30 border-t border-white/5">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-16">
                <div class="scroll-reveal">
                    <h2 class="font-display text-4xl font-medium mb-6">Let's Build Something Great</h2>
                    <p class="text-gray-400 mb-8 text-lg">
                        Tell me about your project. I'll get back to you within 2 hours with next steps.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 bg-blue-500/10 rounded-full flex items-center justify-center">
                                <i data-lucide="mail" class="w-5 h-5 text-blue-400"></i>
                            </div>
                            <div>
                                <div class="text-sm text-gray-500 mb-1">Email</div>
                                <div class="text-white font-medium">[Your Email Here]</div>
                            </div>
                        </div>
                        
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 bg-green-500/10 rounded-full flex items-center justify-center">
                                <i data-lucide="message-circle" class="w-5 h-5 text-green-400"></i>
                            </div>
                            <div>
                                <div class="text-sm text-gray-500 mb-1">WhatsApp</div>
                                <div class="text-white font-medium">[Your WhatsApp Here]</div>
                            </div>
                        </div>
                        
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 bg-purple-500/10 rounded-full flex items-center justify-center">
                                <i data-lucide="clock" class="w-5 h-5 text-purple-400"></i>
                            </div>
                            <div>
                                <div class="text-sm text-gray-500 mb-1">Availability</div>
                                <div class="text-white font-medium">Mon - Fri, 9AM - 6PM EST</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="feature-card rounded-2xl p-8 scroll-reveal">
                    <form class="space-y-6" onsubmit="event.preventDefault(); alert('Form submitted! (Demo only - replace with your form handler)');">
                        <div>
                            <label class="block text-sm text-gray-400 mb-2">Name</label>
                            <input type="text" class="w-full bg-black/50 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-blue-500 transition-colors" placeholder="John Doe">
                        </div>
                        
                        <div>
                            <label class="block text-sm text-gray-400 mb-2">Email</label>
                            <input type="email" class="w-full bg-black/50 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-blue-500 transition-colors" placeholder="john@company.com">
                        </div>
                        
                        <div>
                            <label class="block text-sm text-gray-400 mb-2">Tell me about your project</label>
                            <textarea rows="4" class="w-full bg-black/50 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-blue-500 transition-colors resize-none" placeholder="I need a website for my..."></textarea>
                        </div>
                        
                        <button type="submit" class="w-full py-4 bg-blue-600 hover:bg-blue-700 text-white rounded-lg font-medium transition-all">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-12 border-t border-white/5">
        <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
            <div class="flex items-center gap-2">
                <div class="w-8 h-8 bg-gradient-to-br from-blue-500 to-blue-700 rounded-lg flex items-center justify-center font-display font-bold">
                    V
                </div>
                <span class="font-display font-semibold text-lg">Veloft</span>
            </div>
            
            <p class="text-gray-500 text-sm">
                © 2025 Veloft. Future-Proofing Your Digital Presence.
            </p>
            
            <div class="flex gap-6">
                <a href="#" class="text-gray-500 hover:text-white transition-colors">
                    <i data-lucide="twitter" class="w-5 h-5"></i>
                </a>
                <a href="#" class="text-gray-500 hover:text-white transition-colors">
                    <i data-lucide="linkedin" class="w-5 h-5"></i>
                </a>
                <a href="#" class="text-gray-500 hover:text-white transition-colors">
                    <i data-lucide="instagram" class="w-5 h-5"></i>
                </a>
            </div>
        </div>
    </footer>

    <script>
        // Initialize Lucide Icons
        lucide.createIcons();
        
        // Scroll Reveal Animation
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.scroll-reveal').forEach((el) => observer.observe(el));
        
        // Smooth scroll to contact
        function scrollToContact() {
            document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
        }
        
        // Navbar blur on scroll
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 50) {
                nav.classList.add('py-2');
                nav.classList.remove('py-4');
            } else {
                nav.classList.add('py-4');
                nav.classList.remove('py-2');
            }
        });
        
        // Parallax effect for hero
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallaxElements = document.querySelectorAll('.parallax-layer');
            parallaxElements.forEach(el => {
                const speed = el.dataset.speed || 0.5;
                el.style.transform = `translateY(${scrolled * speed}px)`;
            });
        });
    </script>
</body>
</html>
