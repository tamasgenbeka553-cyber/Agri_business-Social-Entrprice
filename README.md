<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agribusiness Social Enterprise System | Showcase & Dashboard</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0fdf4',
                            100: '#dcfce7',
                            200: '#bbf7d0',
                            500: '#22c55e',
                            600: '#16a34a',
                            700: '#15803d',
                            800: '#166534',
                            900: '#14532d',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- Lucide Icons CDN -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Google Font Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .glass-panel {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
        }
        .active-tab {
            border-bottom: 2px solid #16a34a;
            color: #15803d;
            font-weight: 600;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased selection:bg-brand-100 selection:text-brand-800">

    <!-- Toast Notification Container -->
    <div id="toast-container" class="fixed bottom-5 right-5 z-50 flex flex-col gap-2 pointer-events-none"></div>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 w-full glass-panel border-b border-slate-200/80 shadow-sm transition-all">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="h-10 w-10 rounded-xl bg-gradient-to-br from-brand-500 to-emerald-700 flex items-center justify-center text-white shadow-md shadow-brand-500/20">
                    <i data-lucide="sprout" class="w-6 h-6"></i>
                </div>
                <div>
                    <span class="font-bold text-lg text-slate-900 tracking-tight block leading-none">AgriEnterprise</span>
                    <span class="text-[10px] text-brand-700 font-semibold uppercase tracking-wider">Social System</span>
                </div>
            </div>

            <!-- Desktop Nav -->
            <nav class="hidden md:flex items-center gap-8 text-sm font-medium text-slate-600">
                <a href="#overview" class="hover:text-brand-700 transition-colors">Overview</a>
                <a href="#value-chain" class="hover:text-brand-700 transition-colors">Value Chain</a>
                <a href="#calculator" class="hover:text-brand-700 transition-colors">Impact Simulator</a>
                <a href="#profile" class="hover:text-brand-700 transition-colors">Founder Profile</a>
            </nav>

            <div class="flex items-center gap-3">
                <a href="#contact" class="hidden sm:inline-flex items-center gap-2 px-4 py-2 text-xs font-semibold text-white bg-brand-700 hover:bg-brand-800 rounded-xl shadow-sm transition-all hover:shadow hover:-translate-y-0.5">
                    <i data-lucide="mail" class="w-3.5 h-3.5"></i>
                    Get in Touch
                </a>
                <!-- Mobile menu button -->
                <button id="mobile-menu-btn" class="md:hidden p-2 rounded-lg text-slate-600 hover:bg-slate-100 focus:outline-none">
                    <i data-lucide="menu" class="w-6 h-6"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Navigation Menu -->
        <div id="mobile-menu" class="hidden md:hidden border-b border-slate-200 bg-white px-4 pt-2 pb-4 space-y-2">
            <a href="#overview" class="mobile-nav-link block px-3 py-2 rounded-lg text-slate-700 hover:bg-brand-50 font-medium">Overview</a>
            <a href="#value-chain" class="mobile-nav-link block px-3 py-2 rounded-lg text-slate-700 hover:bg-brand-50 font-medium">Value Chain</a>
            <a href="#calculator" class="mobile-nav-link block px-3 py-2 rounded-lg text-slate-700 hover:bg-brand-50 font-medium">Impact Simulator</a>
            <a href="#profile" class="mobile-nav-link block px-3 py-2 rounded-lg text-slate-700 hover:bg-brand-50 font-medium">Founder Profile</a>
        </div>
    </header>

    <!-- Main Container -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-16">

        <!-- Hero Section -->
        <section class="relative overflow-hidden rounded-3xl bg-gradient-to-br from-slate-900 via-slate-800 to-emerald-950 text-white p-8 sm:p-12 lg:p-16 shadow-xl">
            <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#22c55e_1px,transparent_1px)] [background-size:16px_16px]"></div>
            
            <div class="relative z-10 grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-7 space-y-6">
                    <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-emerald-500/10 border border-emerald-500/30 text-emerald-400 text-xs font-semibold uppercase tracking-wider backdrop-blur-md">
                        <span class="flex h-2 w-2 rounded-full bg-emerald-400 animate-pulse"></span>
                        Sustainable Agriculture Initiative
                    </div>
                    
                    <h1 class="text-3xl sm:text-4xl lg:text-5xl font-extrabold tracking-tight text-white leading-tight">
                        Transforming Agri-Ecosystems via <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-300">Social Enterprise</span>
                    </h1>

                    <p class="text-slate-300 text-base sm:text-lg leading-relaxed max-w-2xl">
                        An integrated business framework applying commercial strategy to agriculture—balancing financial growth with sustainable rural development, environmental preservation, and direct smallholder empowerment.
                    </p>

                    <div class="flex flex-wrap gap-4 pt-2">
                        <a href="#calculator" class="inline-flex items-center gap-2 px-6 py-3 rounded-xl bg-emerald-600 hover:bg-emerald-500 text-white font-semibold text-sm transition-all shadow-lg shadow-emerald-900/40 hover:-translate-y-0.5">
                            <i data-lucide="calculator" class="w-4 h-4"></i>
                            Try Impact Simulator
                        </a>
                        <a href="#profile" class="inline-flex items-center gap-2 px-6 py-3 rounded-xl bg-slate-800/80 hover:bg-slate-700 text-slate-200 border border-slate-700 font-semibold text-sm transition-all">
                            <i data-lucide="user" class="w-4 h-4"></i>
                            Founder Showcase
                        </a>
                    </div>
                </div>

                <!-- Highlight Card in Hero -->
                <div class="lg:col-span-5">
                    <div class="rounded-2xl border border-emerald-500/20 bg-slate-800/60 backdrop-blur-md p-6 shadow-2xl space-y-4">
                        <div class="flex items-center justify-between border-b border-slate-700/60 pb-3">
                            <span class="text-xs font-semibold uppercase text-emerald-400 tracking-wider">Live Enterprise Blueprint</span>
                            <span class="inline-flex items-center gap-1 text-[11px] bg-emerald-500/20 text-emerald-300 px-2.5 py-0.5 rounded-full border border-emerald-500/30">
                                <i data-lucide="check-circle-2" class="w-3 h-3"></i> Verified Model
                            </span>
                        </div>

                        <h3 class="text-lg font-bold text-white">Agribusiness Social Enterprise System</h3>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            An innovative business model and operational framework that applies commercial business strategies to agriculture while prioritizing <strong class="text-emerald-300 font-semibold">social, environmental, and economic impact</strong> over pure profit maximization.
                        </p>

                        <div class="grid grid-cols-3 gap-2 pt-2 text-center">
                            <div class="p-2.5 rounded-xl bg-slate-900/60 border border-slate-700/50">
                                <div class="text-lg font-bold text-emerald-400">🤝</div>
                                <div class="text-[11px] text-slate-400 mt-1 font-medium">Social</div>
                            </div>
                            <div class="p-2.5 rounded-xl bg-slate-900/60 border border-slate-700/50">
                                <div class="text-lg font-bold text-emerald-400">🌱</div>
                                <div class="text-[11px] text-slate-400 mt-1 font-medium">Eco</div>
                            </div>
                            <div class="p-2.5 rounded-xl bg-slate-900/60 border border-slate-700/50">
                                <div class="text-lg font-bold text-emerald-400">📈</div>
                                <div class="text-[11px] text-slate-400 mt-1 font-medium">Economic</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Dynamic Impact Metrics Counter -->
        <section id="overview" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
            <div class="bg-white rounded-2xl p-6 border border-slate-200/80 shadow-sm hover:shadow-md transition-all flex items-center gap-4">
                <div class="p-3.5 rounded-2xl bg-emerald-50 text-emerald-600 border border-emerald-100">
                    <i data-lucide="users" class="w-7 h-7"></i>
                </div>
                <div>
                    <div class="text-2xl sm:text-3xl font-extrabold text-slate-900" id="counter-farmers">0</div>
                    <div class="text-xs font-medium text-slate-500 uppercase tracking-wide mt-0.5">Smallholders Impacted</div>
                </div>
            </div>

            <div class="bg-white rounded-2xl p-6 border border-slate-200/80 shadow-sm hover:shadow-md transition-all flex items-center gap-4">
                <div class="p-3.5 rounded-2xl bg-teal-50 text-teal-600 border border-teal-100">
                    <i data-lucide="trending-up" class="w-7 h-7"></i>
                </div>
                <div>
                    <div class="text-2xl sm:text-3xl font-extrabold text-slate-900" id="counter-income">+0%</div>
                    <div class="text-xs font-medium text-slate-500 uppercase tracking-wide mt-0.5">Average Income Rise</div>
                </div>
            </div>

            <div class="bg-white rounded-2xl p-6 border border-slate-200/80 shadow-sm hover:shadow-md transition-all flex items-center gap-4">
                <div class="p-3.5 rounded-2xl bg-green-50 text-green-600 border border-green-100">
                    <i data-lucide="leaf" class="w-7 h-7"></i>
                </div>
                <div>
                    <div class="text-2xl sm:text-3xl font-extrabold text-slate-900" id="counter-co2">0</div>
                    <div class="text-xs font-medium text-slate-500 uppercase tracking-wide mt-0.5">Tons CO₂ Offset/Yr</div>
                </div>
            </div>

            <div class="bg-white rounded-2xl p-6 border border-slate-200/80 shadow-sm hover:shadow-md transition-all flex items-center gap-4">
                <div class="p-3.5 rounded-2xl bg-amber-50 text-amber-600 border border-amber-100">
                    <i data-lucide="shield-check" class="w-7 h-7"></i>
                </div>
                <div>
                    <div class="text-2xl sm:text-3xl font-extrabold text-slate-900" id="counter-yield">0%</div>
                    <div class="text-xs font-medium text-slate-500 uppercase tracking-wide mt-0.5">Post-Harvest Loss Reduction</div>
                </div>
            </div>
        </section>

        <!-- Interactive Value Chain Explorer -->
        <section id="value-chain" class="space-y-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between gap-4">
                <div>
                    <div class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-brand-50 text-brand-700 text-xs font-semibold">
                        <i data-lucide="layers" class="w-3.5 h-3.5"></i> End-to-End Architecture
                    </div>
                    <h2 class="text-2xl sm:text-3xl font-bold text-slate-900 mt-2">Agri-Social Value Chain Explorer</h2>
                    <p class="text-slate-600 text-sm mt-1 max-w-xl">
                        Click through pillars or filter by enterprise goals to inspect components across the sustainable agricultural lifecycle.
                    </p>
                </div>

                <!-- Pillar Filter Buttons -->
                <div class="flex flex-wrap gap-2 bg-slate-100 p-1.5 rounded-xl self-start">
                    <button onclick="filterPillars('all')" class="pillar-btn px-3 py-1.5 text-xs font-medium rounded-lg transition-all bg-white text-slate-800 shadow-sm" data-filter="all">
                        All Pillars
                    </button>
                    <button onclick="filterPillars('social')" class="pillar-btn px-3 py-1.5 text-xs font-medium rounded-lg text-slate-600 hover:text-slate-900 transition-all" data-filter="social">
                        🤝 Social
                    </button>
                    <button onclick="filterPillars('eco')" class="pillar-btn px-3 py-1.5 text-xs font-medium rounded-lg text-slate-600 hover:text-slate-900 transition-all" data-filter="eco">
                        🌱 Environmental
                    </button>
                    <button onclick="filterPillars('market')" class="pillar-btn px-3 py-1.5 text-xs font-medium rounded-lg text-slate-600 hover:text-slate-900 transition-all" data-filter="market">
                        📈 Market
                    </button>
                </div>
            </div>

            <!-- Value Chain Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="value-chain-grid">
                
                <!-- Stage 1 -->
                <div class="chain-card bg-white rounded-2xl border border-slate-200/80 p-6 shadow-sm hover:shadow-md transition-all flex flex-col justify-between" data-tags="social eco">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="w-8 h-8 rounded-xl bg-brand-100 text-brand-700 font-bold text-xs flex items-center justify-center">01</span>
                            <span class="inline-flex items-center gap-1 text-[11px] font-semibold bg-emerald-50 text-emerald-700 px-2 py-0.5 rounded-md">
                                🌱 Inputs & Skill
                            </span>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">Inputs & Capacity Building</h3>
                        <p class="text-xs text-slate-600 leading-relaxed mb-4">
                            Distributing climate-resilient organic seeds, bio-fertilizers, and delivering regenerative agricultural training to local smallholders.
                        </p>
                    </div>
                    <div class="pt-3 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                        <span>Impact Focus</span>
                        <span class="text-brand-700 font-semibold">Agronomic Training</span>
                    </div>
                </div>

                <!-- Stage 2 -->
                <div class="chain-card bg-white rounded-2xl border border-slate-200/80 p-6 shadow-sm hover:shadow-md transition-all flex flex-col justify-between" data-tags="social market">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="w-8 h-8 rounded-xl bg-teal-100 text-teal-700 font-bold text-xs flex items-center justify-center">02</span>
                            <span class="inline-flex items-center gap-1 text-[11px] font-semibold bg-teal-50 text-teal-700 px-2 py-0.5 rounded-md">
                                🤝 Grouping
                            </span>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">Farm Production & Co-ops</h3>
                        <p class="text-xs text-slate-600 leading-relaxed mb-4">
                            Aggregating small farmers into cooperatives to achieve economies of scale, standardizing crop quality, and protecting water sheds.
                        </p>
                    </div>
                    <div class="pt-3 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                        <span>Impact Focus</span>
                        <span class="text-teal-700 font-semibold">Scale & Synergy</span>
                    </div>
                </div>

                <!-- Stage 3 -->
                <div class="chain-card bg-white rounded-2xl border border-slate-200/80 p-6 shadow-sm hover:shadow-md transition-all flex flex-col justify-between" data-tags="eco market">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="w-8 h-8 rounded-xl bg-amber-100 text-amber-700 font-bold text-xs flex items-center justify-center">03</span>
                            <span class="inline-flex items-center gap-1 text-[11px] font-semibold bg-amber-50 text-amber-700 px-2 py-0.5 rounded-md">
                                ⚙️ Value Addition
                            </span>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">Processing & Cold Chain</h3>
                        <p class="text-xs text-slate-600 leading-relaxed mb-4">
                            Utilizing solar-powered cold storage and localized processing (milling, drying) to reduce post-harvest waste and retain product value.
                        </p>
                    </div>
                    <div class="pt-3 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                        <span>Impact Focus</span>
                        <span class="text-amber-700 font-semibold">Loss Reduction</span>
                    </div>
                </div>

                <!-- Stage 4 -->
                <div class="chain-card bg-white rounded-2xl border border-slate-200/80 p-6 shadow-sm hover:shadow-md transition-all flex flex-col justify-between" data-tags="market social">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="w-8 h-8 rounded-xl bg-blue-100 text-blue-700 font-bold text-xs flex items-center justify-center">04</span>
                            <span class="inline-flex items-center gap-1 text-[11px] font-semibold bg-blue-50 text-blue-700 px-2 py-0.5 rounded-md">
                                📈 Market Access
                            </span>
                        </div>
                        <h3 class="text-lg font-bold text-slate-900 mb-2">Fair Market & Finance</h3>
                        <p class="text-xs text-slate-600 leading-relaxed mb-4">
                            Bypassing predatory middlemen to connect directly with premium buyers, while offering micro-finance and transparent digital payouts.
                        </p>
                    </div>
                    <div class="pt-3 border-t border-slate-100 flex items-center justify-between text-xs text-slate-500 font-medium">
                        <span>Impact Focus</span>
                        <span class="text-blue-700 font-semibold">Fair Profits</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- Interactive Impact & ROI Calculator -->
        <section id="calculator" class="bg-gradient-to-br from-emerald-900 via-slate-900 to-slate-900 rounded-3xl text-white p-6 sm:p-10 shadow-xl">
            <div class="max-w-4xl mx-auto space-y-8">
                <div class="text-center space-y-2">
                    <div class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-emerald-500/20 text-emerald-300 text-xs font-semibold border border-emerald-500/30">
                        <i data-lucide="sliders" class="w-3.5 h-3.5"></i> Interactive Simulator
                    </div>
                    <h2 class="text-2xl sm:text-3xl font-extrabold text-white">Social & Economic Impact Estimator</h2>
                    <p class="text-slate-300 text-xs sm:text-sm max-w-xl mx-auto">
                        Adjust the scale of smallholder farmers integrated into the system to calculate estimated crop yield expansion, income gains, and carbon reduction.
                    </p>
                </div>

                <!-- Interactive Input Controls -->
                <div class="bg-slate-800/80 backdrop-blur-md rounded-2xl p-6 border border-slate-700/60 space-y-6">
                    <div>
                        <div class="flex justify-between items-center mb-2">
                            <label for="farmer-slider" class="text-xs sm:text-sm font-semibold text-slate-200">
                                Number of Participating Smallholder Farmers:
                            </label>
                            <span class="text-lg font-bold text-emerald-400 bg-slate-900/80 px-3 py-1 rounded-lg border border-slate-700" id="slider-val-display">
                                250 Farmers
                            </span>
                        </div>
                        <input type="range" id="farmer-slider" min="20" max="2500" value="250" step="10" 
                               class="w-full h-2.5 bg-slate-700 rounded-lg appearance-none cursor-pointer accent-emerald-500">
                        <div class="flex justify-between text-[11px] text-slate-400 mt-1">
                            <span>20 Farmers</span>
                            <span>1,000</span>
                            <span>2,500 Farmers</span>
                        </div>
                    </div>

                    <!-- Crop Type Selector -->
                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-3 pt-2">
                        <button onclick="setCropType('grains')" class="crop-btn p-3 rounded-xl border border-emerald-500 bg-emerald-500/20 text-white text-left transition-all" data-crop="grains">
                            <div class="text-xs font-bold">🌾 Grains & Cereals</div>
                            <div class="text-[10px] text-slate-300 mt-0.5">High volume, community staple</div>
                        </button>
                        <button onclick="setCropType('coffee')" class="crop-btn p-3 rounded-xl border border-slate-700 bg-slate-900/50 text-slate-300 text-left hover:border-slate-600 transition-all" data-crop="coffee">
                            <div class="text-xs font-bold">☕ Specialty Coffee / Cocoa</div>
                            <div class="text-[10px] text-slate-400 mt-0.5">High premium export crop</div>
                        </button>
                        <button onclick="setCropType('horticulture')" class="crop-btn p-3 rounded-xl border border-slate-700 bg-slate-900/50 text-slate-300 text-left hover:border-slate-600 transition-all" data-crop="horticulture">
                            <div class="text-xs font-bold">🥦 Fresh Horticulture</div>
                            <div class="text-[10px] text-slate-400 mt-0.5">Fast rotation, cold-chain dependent</div>
                        </button>
                    </div>
                </div>

                <!-- Simulation Output Cards -->
                <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                    <div class="bg-slate-800/50 border border-slate-700/60 rounded-2xl p-5 text-center">
                        <div class="text-xs text-slate-400 font-medium uppercase tracking-wider mb-1">Est. Community Revenue Increase</div>
                        <div class="text-2xl sm:text-3xl font-extrabold text-emerald-400" id="est-revenue">$87,500</div>
                        <div class="text-[11px] text-slate-400 mt-1">Directly into farmer households</div>
                    </div>

                    <div class="bg-slate-800/50 border border-slate-700/60 rounded-2xl p-5 text-center">
                        <div class="text-xs text-slate-400 font-medium uppercase tracking-wider mb-1">Annual Yield Expansion</div>
                        <div class="text-2xl sm:text-3xl font-extrabold text-teal-300" id="est-yield">312 Tons</div>
                        <div class="text-[11px] text-slate-400 mt-1">Through sustainable practices</div>
                    </div>

                    <div class="bg-slate-800/50 border border-slate-700/60 rounded-2xl p-5 text-center">
                        <div class="text-xs text-slate-400 font-medium uppercase tracking-wider mb-1">Carbon Offset Equivalent</div>
                        <div class="text-2xl sm:text-3xl font-extrabold text-green-400" id="est-co2">187 Tons</div>
                        <div class="text-[11px] text-slate-400 mt-1">Soil sequestration & organic inputs</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Developer & Founder Profile Showcase Section -->
        <section id="profile" class="space-y-8">
            <div class="text-center max-w-2xl mx-auto space-y-2">
                <div class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-brand-50 text-brand-700 text-xs font-semibold">
                    <i data-lucide="user-check" class="w-3.5 h-3.5"></i> Founder & Visionary
                </div>
                <h2 class="text-2xl sm:text-3xl font-bold text-slate-900">Developer & Founder Showcase</h2>
                <p class="text-slate-600 text-sm">
                    Connecting tech innovation with sustainable agri-social transformation.
                </p>
            </div>

            <!-- Profile Card -->
            <div class="max-w-3xl mx-auto bg-white rounded-3xl border border-slate-200/80 shadow-md overflow-hidden">
                <div class="h-32 bg-gradient-to-r from-emerald-800 via-brand-700 to-teal-800 relative">
                    <div class="absolute inset-0 opacity-15 bg-[radial-gradient(#ffffff_1px,transparent_1px)] [background-size:12px_12px]"></div>
                </div>
                
                <div class="px-6 sm:px-8 pb-8 relative">
                    <!-- Avatar & Header info -->
                    <div class="flex flex-col sm:flex-row sm:items-end justify-between -mt-16 mb-6 gap-4">
                        <div class="flex items-end gap-4">
                            <div class="h-28 w-28 rounded-2xl bg-white p-1.5 shadow-lg border border-slate-100 flex-shrink-0">
                                <div class="w-full h-full rounded-xl bg-gradient-to-tr from-brand-600 to-emerald-800 flex items-center justify-center text-white text-3xl font-bold">
                                    TB
                                </div>
                            </div>
                            <div class="mb-1">
                                <h3 class="text-2xl font-bold text-slate-900">Tamasgen Beka</h3>
                                <p class="text-xs font-semibold text-brand-700">Agri-Tech Developer & System Architect</p>
                            </div>
                        </div>

                        <!-- Action Badges -->
                        <div class="flex items-center gap-2">
                            <span class="inline-flex items-center gap-1 px-3 py-1 rounded-full text-xs font-semibold bg-emerald-50 text-emerald-700 border border-emerald-200">
                                <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
                                Available for Collaboration
                            </span>
                        </div>
                    </div>

                    <!-- Bio -->
                    <div class="space-y-4">
                        <p class="text-sm text-slate-600 leading-relaxed">
                            Dedicated to designing sustainable agribusiness solutions, digital platforms, and social enterprise models that empower agricultural communities and drive climate-resilient economic growth.
                        </p>

                        <!-- Contact Metadata Box -->
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 p-4 rounded-2xl bg-slate-50 border border-slate-200/70">
                            <div class="flex items-center gap-3">
                                <div class="p-2.5 rounded-xl bg-white text-slate-700 shadow-sm border border-slate-200">
                                    <i data-lucide="mail" class="w-4 h-4"></i>
                                </div>
                                <div class="overflow-hidden">
                                    <div class="text-[10px] font-semibold uppercase text-slate-400">Primary Email</div>
                                    <a href="mailto:tamasgenbeka553@gmail.com" class="text-xs font-medium text-slate-800 hover:text-brand-700 truncate block">
                                        tamasgenbeka553@gmail.com
                                    </a>
                                </div>
                            </div>

                            <div class="flex items-center gap-3">
                                <div class="p-2.5 rounded-xl bg-white text-slate-700 shadow-sm border border-slate-200">
                                    <i data-lucide="github" class="w-4 h-4"></i>
                                </div>
                                <div class="overflow-hidden">
                                    <div class="text-[10px] font-semibold uppercase text-slate-400">GitHub Profile</div>
                                    <a href="https://github.com/bekamtamasgen6-svg" target="_blank" rel="noopener noreferrer" class="text-xs font-medium text-slate-800 hover:text-brand-700 truncate block">
                                        github.com/bekamtamasgen6-svg
                                    </a>
                                </div>
                            </div>
                        </div>

                        <!-- Action Buttons -->
                        <div class="flex flex-wrap gap-3 pt-2">
                            <a href="mailto:tamasgenbeka553@gmail.com" class="flex-1 sm:flex-none inline-flex items-center justify-center gap-2 px-5 py-2.5 rounded-xl bg-brand-700 hover:bg-brand-800 text-white text-xs font-semibold shadow-sm transition-all hover:shadow">
                                <i data-lucide="send" class="w-3.5 h-3.5"></i>
                                Send Email
                            </a>
                            <a href="https://github.com/bekamtamasgen6-svg" target="_blank" rel="noopener noreferrer" class="flex-1 sm:flex-none inline-flex items-center justify-center gap-2 px-5 py-2.5 rounded-xl bg-slate-900 hover:bg-slate-800 text-white text-xs font-semibold shadow-sm transition-all">
                                <i data-lucide="github" class="w-3.5 h-3.5"></i>
                                Visit GitHub Profile
                            </a>
                            <button onclick="copyContactInfo()" class="flex-1 sm:flex-none inline-flex items-center justify-center gap-2 px-5 py-2.5 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-semibold transition-all">
                                <i data-lucide="copy" class="w-3.5 h-3.5"></i>
                                Copy Contact Info
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Interactive Contact & Feedback Form Section -->
        <section id="contact" class="max-w-2xl mx-auto bg-white rounded-3xl border border-slate-200/80 p-6 sm:p-8 shadow-md">
            <div class="space-y-4 mb-6">
                <h3 class="text-xl font-bold text-slate-900 flex items-center gap-2">
                    <i data-lucide="message-square" class="w-5 h-5 text-brand-700"></i>
                    Enterprise Feedback & Inquiry Form
                </h3>
                <p class="text-xs text-slate-600">
                    Interested in partnering, investing, or exploring agribusiness models? Leave a message below.
                </p>
            </div>

            <form id="inquiry-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label for="form-name" class="block text-xs font-semibold text-slate-700 mb-1">Your Name</label>
                        <input type="text" id="form-name" required placeholder="e.g. Alex Morgan" 
                               class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-xs text-slate-800 focus:outline-none focus:ring-2 focus:ring-brand-500 focus:border-brand-500">
                    </div>
                    <div>
                        <label for="form-email" class="block text-xs font-semibold text-slate-700 mb-1">Your Email</label>
                        <input type="email" id="form-email" required placeholder="alex@example.com" 
                               class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-xs text-slate-800 focus:outline-none focus:ring-2 focus:ring-brand-500 focus:border-brand-500">
                    </div>
                </div>

                <div>
                    <label for="form-subject" class="block text-xs font-semibold text-slate-700 mb-1">Inquiry Type</label>
                    <select id="form-subject" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-xs text-slate-800 focus:outline-none focus:ring-2 focus:ring-brand-500 focus:border-brand-500">
                        <option value="Collaboration">Agri-Enterprise Partnership</option>
                        <option value="Investment">Social Impact Investment</option>
                        <option value="Tech Inquiry">Agri-Tech Development Query</option>
                        <option value="General">General Feedback</option>
                    </select>
                </div>

                <div>
                    <label for="form-message" class="block text-xs font-semibold text-slate-700 mb-1">Message</label>
                    <textarea id="form-message" rows="4" required placeholder="Describe your project, question, or collaboration opportunity..." 
                              class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-xs text-slate-800 focus:outline-none focus:ring-2 focus:ring-brand-500 focus:border-brand-500"></textarea>
                </div>

                <button type="submit" class="w-full py-3 px-4 rounded-xl bg-brand-700 hover:bg-brand-800 text-white font-semibold text-xs transition-all shadow-sm flex items-center justify-center gap-2">
                    <i data-lucide="send" class="w-4 h-4"></i>
                    Send Message
                </button>
            </form>
        </section>

    </main>

    <!-- Footer -->
    <footer class="border-t border-slate-200 bg-white py-8 mt-16 text-center text-xs text-slate-500">
        <div class="max-w-7xl mx-auto px-4 space-y-2">
            <p>© 2026 Agribusiness Social Enterprise System. Developed by <strong>Tamasgen Beka</strong>.</p>
            <p class="text-slate-400">Empowering smallholders • Preserving Ecosystems • Building Market Resilience</p>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('.mobile-nav-link').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Dynamic Counters Animation
        function animateCounters() {
            const targets = {
                farmers: { element: document.getElementById('counter-farmers'), target: 1250, suffix: '+' },
                income: { element: document.getElementById('counter-income'), target: 45, prefix: '+', suffix: '%' },
                co2: { element: document.getElementById('counter-co2'), target: 820, suffix: ' T' },
                yield: { element: document.getElementById('counter-yield'), target: 35, suffix: '%' }
            };

            const duration = 1500;
            const steps = 40;
            const stepTime = duration / steps;

            let currentStep = 0;

            const timer = setInterval(() => {
                currentStep++;
                const progress = currentStep / steps;

                for (const key in targets) {
                    const item = targets[key];
                    const currentValue = Math.floor(item.target * progress);
                    const prefix = item.prefix || '';
                    const suffix = item.suffix || '';
                    item.element.textContent = `${prefix}${currentValue.toLocaleString()}${suffix}`;
                }

                if (currentStep >= steps) {
                    clearInterval(timer);
                }
            }, stepTime);
        }

        // Start animation on load
        window.addEventListener('DOMContentLoaded', animateCounters);

        // Pillar Filter Functionality
        function filterPillars(category) {
            const cards = document.querySelectorAll('.chain-card');
            const buttons = document.querySelectorAll('.pillar-btn');

            buttons.forEach(btn => {
                if (btn.getAttribute('data-filter') === category) {
                    btn.className = 'pillar-btn px-3 py-1.5 text-xs font-medium rounded-lg transition-all bg-white text-slate-800 shadow-sm';
                } else {
                    btn.className = 'pillar-btn px-3 py-1.5 text-xs font-medium rounded-lg text-slate-600 hover:text-slate-900 transition-all';
                }
            });

            cards.forEach(card => {
                const tags = card.getAttribute('data-tags');
                if (category === 'all' || tags.includes(category)) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Calculator State & Logic
        let currentCropMultiplier = { revenue: 350, yield: 1.25, co2: 0.75 };

        const farmerSlider = document.getElementById('farmer-slider');
        const sliderValDisplay = document.getElementById('slider-val-display');

        function updateCalculator() {
            const farmers = parseInt(farmerSlider.value);
            sliderValDisplay.textContent = `${farmers.toLocaleString()} Farmers`;

            const estRevenue = Math.round(farmers * currentCropMultiplier.revenue);
            const estYield = Math.round(farmers * currentCropMultiplier.yield);
            const estCo2 = Math.round(farmers * currentCropMultiplier.co2);

            document.getElementById('est-revenue').textContent = `$${estRevenue.toLocaleString()}`;
            document.getElementById('est-yield').textContent = `${estYield.toLocaleString()} Tons`;
            document.getElementById('est-co2').textContent = `${estCo2.toLocaleString()} Tons`;
        }

        farmerSlider.addEventListener('input', updateCalculator);

        function setCropType(crop) {
            const cropButtons = document.querySelectorAll('.crop-btn');
            
            cropButtons.forEach(btn => {
                if (btn.getAttribute('data-crop') === crop) {
                    btn.className = 'crop-btn p-3 rounded-xl border border-emerald-500 bg-emerald-500/20 text-white text-left transition-all';
                } else {
                    btn.className = 'crop-btn p-3 rounded-xl border border-slate-700 bg-slate-900/50 text-slate-300 text-left hover:border-slate-600 transition-all';
                }
            });

            if (crop === 'grains') {
                currentCropMultiplier = { revenue: 350, yield: 1.25, co2: 0.75 };
            } else if (crop === 'coffee') {
                currentCropMultiplier = { revenue: 780, yield: 0.85, co2: 1.15 };
            } else if (crop === 'horticulture') {
                currentCropMultiplier = { revenue: 520, yield: 1.80, co2: 0.50 };
            }

            updateCalculator();
        }

        // Toast Notification System
        function showToast(message, type = 'success') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            toast.className = `pointer-events-auto flex items-center gap-2 px-4 py-3 rounded-xl text-xs font-semibold text-white shadow-lg transition-all transform translate-y-2 opacity-0 ${
                type === 'success' ? 'bg-emerald-700' : 'bg-slate-800'
            }`;
            
            toast.innerHTML = `<i data-lucide="${type === 'success' ? 'check-circle' : 'info'}" class="w-4 h-4"></i> ${message}`;
            
            container.appendChild(toast);
            lucide.createIcons();

            setTimeout(() => {
                toast.classList.remove('translate-y-2', 'opacity-0');
            }, 10);

            setTimeout(() => {
                toast.classList.add('opacity-0', 'translate-y-2');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }

        // Copy Contact Information
        function copyContactInfo() {
            const contactText = "Name: Tamasgen Beka\nEmail: tamasgenbeka553@gmail.com\nGitHub: https://github.com/bekamtamasgen6-svg";
            
            // execCommand fallback for strict iFrame execution
            const dummy = document.createElement("textarea");
            document.body.appendChild(dummy);
            dummy.value = contactText;
            dummy.select();
            document.execCommand("copy");
            document.body.removeChild(dummy);

            showToast("Contact details copied to clipboard!");
        }

        // Handle Inquiry Form Submission
        function handleFormSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('form-name').value;
            const subject = document.getElementById('form-subject').value;

            showToast(`Thank you, ${name}! Your inquiry regarding '${subject}' has been submitted.`);
            document.getElementById('inquiry-form').reset();
        }

        // Initial setup run
        updateCalculator();
    </script>
</body>
</html>
---

### 🤝 Connect with Me
- 📧 **Email:** bekamtamasgen6@gmail.com
- 💻 **GitHub:** [github.com/bekamtamasgen6-svg](https://github.com/bekamtamasgen6-svg)

_“Building software to empower communities and advance technology.”_
