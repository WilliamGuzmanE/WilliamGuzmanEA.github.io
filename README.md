<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>William Guzman | Rutgers Senior Finance Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        rutgers: {
                            DEFAULT: '#CC0033',
                            dark: '#990026',
                            light: '#ff3366',
                            subtle: '#fff5f7'
                        },
                        slate: {
                            850: '#151f32',
                            950: '#0b0f19'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        mono: ['JetBrains Mono', 'monospace'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(226, 232, 240, 0.8);
        }
        .dark .glass-card {
            background: rgba(15, 23, 42, 0.85);
            border: 1px solid rgba(51, 65, 85, 0.5);
        }
        .rutgers-gradient {
            background: linear-gradient(135deg, #CC0033 0%, #800020 100%);
        }
        .rutgers-text-gradient {
            background: linear-gradient(135deg, #CC0033 0%, #e60039 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        /* Custom range slider styling */
        input[type=range] {
            -webkit-appearance: none;
            width: 100%;
            background: #e2e8f0;
            height: 6px;
            border-radius: 3px;
            outline: none;
        }
        input[type=range]::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #CC0033;
            cursor: pointer;
            transition: all 0.15s ease;
            box-shadow: 0 2px 4px rgba(204, 0, 51, 0.3);
        }
        input[type=range]::-webkit-slider-thumb:hover {
            transform: scale(1.15);
            background: #990026;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased selection:bg-rutgers selection:text-white min-h-screen flex flex-col justify-between">

    <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-slate-200/80 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <!-- Brand Logo -->
                <a href="#" class="flex items-center space-x-3 group">
                    <div class="w-10 h-10 rounded-lg rutgers-gradient flex items-center justify-center text-white font-extrabold text-xl shadow-md group-hover:scale-105 transition-transform">
                        R
                    </div>
                    <div>
                        <span class="font-bold text-lg tracking-tight text-slate-900 block leading-tight">William Guzman</span>
                        <span class="text-xs font-medium text-rutgers block leading-none">Rutgers Finance '25</span>
                    </div>
                </a>

                <!-- Desktop Navigation -->
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="#about" class="text-sm font-medium text-slate-600 hover:text-rutgers transition-colors">About</a>
                    <a href="#skills" class="text-sm font-medium text-slate-600 hover:text-rutgers transition-colors">Skills</a>
                    <a href="#projects" class="text-sm font-medium text-slate-600 hover:text-rutgers transition-colors">Projects</a>
                    <a href="#dcf-tool" class="text-sm font-medium text-slate-600 hover:text-rutgers transition-colors">Valuation Tool</a>
                    <a href="#contact" class="inline-flex items-center justify-center px-4 py-2 rounded-lg text-sm font-semibold text-white rutgers-gradient hover:opacity-95 transition-all shadow-sm">Contact Me</a>
                </nav>

                <!-- Mobile Menu Button -->
                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="p-2 rounded-lg text-slate-600 hover:text-slate-900 hover:bg-slate-100 focus:outline-none">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path id="menu-icon" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Navigation Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-4 space-y-2">
            <a href="#about" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:bg-rutgers-subtle hover:text-rutgers">About</a>
            <a href="#skills" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:bg-rutgers-subtle hover:text-rutgers">Skills</a>
            <a href="#projects" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:bg-rutgers-subtle hover:text-rutgers">Projects</a>
            <a href="#dcf-tool" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:bg-rutgers-subtle hover:text-rutgers">Valuation Tool</a>
            <a href="#contact" class="block px-3 py-2 rounded-md text-base font-medium text-white rutgers-gradient text-center">Contact Me</a>
        </div>
    </header>

    <main class="flex-grow">
        <section id="about" class="relative py-20 lg:py-28 overflow-hidden bg-gradient-to-b from-slate-100/70 to-slate-50 border-b border-slate-200/60">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
                <div class="grid md:grid-cols-12 gap-12 items-center">
                    <div class="md:col-span-7 space-y-6 text-left">
                        <div class="inline-flex items-center space-x-2 px-3 py-1.5 rounded-full bg-rutgers/10 border border-rutgers/20 text-rutgers font-semibold text-xs tracking-wide uppercase">
                            <span class="w-2 h-2 rounded-full bg-rutgers animate-pulse"></span>
                            <span>Rutgers Business School • Finance Senior</span>
                        </div>
                        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-slate-900 tracking-tight leading-tight">
                            Hi, I'm <span class="rutgers-text-gradient">William Guzman</span>
                        </h1>
                        <p class="text-lg sm:text-xl text-slate-600 leading-relaxed max-w-2xl">
                            A senior Finance major at Rutgers University leveraging quantitative analysis, financial modeling, and data analytics to deliver strategic insights and investment value.
                        </p>
                        <div class="pt-2 flex flex-wrap gap-4 items-center">
                            <a href="#dcf-tool" class="px-6 py-3 rounded-lg text-white font-semibold rutgers-gradient hover:shadow-lg transition-all shadow-md">
                                Try DCF Valuation Tool
                            </a>
                            <a href="#projects" class="px-6 py-3 rounded-lg bg-white border border-slate-300 text-slate-700 font-semibold hover:bg-slate-50 hover:border-slate-400 transition-all shadow-sm">
                                View Projects
                            </a>
                        </div>
                        <div class="pt-6 grid grid-cols-3 gap-4 border-t border-slate-200/80 max-w-lg">
                            <div>
                                <p class="text-2xl font-bold text-slate-900">3.8+</p>
                                <p class="text-xs text-slate-500 font-medium">Finance GPA</p>
                            </div>
                            <div>
                                <p class="text-2xl font-bold text-slate-900">3+</p>
                                <p class="text-xs text-slate-500 font-medium">Valuation Projects</p>
                            </div>
                            <div>
                                <p class="text-2xl font-bold text-slate-900">2025</p>
                                <p class="text-xs text-slate-500 font-medium">Graduation Year</p>
                            </div>
                        </div>
                    </div>

                    <!-- Hero Visual Card -->
                    <div class="md:col-span-5">
                        <div class="relative mx-auto max-w-md bg-white p-6 rounded-2xl shadow-xl border border-slate-200/80">
                            <div class="flex items-center justify-between border-b border-slate-100 pb-4 mb-4">
                                <div class="flex items-center space-x-3">
                                    <div class="w-12 h-12 rounded-full bg-slate-100 flex items-center justify-center font-bold text-rutgers border border-rutgers/20">
                                        WG
                                    </div>
                                    <div>
                                        <h3 class="font-bold text-slate-900 text-base">William Guzman</h3>
                                        <p class="text-xs text-slate-500">New Brunswick, NJ</p>
                                    </div>
                                </div>
                                <span class="px-2.5 py-1 text-xs font-semibold text-emerald-700 bg-emerald-50 rounded-full border border-emerald-200">
                                    Seeking Analyst Roles
                                </span>
                            </div>
                            <div class="space-y-3 text-sm">
                                <div class="flex justify-between py-1.5 border-b border-slate-50">
                                    <span class="text-slate-500">University</span>
                                    <span class="font-medium text-slate-800">Rutgers University</span>
                                </div>
                                <div class="flex justify-between py-1.5 border-b border-slate-50">
                                    <span class="text-slate-500">Major</span>
                                    <span class="font-medium text-slate-800">Finance (BS)</span>
                                </div>
                                <div class="flex justify-between py-1.5 border-b border-slate-50">
                                    <span class="text-slate-500">Core Focus</span>
                                    <span class="font-medium text-slate-800">Valuation & Equity Research</span>
                                </div>
                                <div class="flex justify-between py-1.5">
                                    <span class="text-slate-500">Key Tools</span>
                                    <span class="font-medium text-slate-800">Excel, Python, SQL, Bloomberg</span>
                                </div>
                            </div>
                            <div class="mt-5 p-3 rounded-xl bg-slate-50 border border-slate-100 text-xs text-slate-600 flex items-center justify-between">
                                <span class="flex items-center space-x-1.5">
                                    <svg class="w-4 h-4 text-rutgers" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
                                    <span>Active Bloomberg Market Concepts Certified</span>
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="py-20 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h2 class="text-xs font-bold uppercase tracking-wider text-rutgers mb-2">Core Competencies</h2>
                    <h3 class="text-3xl font-extrabold text-slate-900 sm:text-4xl">Technical & Financial Expertise</h3>
                    <p class="mt-3 text-slate-600 text-base">Comprehensive skill set acquired through rigorous academic coursework at Rutgers and practical financial analysis projects.</p>
                    
                    <!-- Skill Filters -->
                    <div class="mt-8 flex flex-wrap justify-center gap-2">
                        <button onclick="filterSkills('all')" class="skill-btn active-skill px-4 py-2 rounded-full text-xs font-semibold border transition-all bg-rutgers text-white border-rutgers" data-category="all">All Skills</button>
                        <button onclick="filterSkills('valuation')" class="skill-btn px-4 py-2 rounded-full text-xs font-semibold border transition-all bg-slate-100 text-slate-600 border-slate-200 hover:bg-slate-200" data-category="valuation">Valuation & Corporate Finance</button>
                        <button onclick="filterSkills('analytics')" class="skill-btn px-4 py-2 rounded-full text-xs font-semibold border transition-all bg-slate-100 text-slate-600 border-slate-200 hover:bg-slate-200" data-category="analytics">Analytics & Modeling</button>
                        <button onclick="filterSkills('software')" class="skill-btn px-4 py-2 rounded-full text-xs font-semibold border transition-all bg-slate-100 text-slate-600 border-slate-200 hover:bg-slate-200" data-category="software">Software & Platforms</button>
                    </div>
                </div>

                <!-- Skills Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="skills-grid">
                    <!-- Skill Card 1 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="valuation">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Financial Modeling</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">Building dynamic 3-statement models, forecasting revenue, expenses, and working capital under multi-scenario sensitivity cases.</p>
                    </div>

                    <!-- Skill Card 2 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="valuation">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">DCF & Comps Valuation</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">Performing Discounted Cash Flow valuations, WACC calculations, Trading Comps, and Precedent Transaction benchmarking.</p>
                    </div>

                    <!-- Skill Card 3 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="software">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h18M3 14h18m-9-4v8m-7 0h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Advanced MS Excel</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">Proficient with INDEX/MATCH, XLOOKUP, Pivot Tables, Scenario Manager, Data Tables, and macro automation basics.</p>
                    </div>

                    <!-- Skill Card 4 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="analytics">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Python & SQL</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">Data extraction, financial data analysis using Pandas, NumPy, and SQL queries for large dataset manipulation.</p>
                    </div>

                    <!-- Skill Card 5 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="analytics">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 17v-2m3 2v-4m3 4v-6m2 10H7a2 2 0 01-2-2V5a2 2 0 012-2h55.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Financial Analysis</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">In-depth 10-K and 10-Q SEC filing reviews, ratio analysis (DuPont, Liquidity, Solvency), and quality of earnings analysis.</p>
                    </div>

                    <!-- Skill Card 6 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="software">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Bloomberg Terminal</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">Certified in Bloomberg Market Concepts (BMC). Skilled in equity lookup, financial telemetry, and yield curve analysis.</p>
                    </div>

                    <!-- Skill Card 7 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="valuation">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5m0 0h4m-4 0V11m0 0h4m-4 0H9"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Corporate Finance</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">Evaluation of capital structures, cost of capital, dividend policy analysis, and strategic corporate decision frameworks.</p>
                    </div>

                    <!-- Skill Card 8 -->
                    <div class="skill-card p-6 bg-slate-50 rounded-xl border border-slate-200 hover:shadow-md transition-all" data-category="valuation">
                        <div class="w-10 h-10 rounded-lg bg-rutgers/10 text-rutgers flex items-center justify-center font-bold mb-4">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/></svg>
                        </div>
                        <h4 class="font-bold text-slate-900 text-lg mb-1">Capital Budgeting</h4>
                        <p class="text-xs text-slate-600 leading-relaxed">NPV, IRR, Payback Period calculation, and cash flow risk sensitivity modeling for capital expenditure assessments.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects" class="py-20 bg-slate-100 border-t border-b border-slate-200">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h2 class="text-xs font-bold uppercase tracking-wider text-rutgers mb-2">Featured Work</h2>
                    <h3 class="text-3xl font-extrabold text-slate-900 sm:text-4xl">Financial Case Studies & Models</h3>
                    <p class="mt-3 text-slate-600 text-base">In-depth financial models and research papers developed for Rutgers coursework and independent analysis.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Project Card 1 -->
                    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden flex flex-col hover:shadow-lg transition-shadow">
                        <div class="p-6 flex-grow">
                            <div class="flex items-center justify-between mb-4">
                                <span class="px-2.5 py-1 text-xs font-bold text-rutgers bg-rutgers/10 rounded-md">Valuation & DCF</span>
                                <span class="text-xs text-slate-400">Rutgers Coursework</span>
                            </div>
                            <h4 class="text-xl font-bold text-slate-900 mb-2">Rutgers Equity Valuation & DCF Model</h4>
                            <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                                A comprehensive multi-year 3-statement dynamic valuation model for a mega-cap tech sector firm. Features sensitivity tables for WACC vs Terminal Growth and Comps benchmarking.
                            </p>
                            <div class="flex flex-wrap gap-1.5 mb-6">
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">DCF</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">WACC</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Excel</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Comps</span>
                            </div>
                        </div>
                        <div class="px-6 py-4 bg-slate-50 border-t border-slate-100">
                            <button onclick="openModal('project1-modal')" class="w-full py-2 px-4 rounded-lg bg-white border border-slate-300 text-xs font-bold text-slate-700 hover:bg-slate-100 hover:border-slate-400 transition-colors flex items-center justify-center space-x-2">
                                <span>View Model Details</span>
                                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
                            </button>
                        </div>
                    </div>

                    <!-- Project Card 2 -->
                    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden flex flex-col hover:shadow-lg transition-shadow">
                        <div class="p-6 flex-grow">
                            <div class="flex items-center justify-between mb-4">
                                <span class="px-2.5 py-1 text-xs font-bold text-blue-700 bg-blue-50 rounded-md">Portfolio Analytics</span>
                                <span class="text-xs text-slate-400">Quantitative Project</span>
                            </div>
                            <h4 class="text-xl font-bold text-slate-900 mb-2">Portfolio Optimization & Risk Analysis</h4>
                            <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                                Applied Markowitz Efficient Frontier optimization using Python (Pandas/NumPy) on a 10-asset portfolio to compute maximum Sharpe ratio, asset covariance, and VaR (Value at Risk).
                            </p>
                            <div class="flex flex-wrap gap-1.5 mb-6">
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Python</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Sharpe Ratio</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Modern Portfolio Theory</span>
                            </div>
                        </div>
                        <div class="px-6 py-4 bg-slate-50 border-t border-slate-100">
                            <button onclick="openModal('project2-modal')" class="w-full py-2 px-4 rounded-lg bg-white border border-slate-300 text-xs font-bold text-slate-700 hover:bg-slate-100 hover:border-slate-400 transition-colors flex items-center justify-center space-x-2">
                                <span>View Model Details</span>
                                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
                            </button>
                        </div>
                    </div>

                    <!-- Project Card 3 -->
                    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden flex flex-col hover:shadow-lg transition-shadow">
                        <div class="p-6 flex-grow">
                            <div class="flex items-center justify-between mb-4">
                                <span class="px-2.5 py-1 text-xs font-bold text-emerald-700 bg-emerald-50 rounded-md">Corporate Analysis</span>
                                <span class="text-xs text-slate-400">Case Study</span>
                            </div>
                            <h4 class="text-xl font-bold text-slate-900 mb-2">Corporate Health & Solvency Analysis</h4>
                            <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                                Conducted 5-year SEC filing debt profile and cash flow evaluation for an industrial firm, analyzing Altman Z-Score, interest coverage, liquidity traps, and capital allocation strategy.
                            </p>
                            <div class="flex flex-wrap gap-1.5 mb-6">
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">SEC 10-K</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Altman Z-Score</span>
                                <span class="px-2 py-0.5 bg-slate-100 text-slate-600 text-xs rounded font-mono">Credit Risk</span>
                            </div>
                        </div>
                        <div class="px-6 py-4 bg-slate-50 border-t border-slate-100">
                            <button onclick="openModal('project3-modal')" class="w-full py-2 px-4 rounded-lg bg-white border border-slate-300 text-xs font-bold text-slate-700 hover:bg-slate-100 hover:border-slate-400 transition-colors flex items-center justify-center space-x-2">
                                <span>View Case Details</span>
                                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="dcf-tool" class="py-20 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h2 class="text-xs font-bold uppercase tracking-wider text-rutgers mb-2">Interactive Showcase</h2>
                    <h3 class="text-3xl font-extrabold text-slate-900 sm:text-4xl">Live DCF Valuation Calculator</h3>
                    <p class="mt-3 text-slate-600 text-base">Adjust key valuation drivers below to simulate real-time Discounted Cash Flow (DCF) enterprise enterprise values.</p>
                </div>

                <div class="max-w-5xl mx-auto bg-slate-900 rounded-2xl shadow-2xl overflow-hidden border border-slate-800 text-white">
                    <div class="p-6 bg-slate-850 border-b border-slate-800 flex flex-wrap items-center justify-between gap-4">
                        <div class="flex items-center space-x-3">
                            <div class="w-3 h-3 rounded-full bg-red-500"></div>
                            <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
                            <div class="w-3 h-3 rounded-full bg-green-500"></div>
                            <span class="text-xs font-mono text-slate-400 ml-2">DCF_Engine_v2.5.xlsx</span>
                        </div>
                        <span class="text-xs bg-rutgers/20 text-rutgers-light border border-rutgers/30 px-3 py-1 rounded-full font-mono">
                            Live Calculation Active
                        </span>
                    </div>

                    <div class="p-6 lg:p-8 grid md:grid-cols-12 gap-8">
                        <!-- Controls Column -->
                        <div class="md:col-span-7 space-y-6">
                            <h4 class="text-base font-bold text-slate-200 border-b border-slate-800 pb-2 flex items-center justify-between">
                                <span>Valuation Inputs</span>
                                <button onclick="resetDCF()" class="text-xs font-normal text-rutgers-light hover:underline">Reset Defaults</button>
                            </h4>

                            <!-- Input 1: Base Revenue -->
                            <div>
                                <div class="flex justify-between text-xs mb-2">
                                    <span class="text-slate-400 font-medium">Base Year Revenue ($M)</span>
                                    <span id="rev-val" class="font-mono text-white font-bold">$1,000M</span>
                                </div>
                                <input type="range" id="rev-input" min="100" max="5000" step="50" value="1000" oninput="calculateDCF()">
                            </div>

                            <!-- Input 2: Growth Rate -->
                            <div>
                                <div class="flex justify-between text-xs mb-2">
                                    <span class="text-slate-400 font-medium">5-Yr CAGR Revenue Growth</span>
                                    <span id="growth-val" class="font-mono text-emerald-400 font-bold">8.0%</span>
                                </div>
                                <input type="range" id="growth-input" min="1" max="35" step="0.5" value="8" oninput="calculateDCF()">
                            </div>

                            <!-- Input 3: Operating Margin -->
                            <div>
                                <div class="flex justify-between text-xs mb-2">
                                    <span class="text-slate-400 font-medium">Operating Margin (EBIT %)</span>
                                    <span id="margin-val" class="font-mono text-white font-bold">20.0%</span>
                                </div>
                                <input type="range" id="margin-input" min="5" max="45" step="0.5" value="20" oninput="calculateDCF()">
                            </div>

                            <!-- Input 4: Discount Rate (WACC) -->
                            <div>
                                <div class="flex justify-between text-xs mb-2">
                                    <span class="text-slate-400 font-medium">Discount Rate (WACC)</span>
                                    <span id="wacc-val" class="font-mono text-rutgers-light font-bold">9.0%</span>
                                </div>
                                <input type="range" id="wacc-input" min="5" max="16" step="0.25" value="9" oninput="calculateDCF()">
                            </div>

                            <!-- Input 5: Terminal Growth Rate -->
                            <div>
                                <div class="flex justify-between text-xs mb-2">
                                    <span class="text-slate-400 font-medium">Terminal Growth Rate (g)</span>
                                    <span id="terminal-val" class="font-mono text-white font-bold">2.5%</span>
                                </div>
                                <input type="range" id="terminal-input" min="1" max="4" step="0.1" value="2.5" oninput="calculateDCF()">
                            </div>
                        </div>

                        <!-- Results Output Column -->
                        <div class="md:col-span-5 bg-slate-950 p-6 rounded-xl border border-slate-800 flex flex-col justify-between">
                            <div>
                                <span class="text-xs font-semibold uppercase tracking-wider text-slate-400 block mb-1">Implied Enterprise Value</span>
                                <div id="ev-result" class="text-4xl font-extrabold text-white font-mono tracking-tight mb-4">
                                    $2,145.8M
                                </div>

                                <div class="space-y-3 pt-4 border-t border-slate-800/80 text-xs">
                                    <div class="flex justify-between text-slate-400">
                                        <span>PV of 5-Year Cash Flows</span>
                                        <span id="pv-cf-result" class="font-mono text-slate-200 font-semibold">$685.2M</span>
                                    </div>
                                    <div class="flex justify-between text-slate-400">
                                        <span>PV of Terminal Value</span>
                                        <span id="pv-tv-result" class="font-mono text-slate-200 font-semibold">$1,460.6M</span>
                                    </div>
                                    <div class="flex justify-between text-slate-400">
                                        <span>Implied EV / EBITDA Multiple</span>
                                        <span id="multiple-result" class="font-mono text-emerald-400 font-semibold">10.7x</span>
                                    </div>
                                </div>
                            </div>

                            <div class="mt-6 p-3 bg-slate-900 rounded-lg border border-slate-800 text-[11px] text-slate-400 leading-relaxed">
                                <span class="text-slate-300 font-semibold block mb-0.5">Methodology Note:</span>
                                Based on Perpetuity Growth Method. Assumes tax rate of 21% and FCF conversion of 75% of NOPAT.
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact" class="py-20 bg-slate-900 text-white relative">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-12 gap-12 items-center">
                    <div class="md:col-span-6 space-y-6">
                        <div class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-rutgers/20 text-rutgers-light font-semibold text-xs border border-rutgers/30">
                            <span>Get In Touch</span>
                        </div>
                        <h2 class="text-3xl sm:text-4xl font-extrabold tracking-tight">Let's Connect</h2>
                        <p class="text-slate-300 text-base leading-relaxed">
                            I am currently seeking full-time opportunities in Corporate Finance, Investment Banking, Equity Research, or Financial Analysis starting upon graduation in 2025.
                        </p>
                        
                        <div class="space-y-4 pt-2">
                            <div class="flex items-center space-x-4">
                                <div class="w-10 h-10 rounded-lg bg-slate-800 border border-slate-700 flex items-center justify-center text-rutgers-light">
                                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                                </div>
                                <div>
                                    <p class="text-xs text-slate-400">Email Direct</p>
                                    <p class="font-medium text-white text-sm">wguzman@rutgers.edu</p>
                                </div>
                            </div>

                            <div class="flex items-center space-x-4">
                                <div class="w-10 h-10 rounded-lg bg-slate-800 border border-slate-700 flex items-center justify-center text-rutgers-light">
                                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/></svg>
                                </div>
                                <div>
                                    <p class="text-xs text-slate-400">Location</p>
                                    <p class="font-medium text-white text-sm">Rutgers University • New Brunswick, NJ</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Contact Form Card -->
                    <div class="md:col-span-6 bg-slate-800/90 p-8 rounded-2xl border border-slate-700 shadow-xl">
                        <form id="contact-form" onsubmit="handleContactSubmit(event)" class="space-y-4">
                            <div>
                                <label class="block text-xs font-medium text-slate-300 mb-1">Your Name</label>
                                <input type="text" required placeholder="e.g. Jane Doe" class="w-full px-4 py-2.5 rounded-lg bg-slate-900 border border-slate-700 text-white placeholder-slate-500 text-sm focus:outline-none focus:border-rutgers focus:ring-1 focus:ring-rutgers transition-colors">
                            </div>
                            <div>
                                <label class="block text-xs font-medium text-slate-300 mb-1">Your Email</label>
                                <input type="email" required placeholder="e.g. jane@company.com" class="w-full px-4 py-2.5 rounded-lg bg-slate-900 border border-slate-700 text-white placeholder-slate-500 text-sm focus:outline-none focus:border-rutgers focus:ring-1 focus:ring-rutgers transition-colors">
                            </div>
                            <div>
                                <label class="block text-xs font-medium text-slate-300 mb-1">Message / Inquiry</label>
                                <textarea rows="4" required placeholder="Hello William, I would like to connect regarding..." class="w-full px-4 py-2.5 rounded-lg bg-slate-900 border border-slate-700 text-white placeholder-slate-500 text-sm focus:outline-none focus:border-rutgers focus:ring-1 focus:ring-rutgers transition-colors"></textarea>
                            </div>
                            <button type="submit" class="w-full py-3 rounded-lg text-white font-semibold rutgers-gradient hover:opacity-95 transition-all text-sm shadow-md">
                                Send Message
                            </button>
                            <p id="form-status" class="text-xs text-center text-emerald-400 font-medium hidden">Message sent successfully! Thank you.</p>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-slate-950 border-t border-slate-800 text-slate-400 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center sm:flex sm:justify-between sm:items-center text-xs">
            <p>© <span id="year">2026</span> William Guzman. All rights reserved. Rutgers Business School.</p>
            <div class="mt-4 sm:mt-0 flex justify-center space-x-6">
                <a href="https://linkedin.com" target="_blank" rel="noopener" class="hover:text-white transition-colors">LinkedIn</a>
                <a href="https://github.com" target="_blank" rel="noopener" class="hover:text-white transition-colors">GitHub</a>
                <a href="#about" class="hover:text-white transition-colors">Back to Top ↑</a>
            </div>
        </div>
    </footer>

    <!-- Modal 1 -->
    <div id="project1-modal" class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm hidden items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-2xl w-full p-6 shadow-2xl border border-slate-200 relative max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal('project1-modal')" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
            </button>
            <span class="px-2.5 py-1 text-xs font-bold text-rutgers bg-rutgers/10 rounded-md">Project Case Study</span>
            <h3 class="text-2xl font-bold text-slate-900 mt-2 mb-3">Rutgers Equity Valuation & DCF Model</h3>
            <div class="space-y-4 text-sm text-slate-600 leading-relaxed">
                <p>
                    This project involved constructing a thorough 3-statement financial model in Excel to forecast free cash flows over a 5-year discrete projection period for a publicly traded technology firm.
                </p>
                <h4 class="font-bold text-slate-900">Key Deliverables:</h4>
                <ul class="list-disc pl-5 space-y-1">
                    <li>Built dynamic revenue driver schedules based on segment growth rates.</li>
                    <li>Calculated Weighted Average Cost of Capital (WACC) using CAPM for cost of equity.</li>
                    <li>Constructed two-way sensitivity data tables evaluating EV against variations in WACC and Terminal Growth.</li>
                    <li>Benchmarked target firm against peer universe using EV/EBITDA and P/E trading multiples.</li>
                </ul>
            </div>
            <div class="mt-6 text-right">
                <button onclick="closeModal('project1-modal')" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 rounded-lg text-xs font-bold transition-colors">Close Overview</button>
            </div>
        </div>
    </div>

    <!-- Modal 2 -->
    <div id="project2-modal" class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm hidden items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-2xl w-full p-6 shadow-2xl border border-slate-200 relative max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal('project2-modal')" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
            </button>
            <span class="px-2.5 py-1 text-xs font-bold text-blue-700 bg-blue-50 rounded-md">Project Case Study</span>
            <h3 class="text-2xl font-bold text-slate-900 mt-2 mb-3">Portfolio Optimization & Risk Analysis</h3>
            <div class="space-y-4 text-sm text-slate-600 leading-relaxed">
                <p>
                    Utilized Python data science libraries (Pandas, NumPy, Matplotlib) to perform portfolio optimization on 10 large-cap equity securities over a 3-year historical window.
                </p>
                <h4 class="font-bold text-slate-900">Key Highlights:</h4>
                <ul class="list-disc pl-5 space-y-1">
                    <li>Simulated 10,000 portfolio weight combinations to plot the Efficient Frontier.</li>
                    <li>Identified optimal Tangency Portfolio maximizing Sharpe Ratio under historical risk free rates.</li>
                    <li>Calculated 95% 1-day Value at Risk (VaR) using historical and parametric methods.</li>
                </ul>
            </div>
            <div class="mt-6 text-right">
                <button onclick="closeModal('project2-modal')" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 rounded-lg text-xs font-bold transition-colors">Close Overview</button>
            </div>
        </div>
    </div>

    <!-- Modal 3 -->
    <div id="project3-modal" class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm hidden items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-2xl w-full p-6 shadow-2xl border border-slate-200 relative max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal('project3-modal')" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
            </button>
            <span class="px-2.5 py-1 text-xs font-bold text-emerald-700 bg-emerald-50 rounded-md">Project Case Study</span>
            <h3 class="text-2xl font-bold text-slate-900 mt-2 mb-3">Corporate Financial Health & Solvency Analysis</h3>
            <div class="space-y-4 text-sm text-slate-600 leading-relaxed">
                <p>
                    Analyzed multi-year SEC Form 10-K filings to assess liquidity, debt structure, capital expenditure coverage, and insolvency risks for an industrial manufacturing enterprise.
                </p>
                <h4 class="font-bold text-slate-900">Key Highlights:</h4>
                <ul class="list-disc pl-5 space-y-1">
                    <li>Executed DuPont Analysis to decompose ROE into profitability, asset efficiency, and leverage drivers.</li>
                    <li>Evaluated Altman Z-Score trend across 5 fiscal quarters to measure credit solvency.</li>
                    <li>Formulated executive recommendations for debt refinancing and working capital optimization.</li>
                </ul>
            </div>
            <div class="mt-6 text-right">
                <button onclick="closeModal('project3-modal')" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 rounded-lg text-xs font-bold transition-colors">Close Overview</button>
            </div>
        </div>
    </div>

    <script>
        // Set dynamic copyright year
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Skill Filtering Logic
        function filterSkills(category) {
            const cards = document.querySelectorAll('.skill-card');
            const buttons = document.querySelectorAll('.skill-btn');

            buttons.forEach(btn => {
                if(btn.getAttribute('data-category') === category) {
                    btn.classList.remove('bg-slate-100', 'text-slate-600', 'border-slate-200');
                    btn.classList.add('bg-rutgers', 'text-white', 'border-rutgers');
                } else {
                    btn.classList.remove('bg-rutgers', 'text-white', 'border-rutgers');
                    btn.classList.add('bg-slate-100', 'text-slate-600', 'border-slate-200');
                }
            });

            cards.forEach(card => {
                if (category === 'all' || card.getAttribute('data-category') === category) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Modal Handlers
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

        // Contact Form Handling
        function handleContactSubmit(e) {
            e.preventDefault();
            const status = document.getElementById('form-status');
            status.classList.remove('hidden');
            e.target.reset();
            setTimeout(() => {
                status.classList.add('hidden');
            }, 4000);
        }

        // Interactive DCF Calculation Engine
        function calculateDCF() {
            const rev = parseFloat(document.getElementById('rev-input').value);
            const growth = parseFloat(document.getElementById('growth-input').value) / 100;
            const margin = parseFloat(document.getElementById('margin-input').value) / 100;
            const wacc = parseFloat(document.getElementById('wacc-input').value) / 100;
            const g = parseFloat(document.getElementById('terminal-input').value) / 100;

            // Update Labels
            document.getElementById('rev-val').textContent = `$${rev.toLocaleString()}M`;
            document.getElementById('growth-val').textContent = `${(growth * 100).toFixed(1)}%`;
            document.getElementById('margin-val').textContent = `${(margin * 100).toFixed(1)}%`;
            document.getElementById('wacc-val').textContent = `${(wacc * 100).toFixed(2)}%`;
            document.getElementById('terminal-val').textContent = `${(g * 100).toFixed(1)}%`;

            // Calculate 5-Year Cash Flows
            let pvCashFlows = 0;
            let currentRev = rev;
            let finalYearFCF = 0;

            for (let year = 1; year <= 5; year++) {
                currentRev *= (1 + growth);
                const ebit = currentRev * margin;
                const nopat = ebit * (1 - 0.21); // 21% corporate tax rate
                const fcf = nopat * 0.75; // FCF conversion rate
                
                pvCashFlows += fcf / Math.pow(1 + wacc, year);
                if (year === 5) finalYearFCF = fcf;
            }

            // Terminal Value Calculation (Perpetuity Method)
            let pvTerminalValue = 0;
            if (wacc > g) {
                const terminalValue = (finalYearFCF * (1 + g)) / (wacc - g);
                pvTerminalValue = terminalValue / Math.pow(1 + wacc, 5);
            }

            const enterpriseValue = pvCashFlows + pvTerminalValue;
            const year1Ebitda = (rev * (1 + growth)) * (margin + 0.04); // Estimated EBITDA
            const evMultiple = year1Ebitda > 0 ? (enterpriseValue / year1Ebitda) : 0;

            // Render Output
            document.getElementById('ev-result').textContent = `$${enterpriseValue.toLocaleString('en-US', {minimumFractionDigits: 1, maximumFractionDigits: 1})}M`;
            document.getElementById('pv-cf-result').textContent = `$${pvCashFlows.toLocaleString('en-US', {minimumFractionDigits: 1, maximumFractionDigits: 1})}M`;
            document.getElementById('pv-tv-result').textContent = `$${pvTerminalValue.toLocaleString('en-US', {minimumFractionDigits: 1, maximumFractionDigits: 1})}M`;
            document.getElementById('multiple-result').textContent = `${evMultiple.toFixed(1)}x`;
        }

        function resetDCF() {
            document.getElementById('rev-input').value = 1000;
            document.getElementById('growth-input').value = 8;
            document.getElementById('margin-input').value = 20;
            document.getElementById('wacc-input').value = 9;
            document.getElementById('terminal-input').value = 2.5;
            calculateDCF();
        }

        // Initialize DCF engine on page load
        window.onload = function() {
            calculateDCF();
        };
    </script>
</body>
</html>
