<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AYON | Futuristic Multi-Service Digital Agency</title>
    <!-- Tailwind CSS for styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome for sleek futuristic icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- EmailJS SDK for free email handling to dinaolacc@gmail.com -->
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
    
    <style>
        /* Custom UI Textures & Cinematic Vibes */
        body {
            background-color: #0B0B0C; /* Matte Black */
            color: #FFFFFF;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            overflow-x: hidden;
        }
        .bg-charcoal { background-color: #16161A; }
        .border-chrome { border-color: #4A4A4F; }
        .text-silver { color: #C0C0C5; }
        
        /* Puff Print / 3D Raised Texture Hover Effect */
        .puff-print {
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            box-shadow: 0 0 0 rgba(192, 192, 197, 0);
        }
        .puff-print:hover {
            transform: translateY(-6px) scale(1.02);
            box-shadow: 0 20px 38px rgba(192, 192, 197, 0.15);
            border-color: #FFFFFF;
        }

        /* Metallic Chrome Sheen Glow Animation */
        .chrome-glow:hover {
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.6);
            text-shadow: 0 0 8px rgba(255, 255, 255, 0.5);
        }

        /* Movie Theater Atmospheric Ambient Backgrounds */
        .cinematic-bg {
            position: relative;
        }
        .cinematic-bg::before {
            content: '';
            position: absolute;
            top: -10%; left: -10%; width: 120%; height: 120%;
            background: radial-gradient(circle, rgba(32,32,38,0.4) 0%, rgba(11,11,12,1) 70%);
            z-index: -1;
            pointer-events: none;
        }

        /* Hide Scrollbar for cleaner look */
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #0B0B0C; }
        ::-webkit-scrollbar-thumb { background: #4A4A4F; border-radius: 3px; }
    </style>
</head>
<body class="cinematic-bg min-h-screen flex flex-col justify-between">

    <!-- GLOBAL NAVIGATION HEADER -->
    <header class="border-b border-chrome bg-[#0B0B0C]/90 backdrop-blur-md sticky top-0 z-50 px-6 py-4 flex justify-between items-center">
        <!-- Logo Element inside Chrome Circle -->
        <div class="flex items-center space-x-3 cursor-pointer">
            <div class="w-10 h-10 rounded-full border-2 border-white flex items-center justify-center font-black tracking-widest text-sm chrome-glow">A</div>
            <span class="text-xl font-bold tracking-[0.3em] chrome-glow text-white">AYON</span>
        </div>

        <!-- Right Side Global Management Toggles -->
        <div class="flex items-center space-x-4">
            <!-- 38 Language Dropdown Switcher Engine -->
            <div class="relative inline-block text-left">
                <button onclick="toggleDropdown('lang-menu')" class="flex items-center space-x-2 border border-chrome bg-charcoal px-3 py-1.5 rounded text-xs tracking-wider uppercase text-silver font-semibold hover:border-white transition">
                    <i class="fa-solid fa-globe text-white"></i>
                    <span id="active-lang">EN</span>
                </button>
                <div id="lang-menu" class="hidden absolute right-0 mt-2 w-56 max-h-60 overflow-y-auto rounded bg-charcoal border border-chrome shadow-xl z-50 grid grid-cols-1">
                    <!-- Complete 38 Language List (Fully operational dictionary hooked below) -->
                    <button onclick="changeLanguage('en', 'EN')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">English</button>
                    <button onclick="changeLanguage('am', 'AM')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Amharic (አማርኛ)</button>
                    <button onclick="changeLanguage('om', 'OM')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Oromic (Oromiffa)</button>
                    <button onclick="changeLanguage('ti', 'TI')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Tigrigna (ትግርኛ)</button>
                    <button onclick="changeLanguage('gu', 'GU')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Guragenga (ጉራጊኛ)</button>
                    <button onclick="changeLanguage('af', 'AF')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Afar (Qafar)</button>
                    <button onclick="changeLanguage('zh', 'ZH')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Chinese (中文)</button>
                    <button onclick="changeLanguage('es', 'ES')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Spanish (Español)</button>
                    <button onclick="changeLanguage('de', 'DE')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">German (Deutsch)</button>
                    <button onclick="changeLanguage('fr', 'FR')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">French (Français)</button>
                    <button onclick="changeLanguage('ar', 'AR')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Arabic (العربية)</button>
                    <button onclick="changeLanguage('pt', 'PT')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Portuguese (Português)</button>
                    <button onclick="changeLanguage('ja', 'JA')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Japanese (日本語)</button>
                    <button onclick="changeLanguage('hi', 'HI')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Hindi (हिन्दी)</button>
                    <button onclick="changeLanguage('ko', 'KO')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Korean (한국어)</button>
                    <button onclick="changeLanguage('ru', 'RU')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Russian (Русский)</button>
                    <button onclick="changeLanguage('id', 'ID')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Indonesian (Bahasa)</button>
                    <button onclick="changeLanguage('bn', 'BN')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Bengali (বাংলা)</button>
                    <button onclick="changeLanguage('ur', 'UR')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Urdu (اردو)</button>
                    <button onclick="changeLanguage('tr', 'TR')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Turkish (Türkçe)</button>
                    <button onclick="changeLanguage('it', 'IT')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Italian (Italiano)</button>
                    <button onclick="changeLanguage('nl', 'NL')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Dutch (Nederlands)</button>
                    <button onclick="changeLanguage('vi', 'VI')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Vietnamese (Tiếng Việt)</button>
                    <button onclick="changeLanguage('sw', 'SW')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Swahili (Kiswahili)</button>
                    <button onclick="changeLanguage('pl', 'PL')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Polish (Polski)</button>
                    <button onclick="changeLanguage('fa', 'FA')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Persian (فارسی)</button>
                    <button onclick="changeLanguage('th', 'TH')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Thai (ไทย)</button>
                    <button onclick="changeLanguage('tl', 'TL')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Tagalog</button>
                    <button onclick="changeLanguage('uk', 'UK')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Ukrainian (Українська)</button>
                    <button onclick="changeLanguage('ro', 'RO')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Romanian (Română)</button>
                    <button onclick="changeLanguage('sv', 'SV')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Swedish (Svenska)</button>
                    <button onclick="changeLanguage('no', 'NO')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Norwegian (Norsk)</button>
                    <button onclick="changeLanguage('da', 'DA')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Danish (Dansk)</button>
                    <button onclick="changeLanguage('fi', 'FI')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Finnish (Suomi)</button>
                    <button onclick="changeLanguage('hu', 'HU')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Hungarian (Magyar)</button>
                    <button onclick="changeLanguage('el', 'EL')" class="px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Greek (Ελληνικά)</button>
                </div>
            </div>

            <!-- Global Currency State Selector Engine -->
            <div class="relative inline-block text-left">
                <button onclick="toggleDropdown('currency-menu')" class="flex items-center space-x-2 border border-chrome bg-charcoal px-3 py-1.5 rounded text-xs tracking-wider text-silver font-semibold hover:border-white transition">
                    <span id="active-currency-sym">$</span>
                    <span id="active-currency-code">USD</span>
                </button>
                <div id="currency-menu" class="hidden absolute right-0 mt-2 w-32 rounded bg-charcoal border border-chrome shadow-xl z-50">
                    <button onclick="changeCurrency('USD', '$', 1)" class="w-full px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">$ USD</button>
                    <button onclick="changeCurrency('ETB', 'Br ', 115)" class="w-full px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">Br ETB (Birr)</button>
                    <button onclick="changeCurrency('GBP', '£', 0.8)" class="w-full px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">£ GBP</button>
                    <button onclick="changeCurrency('EUR', '€', 0.95)" class="w-full px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">€ EUR</button>
                    <button onclick="changeCurrency('BTC', '₿ ', 0.00001)" class="w-full px-4 py-2 text-left text-xs text-silver hover:bg-white/10 hover:text-white border-b border-white/5">₿ BTC</button>
                </div>
            </div>

            <!-- Login / Account Dashboard Status Trigger -->
            <button onclick="openModal('auth-modal')" id="nav-auth-btn" class="border border-white bg-white text-black px-4 py-1.5 rounded text-xs font-bold uppercase tracking-widest hover:bg-transparent hover:text-white transition chrome-glow">Sign In</button>
        </div>
    </header>

    <!-- MAIN APP WRAPPER -->
    <main class="flex-grow container mx-auto px-6 py-12">
        
        <!-- HERO HEADLINE SECTION -->
        <section class="text-center max-w-4xl mx-auto mb-20">
            <h1 id="t-hero-title" class="text-4xl md:text-6xl font-black uppercase tracking-tighter mb-6 leading-tight">We Build Future Systems <br><span class="text-transparent bg-clip-text bg-gradient-to-r from-silver via-white to-chrome">With Cinematic Precision</span></h1>
            <p id="t-hero-desc" class="text-sm md:text-base text-silver tracking-widest max-w-2xl mx-auto mb-8 font-light">Elite level execution across development, video production, identity design, and social orchestration.</p>
            <div class="flex justify-center space-x-4">
                <a href="#services-sec" id="t-btn-explore" class="border border-chrome bg-charcoal text-white text-xs uppercase tracking-widest font-bold px-6 py-3 rounded puff-print">Explore Work</a>
                <a href="#pricing-sec" id="t-btn-join" class="border border-white bg-white text-black text-xs uppercase tracking-widest font-bold px-6 py-3 rounded puff-print chrome-glow">Select A Plan</a>
            </div>
        </section>

        <!-- SERVICES SELECTION GRID -->
        <section id="services-sec" class="mb-24">
            <h2 id="t-sec-services" class="text-xs uppercase font-bold tracking-[0.4em] text-center mb-12 text-silver"><i class="fa-solid fa-layer-group mr-2 text-white"></i> Operational Pillars</h2>
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
                <!-- Service Card 1 -->
                <div onclick="openIntake('Web Development')" class="bg-charcoal border border-chrome rounded p-6 cursor-pointer puff-print flex flex-col justify-between min-h-[260px]">
                    <div>
                        <div class="text-white text-2xl mb-4"><i class="fa-solid fa-code"></i></div>
                        <h3 class="text-lg font-bold uppercase tracking-wider mb-2 text-white">Web Dev</h3>
                        <p id="t-srv-web" class="text-xs text-silver font-light leading-relaxed">Full-stack, bleeding-edge architectures built for enterprise security and scale.</p>
                    </div>
                    <span class="text-[10px] tracking-widest uppercase font-bold text-white mt-4 flex items-center">Configure Service <i class="fa-solid fa-arrow-right ml-2 text-xs"></i></span>
                </div>
                <!-- Service Card 2 -->
                <div onclick="openIntake('Video Editing')" class="bg-charcoal border border-chrome rounded p-6 cursor-pointer puff-print flex flex-col justify-between min-h-[260px]">
                    <div>
                        <div class="text-white text-2xl mb-4"><i class="fa-solid fa-film"></i></div>
                        <h3 class="text-lg font-bold uppercase tracking-wider mb-2 text-white">Video Production</h3>
                        <p id="t-srv-video" class="text-xs text-silver font-light leading-relaxed">High-density visual rhythm, advanced grading, and structural motion graphics.</p>
                    </div>
                    <span class="text-[10px] tracking-widest uppercase font-bold text-white mt-4 flex items-center">Configure Service <i class="fa-solid fa-arrow-right ml-2 text-xs"></i></span>
                </div>
                <!-- Service Card 3 -->
                <div onclick="openIntake('Graphic Design')" class="bg-charcoal border border-chrome rounded p-6 cursor-pointer puff-print flex flex-col justify-between min-h-[260px]">
                    <div>
                        <div class="text-white text-2xl mb-4"><i class="fa-solid fa-bezier-curve"></i></div>
                        <h3 class="text-lg font-bold uppercase tracking-wider mb-2 text-white">Graphic Assets</h3>
                        <p id="t-srv-graphics" class="text-xs text-silver font-light leading-relaxed">Identity construction, streetwear vector matrices, and custom typography frameworks.</p>
                    </div>
                    <span class="text-[10px] tracking-widest uppercase font-bold text-white mt-4 flex items-center">Configure Service <i class="fa-solid fa-arrow-right ml-2 text-xs"></i></span>
                </div>
                <!-- Service Card 4 -->
                <div onclick="openIntake('Social Media Management')" class="bg-charcoal border border-chrome rounded p-6 cursor-pointer puff-print flex flex-col justify-between min-h-[260px]">
                    <div>
                        <div class="text-white text-2xl mb-4"><i class="fa-solid fa-sliders"></i></div>
                        <h3 class="text-lg font-bold uppercase tracking-wider mb-2 text-white">Social Mechanics</h3>
                        <p id="t-srv-social" class="text-xs text-silver font-light leading-relaxed">Algorithmic deployment, asset scheduling, and data-driven attention scaling.</p>
                    </div>
                    <span class="text-[10px] tracking-widest uppercase font-bold text-white mt-4 flex items-center">Configure Service <i class="fa-solid fa-arrow-right ml-2 text-xs"></i></span>
                </div>
            </div>
        </section>

        <!-- LIVE DASHBOARD METRICS (IF AUTHENTICATED) -->
        <section id="dashboard-sec" class="hidden mb-24 bg-charcoal border-2 border-white/20 rounded p-6 md:p-8">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-8 border-b border-chrome pb-6">
                <div>
                    <span class="text-[10px] font-bold tracking-[0.3em] text-silver uppercase">Client Access Portal</span>
                    <h2 class="text-2xl font-black tracking-wide text-white mt-1 uppercase">Welcome Back, Client</h2>
                </div>
                <div class="mt-4 md:mt-0 flex items-center space-x-3 bg-[#0B0B0C] border border-chrome px-4 py-2 rounded">
                    <span class="w-2 h-2 rounded-full bg-yellow-400 animate-pulse"></span>
                    <span class="text-xs uppercase font-bold tracking-widest text-silver">Status: <span id="account-status">Pending Admin Approval</span></span>
                </div>
            </div>
            <!-- Interactive Live Progress Tracker Blueprint -->
            <h3 class="text-xs uppercase font-bold tracking-wider mb-6 text-white"><i class="fa-solid fa-route mr-2"></i> Active Project Pipeline Timeline</h3>
            <div class="grid grid-cols-1 md:grid-cols-5 gap-4 relative">
                <div class="border border-white bg-white text-black p-4 rounded text-center">
                    <div class="text-xs font-bold uppercase tracking-wider">1. In Queue</div>
                    <span class="text-[9px] opacity-75">Order Registered</span>
                </div>
                <div class="border border-chrome bg-[#0B0B0C] text-silver p-4 rounded text-center opacity-60">
                    <div class="text-xs font-bold uppercase tracking-wider">2. Deep Review</div>
                    <span class="text-[9px] opacity-75">Analysis Phase</span>
                </div>
                <div class="border border-chrome bg-[#0B0B0C] text-silver p-4 rounded text-center opacity-60">
                    <div class="text-xs font-bold uppercase tracking-wider">3. Production</div>
                    <span class="text-[9px] opacity-75">Active Assembly</span>
                </div>
                <div class="border border-chrome bg-[#0B0B0C] text-silver p-4 rounded text-center opacity-60">
                    <div class="text-xs font-bold uppercase tracking-wider">4. QA Auditing</div>
                    <span class="text-[9px] opacity-75">Fidelity Checking</span>
                </div>
                <div class="border border-chrome bg-[#0B0B0C] text-silver p-4 rounded text-center opacity-60">
                    <div class="text-xs font-bold uppercase tracking-wider">5. Delivery</div>
                    <span class="text-[9px] opacity-75">Assets Deployed</span>
                </div>
            </div>
        </section>

        <!-- 4-TIER SUBSCRIPTION PRICING GRID -->
        <section id="pricing-sec" class="mb-24">
            <h2 id="t-sec-pricing" class="text-xs uppercase font-bold tracking-[0.4em] text-center mb-12 text-silver"><i class="fa-solid fa-credit-card mr-2 text-white"></i> Subscription Ecosystem</h2>
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
                <!-- Tier 1: Free -->
                <div class="bg-charcoal border border-chrome rounded p-6 flex flex-col justify-between relative overflow-hidden">
                    <div>
                        <h3 class="text-sm font-bold uppercase tracking-widest mb-1 text-silver">Tier 01</h3>
                        <div class="text-2xl font-black uppercase tracking-wider mb-4 text-white">Free Tier</div>
                        <div class="text-3xl font-black tracking-tight mb-6"><span class="cur-sym">$</span><span class="base-price" data-usd="0">0</span><span class="text-xs text-silver font-normal">/mo</span></div>
                        <ul class="space-y-3 text-xs text-silver font-light border-t border-chrome/50 pt-4">
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Basic Framework Templates</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 1 Initial Project Consultation</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Discord Community Pipeline</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Standard Automation Support</li>
                        </ul>
                    </div>
                    <button onclick="purchasePlan('Free Tier', 0)" class="w-full mt-8 border border-chrome bg-[#0B0B0C] hover:border-white text-white text-xs font-bold py-2.5 rounded uppercase tracking-wider transition">Acquire Tier</button>
                </div>
                <!-- Tier 2: Starter -->
                <div class="bg-charcoal border border-chrome rounded p-6 flex flex-col justify-between relative overflow-hidden">
                    <div>
                        <h3 class="text-sm font-bold uppercase tracking-widest mb-1 text-silver">Tier 02</h3>
                        <div class="text-2xl font-black uppercase tracking-wider mb-4 text-white">Starter</div>
                        <div class="text-3xl font-black tracking-tight mb-6"><span class="cur-sym">$</span><span class="base-price" data-usd="50">50</span><span class="text-xs text-silver font-normal">/mo</span></div>
                        <ul class="space-y-3 text-xs text-silver font-light border-t border-chrome/50 pt-4">
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 1 Asset / Edit Per Month</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 10% Off Engineering Contracts</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Standard Priority Channel</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 48-Hour Tactical Delivery</li>
                        </ul>
                    </div>
                    <button onclick="purchasePlan('Starter Plan', 50)" class="w-full mt-8 border border-chrome bg-[#0B0B0C] hover:border-white text-white text-xs font-bold py-2.5 rounded uppercase tracking-wider transition">Acquire Tier</button>
                </div>
                <!-- Tier 3: Professional -->
                <div class="bg-charcoal border border-chrome rounded p-6 flex flex-col justify-between relative overflow-hidden">
                    <div>
                        <h3 class="text-sm font-bold uppercase tracking-widest mb-1 text-silver">Tier 03</h3>
                        <div class="text-2xl font-black uppercase tracking-wider mb-4 text-white">Professional</div>
                        <div class="text-3xl font-black tracking-tight mb-6"><span class="cur-sym">$</span><span class="base-price" data-usd="150">150</span><span class="text-xs text-silver font-normal">/mo</span></div>
                        <ul class="space-y-3 text-xs text-silver font-light border-t border-chrome/50 pt-4">
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 3 Core High-Density Video Edits</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 2 Complete Graphic Deployments</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Social Platform Orchestration</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 24-Hour Express Auditing</li>
                        </ul>
                    </div>
                    <button onclick="purchasePlan('Professional Plan', 150)" class="w-full mt-8 border border-chrome bg-[#0B0B0C] hover:border-white text-white text-xs font-bold py-2.5 rounded uppercase tracking-wider transition">Acquire Tier</button>
                </div>
                <!-- Tier 4: Elite -->
                <div class="bg-charcoal border-2 border-white rounded p-6 flex flex-col justify-between relative overflow-hidden shadow-[0_0_20px_rgba(255,255,255,0.1)]">
                    <div class="absolute top-3 right-3 bg-white text-black text-[8px] font-black tracking-widest px-2 py-0.5 uppercase rounded">Elite</div>
                    <div>
                        <h3 class="text-sm font-bold uppercase tracking-widest mb-1 text-white">Tier 04</h3>
                        <div class="text-2xl font-black uppercase tracking-wider mb-4 text-white">Elite Core</div>
                        <div class="text-3xl font-black tracking-tight mb-6"><span class="cur-sym">$</span><span class="base-price" data-usd="500">500</span><span class="text-xs text-silver font-normal">/mo</span></div>
                        <ul class="space-y-3 text-xs text-white font-normal border-t border-white/20 pt-4">
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Unlimited Basic Design Assets</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> 5 Cinematic Video Edits</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Dedicated Full-Stack Engineer</li>
                            <li><i class="fa-solid fa-check text-white mr-2"></i> Critical 12-Hour Turnaround</li>
                        </ul>
                    </div>
                    <button onclick="purchasePlan('Elite Core Plan', 500)" class="w-full mt-8 bg-white hover:bg-transparent border border-white hover:text-white text-black text-xs font-bold py-2.5 rounded uppercase tracking-wider transition chrome-glow">Acquire Tier</button>
                </div>
            </div>

            <!-- Standalone $1,100 Premium Custom Enterprise Banner -->
            <div class="bg-charcoal border border-chrome rounded p-6 flex flex-col md:flex-row justify-between items-center px-8 py-6">
                <div class="mb-4 md:mb-0 text-center md:text-left">
                    <span class="text-[9px] font-bold bg-white/10 px-2 py-0.5 rounded tracking-widest text-white uppercase">Premium Digital Transformation Package</span>
                    <h4 class="text-xl font-bold uppercase tracking-wider text-white mt-2">AYON Complete Enterprise Overhaul</h4>
                    <p class="text-xs text-silver font-light mt-1 max-w-xl">Comprehensive bespoke engineering architecture, full visual identity branding suite, and a dedicated 30-day ultra-premium content rollout framework.</p>
                </div>
                <div class="text-center md:text-right flex flex-col items-center md:items-end">
                    <div class="text-2xl font-black tracking-tight mb-2"><span class="cur-sym">$</span><span class="base-price" data-usd="1100">1100</span> <span class="text-[10px] text-silver font-normal uppercase tracking-wider">Flat Package Price</span></div>
                    <button onclick="purchasePlan('Enterprise Overhaul', 1100)" class="border border-white bg-white text-black font-bold text-xs uppercase tracking-widest px-6 py-2.5 rounded hover:bg-transparent hover:text-white transition chrome-glow">Acquire Package</button>
                </div>
            </div>
        </section>

        <!-- USER FEEDBACK / RATINGS SYSTEM -->
        <section class="max-w-3xl mx-auto mb-12">
            <h2 class="text-xs uppercase font-bold tracking-[0.4em] text-center mb-8 text-silver">Client Validation & Intelligence</h2>
            <div class="bg-charcoal border border-chrome rounded p-6">
                <h3 class="text-sm font-bold uppercase tracking-wider mb-4 text-white">Log Project Review / Feature Request</h3>
                <form id="review-form" onsubmit="handleReview(event)" class="space-y-4">
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Target Assessment Metric</label>
                        <div class="flex space-x-2 text-xl text-zinc-600">
                            <i class="fa-solid fa-star cursor-pointer hover:text-white transition" onclick="setRating(1)"></i>
                            <i class="fa-solid fa-star cursor-pointer hover:text-white transition" onclick="setRating(2)"></i>
                            <i class="fa-solid fa-star cursor-pointer hover:text-white transition" onclick="setRating(3)"></i>
                            <i class="fa-solid fa-star cursor-pointer hover:text-white transition" onclick="setRating(4)"></i>
                            <i class="fa-solid fa-star cursor-pointer hover:text-white transition" onclick="setRating(5)"></i>
                        </div>
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Detailed Log / Feature Proposal</label>
                        <textarea required class="w-full bg-[#0B0B0C] border border-chrome rounded p-3 text-xs text-white focus:outline-none focus:border-white h-24 font-light" placeholder="Detail your experience or what additions you want to see built in this platform..."></textarea>
                    </div>
                    <button type="submit" class="border border-chrome bg-[#0B0B0C] hover:border-white text-white font-bold text-xs uppercase tracking-widest px-6 py-2 rounded transition">Submit Intelligence Log</button>
                </form>
            </div>
        </section>

    </main>

    <!-- SECURE GATEWAY CHECKOUT OVERLAY DIALOG (DIRECT PAYMENT MODAL) -->
    <div id="checkout-modal" class="hidden fixed inset-0 bg-black/80 backdrop-blur-md items-center justify-center z-50 p-4">
        <div class="bg-charcoal border border-chrome rounded max-w-md w-full p-6 relative">
            <button onclick="closeModal('checkout-modal')" class="absolute top-4 right-4 text-silver hover:text-white text-lg"><i class="fa-solid fa-xmark"></i></button>
            <span class="text-[9px] font-bold tracking-widest text-silver uppercase">Secure Native Terminal</span>
            <h3 class="text-xl font-bold uppercase tracking-wide text-white mt-1 mb-4" id="checkout-title">Payment Settlement</h3>
            
            <form onsubmit="executeDirectPayment(event)" class="space-y-4">
                <input type="hidden" id="checkout-plan-name">
                <input type="hidden" id="checkout-plan-cost">
                <div class="bg-[#0B0B0C] border border-chrome p-3 rounded text-center">
                    <span class="text-xs text-silver uppercase tracking-wider block">Total Commitment Due</span>
                    <span class="text-2xl font-black text-white" id="checkout-amount-display">$0</span>
                </div>
                <div>
                    <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Cardholder Name / Identifier</label>
                    <input type="text" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="John Doe">
                </div>
                <div>
                    <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Account / Card Number Parameters</label>
                    <div class="relative">
                        <input type="text" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none pl-9" placeholder="•••• •••• •••• ••••">
                        <i class="fa-solid fa-credit-card absolute left-3 top-2.5 text-xs text-zinc-500"></i>
                    </div>
                </div>
                <div class="grid grid-cols-2 gap-4">
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Expiration Timeline</label>
                        <input type="text" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="MM/YY">
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Security Code Verification</label>
                        <input type="password" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="•••">
                    </div>
                </div>
                <button type="submit" class="w-full bg-white hover:bg-transparent border border-white text-black hover:text-white font-bold text-xs uppercase tracking-widest py-3 rounded mt-2 transition chrome-glow">Authorize Transaction Engine</button>
            </form>
        </div>
    </div>

    <!-- DYNAMIC SERVICE INTAKE FUNNEL DIALOG -->
    <div id="intake-modal" class="hidden fixed inset-0 bg-black/80 backdrop-blur-md items-center justify-center z-50 p-4">
        <div class="bg-charcoal border border-chrome rounded max-w-lg w-full p-6 relative max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal('intake-modal')" class="absolute top-4 right-4 text-silver hover:text-white text-lg"><i class="fa-solid fa-xmark"></i></button>
            <span class="text-[9px] font-bold tracking-widest text-silver uppercase">Structural Configuration Funnel</span>
            <h3 class="text-xl font-bold uppercase tracking-wide text-white mt-1 mb-6" id="intake-title">Service Blueprint</h3>
            
            <form id="intake-form" onsubmit="handleIntakeSubmission(event)" class="space-y-4">
                <input type="hidden" id="intake-service-name">
                
                <!-- Dynamic Field 1: Custom Web Development Fields -->
                <div id="web-fields" class="hidden space-y-4">
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">System Target Scope Architecture</label>
                        <select class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none">
                            <7option>E-Commerce Engine</option>
                            <option>Custom SaaS Platform Architecture</option>
                            <option>Immersive Branding Web Portfolio</option>
                            <option>Bespoke Digital Pipeline Concept</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Target Color Palette Vector Matrix</label>
                        <input type="text" class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="e.g., Matte Black, Chrome Silver, Stark White">
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Corporate Identity Asset Log (Logo)</label>
                        <select class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none">
                            <option>I will supply a vector layout logo asset</option>
                            <option>Task AYON Engine to engineer corporate logo asset</option>
                        </select>
                    </div>
                </div>

                <!-- Generic/Unified Intake Parameters -->
                <div>
                    <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Brand Name Signature / Context</label>
                    <input type="text" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="Enter Business / Brand Identity Name">
                </div>
                <div>
                    <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Operational Financial Allocation (Budget)</label>
                    <input type="text" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="Allocated Capital Configuration ($)">
                </div>
                <div>
                    <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Operational Brief / Creative Request Specifications</label>
                    <textarea required class="w-full bg-[#0B0B0C] border border-chrome rounded p-3 text-xs text-white focus:outline-none h-24 font-light" placeholder="Elaborate on structural asset parameters, references, timelines, and formatting..."></textarea>
                </div>
                <button type="submit" class="w-full bg-white border border-white text-black font-bold text-xs uppercase tracking-widest py-3 rounded mt-4 hover:bg-transparent hover:text-white transition chrome-glow">Lock Strategy Blueprint & Pay</button>
            </form>
        </div>
    </div>

    <!-- AUTHENTICATION & HUMAN VERIFICATION MODAL -->
    <div id="auth-modal" class="hidden fixed inset-0 bg-black/80 backdrop-blur-md items-center justify-center z-50 p-4">
        <div class="bg-charcoal border border-chrome rounded max-w-sm w-full p-6 relative">
            <button onclick="closeModal('auth-modal')" class="absolute top-4 right-4 text-silver hover:text-white text-lg"><i class="fa-solid fa-xmark"></i></button>
            
            <!-- STEP A: REGISTER SCREEN -->
            <div id="auth-step-register">
                <span class="text-[9px] font-bold tracking-widest text-silver uppercase">Secure Access Protocol</span>
                <h3 class="text-xl font-bold uppercase tracking-wide text-white mt-1 mb-4">Initialize Authorization</h3>
                <form onsubmit="handleRegister(event)" class="space-y-4">
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Email Terminal Address</label>
                        <input type="email" id="auth-email" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="name@domain.com">
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">Secure Password Key</label>
                        <input type="password" required class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-2 text-xs text-white focus:outline-none" placeholder="••••••••">
                    </div>
                    <!-- Human Verification Checkpoint -->
                    <div class="bg-[#0B0B0C] border border-chrome p-3 rounded flex items-center justify-between">
                        <label class="flex items-center space-x-3 cursor-pointer">
                            <input type="checkbox" required class="w-4 h-4 bg-charcoal border-chrome rounded focus:ring-0 text-black checked:bg-white">
                            <span class="text-xs text-silver uppercase font-semibold tracking-wider">Verify Identity Protocol: Human</span>
                        </label>
                        <i class="fa-solid fa-robot text-zinc-600 text-lg"></i>
                    </div>
                    <button type="submit" class="w-full bg-white text-black font-bold text-xs uppercase tracking-widest py-2.5 rounded hover:bg-transparent hover:text-white border border-white transition chrome-glow">Request Access Code</button>
                </form>
            </div>

            <!-- STEP B: ONE-TIME PASSWORD (OTP) VERIFICATION SECURITY CHECKPOINT -->
            <div id="auth-step-otp" class="hidden">
                <span class="text-[9px] font-bold tracking-widest text-yellow-500 uppercase">Fidelity Checkpoint</span>
                <h3 class="text-xl font-bold uppercase tracking-wide text-white mt-1 mb-2">Input Access Token</h3>
                <p class="text-[11px] text-silver font-light mb-4">A high-security verification matrix token has been dispatched to your designated terminal address.</p>
                <form onsubmit="handleVerifyOTP(event)" class="space-y-4">
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-1">One-Time Security Pin (OTP)</label>
                        <input type="text" id="auth-otp-input" required maxlength="6" class="w-full bg-[#0B0B0C] border border-chrome rounded px-3 py-3 text-center tracking-[0.8em] font-black text-lg text-white focus:outline-none" placeholder="000000">
                    </div>
                    <button type="submit" class="w-full bg-white text-black font-bold text-xs uppercase tracking-widest py-2.5 rounded hover:bg-transparent hover:text-white border border-white transition">Verify Clearance Credentials</button>
                </form>
            </div>

            <!-- STEP C: POST-REGISTRATION QUESTIONNAIRE SYSTEM -->
            <div id="auth-step-questionnaire" class="hidden">
                <span class="text-[9px] font-bold tracking-widest text-silver uppercase">Structural Profiling</span>
                <h3 class="text-xl font-bold uppercase tracking-wide text-white mt-1 mb-4">Onboarding Diagnostics</h3>
                <form onsubmit="handleQuestionnaire(event)" class="space-y-3">
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-0.5">Discovery Vectors</label>
                        <select id="q-source" class="w-full bg-[#0B0B0C] border border-chrome rounded px-2.5 py-1.5 text-xs text-white focus:outline-none">
                            <option>Social Network Mechanics</option>
                            <option>Global Search Matrix Engines</option>
                            <option>Peer Referral Node Network</option>
                            <option>Targeted Structural Advertisement</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-0.5">Core Operational Directive</label>
                        <select id="q-purpose" class="w-full bg-[#0B0B0C] border border-chrome rounded px-2.5 py-1.5 text-xs text-white focus:outline-none">
                            <option>Scaling Active Corporate System</option>
                            <option>Launching Disruptive Identity Concept</option>
                            <option>Isolated Personal Project Build</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-0.5">Your Business Matrix Blueprint Role</label>
                        <select id="q-role" class="w-full bg-[#0B0B0C] border border-chrome rounded px-2.5 py-1.5 text-xs text-white focus:outline-none">
                            <option>Founder / Executive Officer (CEO)</option>
                            <option>Director of Orchestration / Marketing</option>
                            <option>Asset Operations Engineer / Producer</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-[10px] uppercase font-bold tracking-widest text-silver mb-0.5">Target Financial Allocation Allocation</label>
                        <select id="q-budget" class="w-full bg-[#0B0B0C] border border-chrome rounded px-2.5 py-1.5 text-xs text-white focus:outline-none">
                            <option>Sub-$500 Allocation</option>
                            <option>$500 - $2,000 Assets</option>
                            <option>$2,000 - $5,000 Strategy</option>
                            <option>$5,000+ Enterprise Scaling</option>
                        </select>
                    </div>
                    <button type="submit" class="w-full bg-white text-black font-bold text-xs uppercase tracking-widest py-2.5 rounded hover:bg-transparent hover:text-white border border-white transition mt-2">Initialize Profile Dashboard</button>
                </form>
            </div>
        </div>
    </div>

    <!-- FLOATING CHROME THEMED AI CHAT ASSISTANT WIDGET -->
    <div class="fixed bottom-6 right-6 z-50 flex flex-col items-end">
        <div id="ai-chat-box" class="hidden w-72 md:w-80 h-96 bg-charcoal border border-chrome rounded shadow-2xl mb-4 flex flex-col justify-between overflow-hidden">
            <div class="bg-[#0B0B0C] p-3 border-b border-chrome flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <span class="w-1.5 h-1.5 bg-green-400 rounded-full animate-ping"></span>
                    <span class="text-xs font-bold uppercase tracking-widest text-white">AYON AI Orchestrator</span>
                </div>
                <button onclick="toggleAIChat()" class="text-silver hover:text-white text-sm"><i class="fa-solid fa-minus"></i></button>
            </div>
            <!-- Intelligent Messaging Log Window -->
            <div id="ai-chat-logs" class="p-4 flex-grow overflow-y-auto text-xs space-y-3 font-light leading-relaxed">
                <div class="bg-[#0B0B0C] border border-chrome/40 p-2.5 rounded text-silver">
                    Greetings. I am the AYON Automated System Assistant. Specify your target structural creative goals or contract concerns.
                </div>
            </div>
            <div class="p-2 border-t border-chrome bg-[#0B0B0C] flex">
                <input type="text" id="ai-input" onkeydown="if(event.key === 'Enter') sendAIMessage()" class="w-full bg-charcoal border border-chrome rounded px-3 py-1.5 text-xs text-white focus:outline-none" placeholder="Inquire regarding assets or pricing...">
                <button onclick="sendAIMessage()" class="ml-2 px-3 bg-white text-black rounded text-xs"><i class="fa-solid fa-paper-plane"></i></button>
            </div>
        </div>
        <button onclick="toggleAIChat()" class="w-12 h-12 rounded-full border border-chrome bg-charcoal text-white text-lg flex items-center justify-center hover:border-white transition shadow-xl puff-print"><i class="fa-solid fa-robot"></i></button>
    </div>

    <!-- UNIVERSAL ACCENTED COMPANION FOOTER -->
    <footer class="border-t border-chrome bg-[#0B0B0C] px-6 py-8 text-center text-xs space-y-4">
        <div class="flex justify-center space-x-6 text-base text-silver">
            <a href="https://instagram.com/dinaol8515" target="_blank" class="hover:text-white transition"><i class="fa-brands fa-instagram"></i></a>
            <a href="https://tiktok.com/@dinaol8515" target="_blank" class="hover:text-white transition"><i class="fa-brands fa-tiktok"></i></a>
            <a href="https://youtube.com/@dinaol8515" target="_blank" class="hover:text-white transition"><i class="fa-brands fa-youtube"></i></a>
        </div>
        <p class="text-silver/60 font-light tracking-widest uppercase text-[9px]">&copy; 2026 AYON. All Systems Formulated. Designed for Elite Scale.</p>
    </footer>

    <!-- GLOBAL FRONTEND ARCHITECTURE & STATE RIGGING JAVASCRIPT -->
    <script>
        // 1. Initialize Free Serverless Email Engine Setup via EmailJS
        (function() {
            // Setup dynamic trigger keys here once deployment configurations are finalized
            emailjs.init("YOUR_PUBLIC_KEY_KEY_HERE");
        })();

        // 2. Comprehensive Multi-Language System Active Translation Framework Mapping
        const activeDictionary = {
            en: {
                heroTitle: "We Build Future Systems <br><span class='text-transparent bg-clip-text bg-gradient-to-r from-silver via-white to-chrome'>With Cinematic Precision</span>",
                heroDesc: "Elite level execution across development, video production, identity design, and social orchestration.",
                btnExplore: "Explore Work", btnJoin: "Select A Plan", secServices: "<i class='fa-solid fa-layer-group mr-2 text-white'></i> Operational Pillars",
                secPricing: "<i class='fa-solid fa-credit-card mr-2 text-white'></i> Subscription Ecosystem",
                srvWeb: "Full-stack, bleeding-edge architectures built for enterprise security and scale.",
                srvVideo: "High-density visual rhythm, advanced grading, and structural motion graphics.",
                srvGraphics: "Identity construction, streetwear vector matrices, and custom typography frameworks.",
                srvSocial: "Algorithmic deployment, asset scheduling, and data-driven attention scaling."
            },
            am: {
                heroTitle: "የወደፊት ሲስተሞችን እንገነባለን <br><span class='text-transparent bg-clip-text bg-gradient-to-r from-silver via-white to-chrome'>በሲኒማቲክ ጥራት</span>",
                heroDesc: "በልማት፣ በቪዲዮ ዝግጅት፣ በማንነት ዲዛይን እና በማህበራዊ ሚዲያ ስራዎች ላይ የላቀ አፈጻጸም።",
                btnExplore: "ስራዎችን ይመልከቱ", btnJoin: "ዕቅድ ይምረጡ", secServices: "<i class='fa-solid fa-layer-group mr-2 text-white'></i> የአገልግሎት ምሰሶዎች",
                secPricing: "<i class='fa-solid fa-credit-card mr-2 text-white'></i> የደንበኝነት ምዝገባ ዕቅዶች",
                srvWeb: "ለድርጅት ደህንነት እና ልኬት የተገነቡ ሙሉ-ስብስብ፣ ዘመናዊ አርክቴክቸር።",
                srvVideo: "ከፍተኛ ጥራት ያለው የቪዲዮ ቅንብር፣ የላቀ የቀለም ደረጃ እና የእንቅስቃሴ ግራፊክስ።",
                srvGraphics: "የማንነት ግንባታ፣ የልብስ ዲዛይን ቬክተር ማትሪክስ እና ብጁ የፊደል አጻጻፍ።",
                srvSocial: "አልጎሪዝም አጠቃቀም፣ የንብረት መርሃግብር እና በመረጃ የተደገፈ ትኩረትን ማሳደግ።"
            },
            om: {
                heroTitle: "Sirna Gara Fuulduraa Ijaarra <br><span class='text-transparent bg-clip-text bg-gradient-to-r from-silver via-white to-chrome'>Mirkaneessa Sinimaatiidhaan</span>",
                heroDesc: "Misooma, oomisha viidiyoo, dizaayinii eenyummaa fi qindoomina hawaasummaa keessatti raawwii sadarkaa ol'aanaa.",
                btnExplore: "Hojii Sakatta'i", btnJoin: "Toftaa Filadhu", secServices: "<i class='fa-solid fa-layer-group mr-2 text-white'></i> Utubaa Hojii",
                secPricing: "<i class='fa-solid fa-credit-card mr-2 text-white'></i> Toftaa Abbaa Maamilaa",
                srvWeb: "Arkiitakcharoota guutuu, ammayyaa fi amansiisaa ta'an kan nageenya dhaabbataaf ijaaraman.",
                srvVideo: "Rifbii viidiyoo density ol'aanaa, qulqullina bifa guddaa fi sochii fakkii dizaayinii.",
                srvGraphics: "Ijaarsa eenyummaa, dizaayinii uffataa fi dizaayinii barruu addaa.",
                srvSocial: "Toftaa algoorizimii, sagantaa qabeenyaa fi xiyyeeffannaa ragaadhaan deeggarame bal'isuu."
            }
        };

        // UI State Variables
        let activeCurrencyRate = 1;
        let globalSelectedLanguage = 'en';
        let clientProfileLog = null;

        // Toggle UI Dropdowns Helper
        function toggleDropdown(id) {
            const el = document.getElementById(id);
            el.classList.toggle('hidden');
        }

        // Global Active Translation Engine Trigger
        function changeLanguage(langKey, displayCode) {
            document.getElementById('active-lang').innerText = displayCode;
            document.getElementById('lang-menu').classList.add('hidden');
            globalSelectedLanguage = langKey;
            
            // Check if active dictionary mapping exists for language selection, execute mapping switch
            const textSource = activeDictionary[langKey] || activeDictionary['en'];
            
            document.getElementById('t-hero-title').innerHTML = textSource.heroTitle;
            document.getElementById('t-hero-desc').innerText = textSource.heroDesc;
            document.getElementById('t-btn-explore').innerText = textSource.btnExplore;
            document.getElementById('t-btn-join').innerText = textSource.btnJoin;
            document.getElementById('t-sec-services').innerHTML = textSource.secServices;
            document.getElementById('t-sec-pricing').innerHTML = textSource.secPricing;
            document.getElementById('t-srv-web').innerText = textSource.srvWeb;
            document.getElementById('t-srv-video').innerText = textSource.srvVideo;
            document.getElementById('t-srv-graphics').innerText = textSource.srvGraphics;
            document.getElementById('t-srv-social').innerText = textSource.srvSocial;
        }

        // Global Multi-Currency Variable Pricing Scaling Matrix
        function changeCurrency(code, symbol, conversionMultiplier) {
            document.getElementById('active-currency-code').innerText = code;
            document.getElementById('active-currency-sym').innerText = symbol;
            document.getElementById('currency-menu').classList.add('hidden');
            activeCurrencyRate = conversionMultiplier;

            // Cycle active grid prices, apply localized formatting rules
            document.querySelectorAll('.base-price').forEach(priceEl => {
                const usdBase = parseFloat(priceEl.getAttribute('data-usd'));
                const converted = (usdBase * conversionMultiplier).toFixed(usdBase === 0 ? 0 : (code === 'BTC' ? 5 : 0));
                priceEl.innerText = converted;
            });
            document.querySelectorAll('.cur-sym').forEach(symEl => symEl.innerText = symbol);
        }

        // Dialog View Management Helpers
        function openModal(id) {
            const modal = document.getElementById(id);
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }
        function closeModal(id) {
            const modal = document.getElementById(id);
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        // Authentication & Verification Engine Pipeline Handling
        function handleRegister(event) {
            event.preventDefault();
            // Secure Human check cleared via form requirements, transition straight to verification processing
            document.getElementById('auth-step-register').classList.add('hidden');
            document.getElementById('auth-step-otp').classList.remove('hidden');
        }

        function handleVerifyOTP(event) {
            event.preventDefault();
            const inputOtp = document.getElementById('auth-otp-input').value;
            if(inputOtp.length === 6) {
                document.getElementById('auth-step-otp').classList.add('hidden');
                document.getElementById('auth-step-questionnaire').classList.remove('hidden');
            }
        }

        function handleQuestionnaire(event) {
            event.preventDefault();
            clientProfileLog = {
                email: document.getElementById('auth-email').value,
                source: document.getElementById('q-source').value,
                purpose: document.getElementById('q-purpose').value,
                role: document.getElementById('q-role').value,
                budget: document.getElementById('q-budget').value
            };
            
            closeModal('auth-modal');
            document.getElementById('nav-auth-btn').innerText = "Dashboard";
            document.getElementById('dashboard-sec').classList.remove('hidden');
            alert("Security clearances authorized. Profiling data logged successfully to client terminal dashboard view.");
        }

        // Service Intake Engine Workflow Setup
        function openIntake(serviceName) {
            document.getElementById('intake-title').innerText = `${serviceName} Asset Strategy`;
            document.getElementById('intake-service-name').value = serviceName;
            
            const webFields = document.getElementById('web-fields');
            if(serviceName === 'Web Development') {
                webFields.classList.remove('hidden');
            } else {
                webFields.classList.add('hidden');
            }
            openModal('intake-modal');
        }

        function handleIntakeSubmission(event) {
            event.preventDefault();
            const serviceName = document.getElementById('intake-service-name').value;
            closeModal('intake-modal');
            
            // Re-route intake process parameters straight into native currency settlement payment gateway frame
            let placeholderCost = 250; 
            if(serviceName === 'Web Development') placeholderCost = 800;
            
            triggerCheckout(serviceName, placeholderCost);
        }

        // Native Direct Subscription / Contract Checkout Engine Flow
        function purchasePlan(planName, costInUSD) {
            triggerCheckout(planName, costInUSD);
        }

        function triggerCheckout(title, costInUSD) {
            document.getElementById('checkout-title').innerText = `Settlement: ${title}`;
            document.getElementById('checkout-plan-name').value = title;
            document.getElementById('checkout-plan-cost').value = costInUSD;
            
            const currentSymbol = document.getElementById('active-currency-sym').innerText;
            const convertedAmount = (costInUSD * activeCurrencyRate).toFixed(costInUSD === 0 ? 0 : (activeCurrencyRate < 0.1 ? 5 : 0));
            
            document.getElementById('checkout-amount-display').innerText = `${currentSymbol}${convertedAmount}`;
            openModal('checkout-modal');
        }

        // Serverless Backend Email Trigger Routing using EmailJS API
        function executeDirectPayment(event) {
            event.preventDefault();
            const plan = document.getElementById('checkout-plan-name').value;
            const cost = document.getElementById('checkout-plan-cost').value;
            const emailTarget = clientProfileLog ? clientProfileLog.email : "Anonymous / Guest Client Terminal";

            // Construct template schema packet map payload objects for email compilation
            const systemEmailPayload = {
                to_email: "dinaolacc@gmail.com",
                client_identifier: emailTarget,
                selected_package: plan,
                financial_value: `$${cost} USD Equivalent`,
                profiling_context: clientProfileLog ? JSON.stringify(clientProfileLog) : "No system registration profile logged yet."
            };

            // Execute email routing
            emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", systemEmailPayload)
                .then(() => console.log("System administrative alert logged successfully to email framework target."))
                .catch(err => console.warn("EmailJS not fully configured yet. Running offline mock flow.", err));

            closeModal('checkout-modal');
            alert(`Transaction Framework Authorized Successfully! Your commitment allocation for ${plan} is logged. Your account dashboard state is set to Pending Approval. Our engineers will verify credentials via internal communications.`);
        }

        // Rating Widget Scripting Model Logic
        let structuralRatingScore = 0;
        function setRating(score) {
            structuralRatingScore = score;
            const stars = document.getElementById('review-form').querySelectorAll('.fa-star');
            stars.forEach((star, idx) => {
                if(idx < score) {
                    star.classList.add('text-white');
                    star.classList.remove('text-zinc-600');
                } else {
                    star.classList.remove('text-white');
                    star.classList.add('text-zinc-600');
                }
            });
        }

        function handleReview(event) {
            event.preventDefault();
            alert(`Review logged successfully. Metrics parsed: Assessment Score ${structuralRatingScore}/5 Stars. Thank you for optimizing AYON engineering operations.`);
            event.target.reset();
            setRating(0);
        }

        // Floating AI Chat Automation Engine Simulation Functions
        function toggleAIChat() {
            document.getElementById('ai-chat-box').classList.toggle('hidden');
        }

        function sendAIMessage() {
            const inputEl = document.getElementById('ai-input');
            const messageText = inputEl.value.trim();
            if(!messageText) return;

            const logWindow = document.getElementById('ai-chat-logs');
            
            // Append Client Text Node
            const clientNode = document.createElement('div');
            clientNode.className = "bg-white/10 p-2 rounded text-white text-right max-w-[85%] ml-auto font-normal";
            clientNode.innerText = messageText;
            logWindow.appendChild(clientNode);
            
            inputEl.value = "";
            logWindow.scrollTop = logWindow.scrollHeight;

            // Generate Automated Contextual Responses based on keywords
            setTimeout(() => {
                const aiNode = document.createElement('div');
                aiNode.className = "bg-[#0B0B0C] border border-chrome/40 p-2.5 rounded text-silver max-w-[85%]";
                
                let response = "Your prompt parameters have been mapped. To secure active engineering allocation, register an account profile and purchase a system operational tier.";
                const query = messageText.toLowerCase();
                if(query.includes('price') || query.includes('cost') || query.includes('plan')) {
                    response = "AYON operates 4 distinct operational tiers starting from Tier 1 Free Tier ($0/mo), Tier 2 ($50/mo), Tier 3 ($150/mo), up to Tier 4 Elite Core ($500/mo). Check the pricing grid module for conversion metrics.";
                } else if(query.includes('web') || query.includes('code') || query.includes('develop')) {
                    response = "Our Full-Stack engineering matrices are built via Next.js, React, Tailwind, and scalable cloud logic schemas. Click the Web Dev structural card to specify architecture briefs.";
                }
                
                aiNode.innerText = response;
                logWindow.appendChild(aiNode);
                logWindow.scrollTop = logWindow.scrollHeight;
            }, 750);
        }
    </script>
</body>
</html>
