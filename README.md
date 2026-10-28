# Assam-nursary-Dewdrop-nursary-```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dewdrop Nursery | Forestry, Agriculture & Landscaping - Lanka, Assam</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        forest: {
                            900: '#0f291e',
                            800: '#1b4332',
                            700: '#2d6a4f',
                            600: '#40916c',
                            500: '#52b788',
                            400: '#74c69d',
                            100: '#d8f3dc',
                            50: '#f4fbf7'
                        },
                        amberAccent: '#d97706'
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        .glass-nav {
            background: rgba(255, 255, 255, 0.94);
            backdrop-filter: blur(12px);
        }
        .custom-scrollbar::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #2d6a4f;
            border-radius: 4px;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans antialiased selection:bg-forest-500 selection:text-white">

    <!-- TOP ANNOUNCEMENT BAR -->
    <div class="bg-forest-900 text-slate-100 text-xs sm:text-sm py-2 px-4">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row justify-between items-center gap-2 text-center sm:text-left">
            <div class="flex items-center gap-3 flex-wrap justify-center sm:justify-start">
                <span class="inline-flex items-center gap-1 bg-forest-700 text-emerald-200 text-xs px-2.5 py-0.5 rounded-full border border-forest-600">
                    <i data-lucide="check-circle-2" class="w-3.5 h-3.5"></i> Govt. Registered Nursery
                </span>
                <span>GSTIN: <strong>18DLEPR2353R1ZC</strong></span>
                <span class="hidden md:inline">|</span>
                <span class="hidden md:inline">MSME: <strong>UDYAM-AS-30-0032621</strong></span>
            </div>
            <div class="flex items-center gap-4 text-xs">
                <span class="flex items-center gap-1"><i data-lucide="map-pin" class="w-3.5 h-3.5 text-forest-400"></i> Lanka, Hojai, Assam</span>
                <a href="tel:+919707467445" class="hover:text-forest-400 transition-colors flex items-center gap-1">
                    <i data-lucide="phone" class="w-3.5 h-3.5 text-forest-400"></i> +91 97074 67445
                </a>
            </div>
        </div>
    </div>

    <!-- MAIN NAVBAR -->
    <header class="sticky top-0 z-40 glass-nav border-b border-slate-200 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Brand Logo & Name -->
            <a href="#home" class="flex items-center gap-3 group">
                <div class="w-11 h-11 rounded-xl bg-gradient-to-br from-forest-800 to-forest-600 flex items-center justify-center text-white shadow-md group-hover:scale-105 transition-transform">
                    <i data-lucide="sprout" class="w-6 h-6"></i>
                </div>
                <div>
                    <span class="text-xl sm:text-2xl font-bold tracking-tight text-forest-900 block leading-tight">Dewdrop Nursery</span>
                    <span class="text-[10px] sm:text-xs font-medium text-forest-600 tracking-wider uppercase block">Forestry • Agro • Landscaping</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden lg:flex items-center gap-8 font-medium text-sm text-slate-700">
                <a href="#home" class="hover:text-forest-700 transition-colors">Home</a>
                <a href="#about" class="hover:text-forest-700 transition-colors">About Us</a>
                <a href="#catalog" class="hover:text-forest-700 transition-colors">Plant Varieties</a>
                <a href="#services" class="hover:text-forest-700 transition-colors">Services</a>
                <a href="#calculator" class="hover:text-forest-700 transition-colors">Requirement Builder</a>
                <a href="#contact" class="hover:text-forest-700 transition-colors">Contact</a>
            </nav>

            <!-- Action Buttons -->
            <div class="hidden sm:flex items-center gap-3">
                <a href="https://wa.me/919707467445?text=Hello%20Dewdrop%20Nursery,%20I%20have%20an%20inquiry%20regarding%20commercial%20plants." 
                   target="_blank" 
                   class="inline-flex items-center gap-2 bg-emerald-600 hover:bg-emerald-700 text-white px-4 py-2.5 rounded-lg text-sm font-semibold shadow-sm transition-all hover:shadow-md">
                    <i data-lucide="message-circle" class="w-4 h-4"></i>
                    <span>WhatsApp Us</span>
                </a>
                <button onclick="toggleCartDrawer()" class="relative bg-forest-800 hover:bg-forest-700 text-white p-2.5 rounded-lg shadow-sm transition-all" title="View Selected Items">
                    <i data-lucide="clipboard-list" class="w-5 h-5"></i>
                    <span id="cart-badge" class="absolute -top-1.5 -right-1.5 bg-amber-500 text-white text-[10px] font-bold w-5 h-5 rounded-full flex items-center justify-center border-2 border-white hidden">0</span>
                </button>
            </div>

            <!-- Mobile Menu Toggle -->
            <div class="flex items-center gap-2 lg:hidden">
                <button onclick="toggleCartDrawer()" class="relative bg-forest-800 text-white p-2 rounded-lg">
                    <i data-lucide="clipboard-list" class="w-5 h-5"></i>
                    <span id="cart-badge-mobile" class="absolute -top-1 -right-1 bg-amber-500 text-white text-[10px] font-bold w-4 h-4 rounded-full flex items-center justify-center hidden">0</span>
                </button>
                <button onclick="toggleMobileMenu()" class="p-2 text-slate-700 hover:text-forest-800 focus:outline-none">
                    <i data-lucide="menu" id="menu-icon" class="w-7 h-7"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Nav Menu -->
        <div id="mobile-menu" class="hidden lg:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-6 space-y-3">
            <a href="#home" onclick="toggleMobileMenu()" class="block py-2 text-slate-700 font-medium hover:text-forest-700">Home</a>
            <a href="#about" onclick="toggleMobileMenu()" class="block py-2 text-slate-700 font-medium hover:text-forest-700">About Us</a>
            <a href="#catalog" onclick="toggleMobileMenu()" class="block py-2 text-slate-700 font-medium hover:text-forest-700">Plant Varieties</a>
            <a href="#services" onclick="toggleMobileMenu()" class="block py-2 text-slate-700 font-medium hover:text-forest-700">Services</a>
            <a href="#calculator" onclick="toggleMobileMenu()" class="block py-2 text-slate-700 font-medium hover:text-forest-700">Requirement Builder</a>
            <a href="#contact" onclick="toggleMobileMenu()" class="block py-2 text-slate-700 font-medium hover:text-forest-700">Contact Us</a>
            <div class="pt-2 flex flex-col gap-2">
                <a href="tel:+919707467445" class="w-full text-center bg-slate-100 hover:bg-slate-200 text-slate-800 py-2.5 rounded-lg text-sm font-semibold flex items-center justify-center gap-2">
                    <i data-lucide="phone" class="w-4 h-4"></i> Call +91 97074 67445
                </a>
                <a href="https://wa.me/919707467445" target="_blank" class="w-full text-center bg-emerald-600 text-white py-2.5 rounded-lg text-sm font-semibold flex items-center justify-center gap-2">
                    <i data-lucide="message-circle" class="w-4 h-4"></i> WhatsApp Inquiry
                </a>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="home" class="relative bg-gradient-to-br from-forest-900 via-forest-800 to-forest-900 text-white py-16 md:py-24 overflow-hidden">
        <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#ffffff_1px,transparent_1px)] [background-size:16px_16px]"></div>
        <div class="absolute -right-20 -bottom-20 w-96 h-96 bg-forest-500/20 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-forest-700/60 border border-forest-500/30 text-emerald-200 text-xs sm:text-sm font-medium">
                        <i data-lucide="trees" class="w-4 h-4 text-forest-400"></i> Commercial Plantation & Forestry Specialists
                    </div>
                    
                    <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight leading-tight">
                        Your Trusted Partner in <span class="text-emerald-300">Forestry, Agriculture</span> & Exotic Plants
                    </h1>
                    
                    <p class="text-slate-200 text-base sm:text-lg max-w-2xl font-light mx-auto lg:mx-0">
                        Supplying premium commercial grade saplings, high-yielding grafted fruit trees, high-value timber, sericulture hosts, and full afforestation contracting services across Assam and Northeast India.
                    </p>

                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-2">
                        <a href="#catalog" class="w-full sm:w-auto bg-forest-500 hover:bg-forest-400 text-forest-900 font-bold px-7 py-3.5 rounded-xl shadow-lg transition-all transform hover:-translate-y-0.5 text-center flex items-center justify-center gap-2">
                            <i data-lucide="leaf" class="w-5 h-5"></i> View All Plant Varieties
                        </a>
                        <a href="#calculator" class="w-full sm:w-auto bg-white/10 hover:bg-white/20 text-white border border-white/20 font-semibold px-7 py-3.5 rounded-xl transition-all text-center flex items-center justify-center gap-2 backdrop-blur-sm">
                            <i data-lucide="clipboard-list" class="w-5 h-5"></i> Build Inquiry List
                        </a>
                    </div>

                    <!-- Highlight Badges -->
                    <div class="pt-8 grid grid-cols-2 sm:grid-cols-3 gap-4 text-left border-t border-forest-600/40">
                        <div>
                            <div class="text-2xl font-bold text-emerald-300">50,000+</div>
                            <div class="text-xs text-slate-300">Annual Sapling Nursery Capacity</div>
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-emerald-300">35+ Varieties</div>
                            <div class="text-xs text-slate-300">Timber, Fruits & Spices</div>
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-emerald-300">Pan-India</div>
                            <div class="text-xs text-slate-300">Logistics & Direct Supply</div>
                        </div>
                    </div>
                </div>

                <!-- Hero Image & Quick Info Card -->
                <div class="lg:col-span-5">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <div class="rounded-3xl overflow-hidden shadow-2xl border-4 border-white/10 relative group">
                            <img src="https://images.unsplash.com/photo-1585320806297-9794b3e4eeae?auto=format&fit=crop&w=800&q=80" 
                                 alt="Dewdrop Commercial Nursery Saplings" 
                                 class="w-full h-80 sm:h-96 object-cover transform group-hover:scale-105 transition-transform duration-500"
                                 onerror="this.src='https://placehold.co/800x600/2d6a4f/ffffff?text=Dewdrop+Nursery+Plantation'">
                            <div class="absolute inset-0 bg-gradient-to-t from-forest-900/90 via-transparent to-transparent"></div>
                            <div class="absolute bottom-6 left-6 right-6 text-white">
                                <span class="bg-amber-500 text-white text-xs font-bold px-2.5 py-1 rounded-md uppercase tracking-wider">Certified Varieties</span>
                                <h3 class="text-xl font-bold mt-2">Agarwood, Sandalwood & Grafted Fruit Saplings</h3>
                                <p class="text-xs text-slate-200 mt-1">High survival rate & expert agro-forestry advice.</p>
                            </div>
                        </div>

                        <!-- Floating Badge -->
                        <div class="absolute -bottom-6 -left-6 bg-white text-slate-800 p-4 rounded-2xl shadow-xl hidden sm:flex items-center gap-3 border border-slate-100">
                            <div class="w-12 h-12 rounded-xl bg-forest-100 text-forest-700 flex items-center justify-center">
                                <i data-lucide="shield-check" class="w-6 h-6"></i>
                            </div>
                            <div>
                                <div class="text-xs text-slate-500 font-medium">Govt Registration</div>
                                <div class="text-sm font-bold text-forest-800">GSTIN & MSME Certified</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CREDENTIALS & TRUST BAR -->
    <section class="bg-white py-8 border-b border-slate-200 shadow-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6 text-center md:text-left divide-y md:divide-y-0 md:divide-x divide-slate-100">
                <div class="flex items-center justify-center md:justify-start gap-4 pt-4 md:pt-0">
                    <i data-lucide="badge-check" class="w-8 h-8 text-forest-600 flex-shrink-0"></i>
                    <div>
                        <h4 class="font-bold text-slate-800 text-sm">Proprietor</h4>
                        <p class="text-xs text-slate-500">Imrazur Rahman</p>
                    </div>
                </div>
                <div class="flex items-center justify-center md:justify-start gap-4 pt-4 md:pt-0 md:pl-6">
                    <i data-lucide="building-2" class="w-8 h-8 text-forest-600 flex-shrink-0"></i>
                    <div>
                        <h4 class="font-bold text-slate-800 text-sm">GSTIN Registered</h4>
                        <p class="text-xs text-slate-500">18DLEPR2353R1ZC</p>
                    </div>
                </div>
                <div class="flex items-center justify-center md:justify-start gap-4 pt-4 md:pt-0 md:pl-6">
                    <i data-lucide="award" class="w-8 h-8 text-forest-600 flex-shrink-0"></i>
                    <div>
                        <h4 class="font-bold text-slate-800 text-sm">MSME Udyam</h4>
                        <p class="text-xs text-slate-500">UDYAM-AS-30-0032621</p>
                    </div>
                </div>
                <div class="flex items-center justify-center md:justify-start gap-4 pt-4 md:pt-0 md:pl-6">
                    <i data-lucide="truck" class="w-8 h-8 text-forest-600 flex-shrink-0"></i>
                    <div>
                        <h4 class="font-bold text-slate-800 text-sm">Supply Radius</h4>
                        <p class="text-xs text-slate-500">Assam, NE & Pan-India</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FEATURED CATALOG & INTERACTIVE CATALOG -->
    <section id="catalog" class="py-16 md:py-24 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-8 gap-4">
                <div>
                    <span class="text-forest-600 font-bold text-xs uppercase tracking-wider">High Quality Plant Stock</span>
                    <h2 class="text-3xl font-extrabold text-slate-900 mt-1">Explore Our Plant Varieties</h2>
                    <p class="text-slate-600 text-sm mt-1">Select plant species to request custom bulk price quotations & technical specifications.</p>
                </div>
                
                <!-- Search Bar -->
                <div class="w-full md:w-80 relative">
                    <i data-lucide="search" class="w-4 h-4 text-slate-400 absolute left-3.5 top-1/2 -translate-y-1/2"></i>
                    <input type="text" id="catalog-search" onkeyup="filterPlants()" placeholder="Search plant name, species..." 
                           class="w-full pl-10 pr-4 py-2.5 bg-white border border-slate-300 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-forest-600 focus:border-transparent shadow-xs">
                </div>
            </div>

            <!-- Category Filter Tabs -->
            <div class="flex items-center gap-2 overflow-x-auto pb-4 mb-8 custom-scrollbar border-b border-slate-200">
                <button onclick="setCategory('all')" id="cat-all" class="cat-btn bg-forest-800 text-white px-4 py-2 rounded-xl text-sm font-semibold whitespace-nowrap transition-colors shadow-xs">
                    All Varieties (30+)
                </button>
                <button onclick="setCategory('forestry')" id="cat-forestry" class="cat-btn bg-white hover:bg-slate-100 text-slate-700 border border-slate-200 px-4 py-2 rounded-xl text-sm font-medium whitespace-nowrap transition-colors">
                    Forestry & Timber
                </button>
                <button onclick="setCategory('fruit')" id="cat-fruit" class="cat-btn bg-white hover:bg-slate-100 text-slate-700 border border-slate-200 px-4 py-2 rounded-xl text-sm font-medium whitespace-nowrap transition-colors">
                    Fruit-Bearing Saplings
                </button>
                <button onclick="setCategory('indoor')" id="cat-indoor" class="cat-btn bg-white hover:bg-slate-100 text-slate-700 border border-slate-200 px-4 py-2 rounded-xl text-sm font-medium whitespace-nowrap transition-colors">
                    Indoor & Landscaping
                </button>
                <button onclick="setCategory('medicinal')" id="cat-medicinal" class="cat-btn bg-white hover:bg-slate-100 text-slate-700 border border-slate-200 px-4 py-2 rounded-xl text-sm font-medium whitespace-nowrap transition-colors">
                    Medicinal & High-Value
                </button>
                <button onclick="setCategory('sericulture')" id="cat-sericulture" class="cat-btn bg-white hover:bg-slate-100 text-slate-700 border border-slate-200 px-4 py-2 rounded-xl text-sm font-medium whitespace-nowrap transition-colors">
                    Sericulture & Spices
                </button>
            </div>

            <!-- Plant Cards Grid -->
            <div id="plant-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                <!-- JavaScript will dynamically render plant cards here -->
            </div>

            <!-- No results state -->
            <div id="no-results" class="hidden py-16 text-center">
                <i data-lucide="leaf" class="w-12 h-12 text-slate-300 mx-auto mb-3"></i>
                <h3 class="text-lg font-bold text-slate-700">No matching plant varieties found</h3>
                <p class="text-slate-500 text-sm mt-1">Try adjusting your search query or switching category filters.</p>
            </div>
        </div>
    </section>

    <!-- QUOTATION & REQUIREMENT BUILDER SECTION -->
    <section id="calculator" class="py-16 md:py-24 bg-white border-y border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <span class="text-forest-600 font-bold text-xs uppercase tracking-wider">Custom Order Request</span>
                <h2 class="text-3xl font-extrabold text-slate-900 mt-1">Plant Requirement & Specification Builder</h2>
                <p class="text-slate-600 text-sm mt-2">
                    Configure your plantation requirements, choose sapling stages and delivery zones, and generate an official inquiry request directly for custom quote calculation.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
                <!-- Requirement Configuration Form -->
                <div class="lg:col-span-7 bg-slate-50 p-6 sm:p-8 rounded-2xl border border-slate-200 shadow-sm space-y-6">
                    <h3 class="text-lg font-bold text-forest-800 flex items-center gap-2 border-b border-slate-200 pb-3">
                        <i data-lucide="sliders" class="w-5 h-5 text-forest-600"></i> Configure Plant Specification
                    </h3>

                    <!-- Select Variety -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-2">Select Plant Variety</label>
                        <select id="calc-plant-select" onchange="updateCalcPreview()" class="w-full bg-white border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                            <!-- Populated dynamically by JS -->
                        </select>
                    </div>

                    <!-- Quantity & Stage -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-2">Required Quantity</label>
                            <input type="number" id="calc-qty" value="100" min="10" step="10" oninput="updateCalcPreview()" 
                                   class="w-full bg-white border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-2">Plant Form / Stage</label>
                            <select id="calc-stage" onchange="updateCalcPreview()" class="w-full bg-white border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                                <option value="Standard Nursery Sapling (Polybag)">Standard Nursery Sapling (Polybag)</option>
                                <option value="Grafted / Premium Rootstock">Grafted / Premium Rootstock</option>
                                <option value="Bare Root Seedling / Stump">Bare Root Seedling / Stump</option>
                                <option value="Mature Hardened Plant (Container)">Mature Hardened Plant (Container)</option>
                            </select>
                        </div>
                    </div>

                    <!-- Delivery Region -->
                    <div>
                        <label class="block text-xs font-bold text-slate-700 uppercase tracking-wider mb-2">Delivery Location Zone</label>
                        <select id="calc-region" onchange="updateCalcPreview()" class="w-full bg-white border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                            <option value="Assam Local Pick-Up / Self Transport (Lanka Base)">Assam Local Pick-Up / Self Transport (Lanka Base)</option>
                            <option value="Central Assam (Hojai, Nagaon, Karbi Anglong)">Central Assam (Hojai, Nagaon, Karbi Anglong)</option>
                            <option value="Greater Assam & Guwahati Region">Greater Assam & Guwahati Region</option>
                            <option value="Other Northeast States (Arunachal, Meghalaya, Nagaland, etc.)">Other Northeast States (Arunachal, Meghalaya, Nagaland, etc.)</option>
                            <option value="Pan-India Freight Transport">Pan-India Freight Transport</option>
                        </select>
                    </div>

                    <!-- Add to Specification List Button -->
                    <button onclick="addCurrentCalcToCart()" class="w-full bg-forest-800 hover:bg-forest-700 text-white font-bold py-3.5 px-4 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                        <i data-lucide="plus-circle" class="w-5 h-5"></i> Add Item to Inquiry List
                    </button>
                </div>

                <!-- Requirement Summary Box -->
                <div class="lg:col-span-5 bg-gradient-to-br from-forest-900 to-forest-800 text-white p-6 sm:p-8 rounded-2xl shadow-xl flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between border-b border-forest-600 pb-4 mb-6">
                            <h3 class="text-lg font-bold flex items-center gap-2">
                                <i data-lucide="clipboard-check" class="w-5 h-5 text-emerald-300"></i> Requirement Summary
                            </h3>
                            <span class="text-xs bg-forest-600/80 px-2.5 py-1 rounded-full text-emerald-200">Quote Ready</span>
                        </div>

                        <div class="space-y-4 text-sm">
                            <div class="flex justify-between items-start text-slate-200">
                                <span>Selected Variety:</span>
                                <strong id="summary-plant-name" class="text-white text-right max-w-[200px]">Teak Wood (Tectona grandis)</strong>
                            </div>
                            <div class="flex justify-between items-center text-slate-200">
                                <span>Required Quantity:</span>
                                <strong id="summary-qty" class="text-white">100 units</strong>
                            </div>
                            <div class="flex justify-between items-start text-slate-200">
                                <span>Planting Stage:</span>
                                <strong id="summary-stage" class="text-white text-right max-w-[200px]">Standard Nursery Sapling</strong>
                            </div>
                            <div class="flex justify-between items-start text-slate-200 border-b border-forest-600 pb-4">
                                <span>Destination Zone:</span>
                                <strong id="summary-region" class="text-white text-right max-w-[200px]">Central Assam</strong>
                            </div>
                        </div>

                        <div class="pt-4 mt-2">
                            <div class="text-xs text-emerald-200 uppercase font-semibold">Inquiry Status</div>
                            <div class="text-xl sm:text-2xl font-bold text-white mt-1">Ready to Request Custom Pricing</div>
                            <p class="text-[11px] text-slate-300 mt-2 italic">*Our agro experts will prepare an official customized quote with freight options based on bulk volume.</p>
                        </div>
                    </div>

                    <!-- Direct Send Actions -->
                    <div class="mt-8 space-y-3 pt-6 border-t border-forest-600">
                        <button onclick="sendCalcToWhatsApp()" class="w-full bg-emerald-500 hover:bg-emerald-400 text-forest-900 font-bold py-3 px-4 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                            <i data-lucide="message-square" class="w-5 h-5"></i> Request Pricing via WhatsApp
                        </button>
                        <button onclick="copyQuoteToClipboard()" class="w-full bg-white/10 hover:bg-white/20 text-white font-medium py-2.5 px-4 rounded-xl border border-white/20 transition-all text-xs flex items-center justify-center gap-2">
                            <i data-lucide="copy" class="w-4 h-4"></i> Copy Requirement Details
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- BUSINESS SERVICES & CONTRACTING -->
    <section id="services" class="py-16 md:py-24 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-forest-600 font-bold text-xs uppercase tracking-wider">Expertise & Execution</span>
                <h2 class="text-3xl font-extrabold text-slate-900 mt-1">Commercial Contracting & Nursery Services</h2>
                <p class="text-slate-600 text-sm mt-2">
                    Beyond plant production, Dewdrop Nursery provides full turnkey afforestation, agricultural land preparation, and official greening services.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition-all flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 bg-forest-100 text-forest-700 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-forest-700 group-hover:text-white transition-colors">
                            <i data-lucide="truck" class="w-7 h-7"></i>
                        </div>
                        <h3 class="text-xl font-bold text-slate-800 mb-3">Bulk Wholesale Plant Supply</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            Logistics setup for supplying tens of thousands of healthy commercial saplings (Timber, Agarwood, Sericulture hosts, Grafted Fruit plants) straight to plantation sites.
                        </p>
                    </div>
                    <ul class="mt-6 space-y-2 border-t border-slate-100 pt-4 text-xs font-medium text-slate-700">
                        <li class="flex items-center gap-2"><i data-lucide="check" class="w-4 h-4 text-forest-600"></i> Shock-proof transport packaging</li>
                        <li class="flex items-center gap-2"><i data-lucide="check" class="w-4 h-4 text-forest-600"></i> Dedicated vehicle freight support</li>
                    </ul>
                </div>

                <!-- Service 2 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition-all flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 bg-forest-100 text-forest-700 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-forest-700 group-hover:text-white transition-colors">
                            <i data-lucide="trees" class="w-7 h-7"></i>
                        </div>
                        <h3 class="text-xl font-bold text-slate-800 mb-3">Commercial Plantation Contracting</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            Complete field execution for landowners, corporate CSR/ESG projects, and government agro-forestry initiatives, including ground preparation, pit digging, and sapling planting.
                        </p>
                    </div>
                    <ul class="mt-6 space-y-2 border-t border-slate-100 pt-4 text-xs font-medium text-slate-700">
                        <li class="flex items-center gap-2"><i data-lucide="check" class="w-4 h-4 text-forest-600"></i> High-density planting layout</li>
                        <li class="flex items-center gap-2"><i data-lucide="check" class="w-4 h-4 text-forest-600"></i> Inoculation & growth advisory</li>
                    </ul>
                </div>

                <!-- Service 3 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition-all flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 bg-forest-100 text-forest-700 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-forest-700 group-hover:text-white transition-colors">
                            <i data-lucide="flower2" class="w-7 h-7"></i>
                        </div>
                        <h3 class="text-xl font-bold text-slate-800 mb-3">Landscaping & Beautification</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            Landscape architecture, planting layout, and greening solutions for institutional campuses, resorts, private estates, and urban parks with hardy indoor and outdoor species.
                        </p>
                    </div>
                    <ul class="mt-6 space-y-2 border-t border-slate-100 pt-4 text-xs font-medium text-slate-700">
                        <li class="flex items-center gap-2"><i data-lucide="check" class="w-4 h-4 text-forest-600"></i> Climate & soil suitability checks</li>
                        <li class="flex items-center gap-2"><i data-lucide="check" class="w-4 h-4 text-forest-600"></i> Post-plantation maintenance support</li>
                    </ul>
                </div>
            </div>

            <!-- Quality Assurance Banner -->
            <div class="mt-12 bg-forest-800 text-white rounded-2xl p-6 sm:p-8 flex flex-col md:flex-row items-center justify-between gap-6">
                <div class="flex items-center gap-4">
                    <div class="w-12 h-12 rounded-full bg-forest-600 flex items-center justify-center flex-shrink-0">
                        <i data-lucide="shield-check" class="w-6 h-6 text-emerald-300"></i>
                    </div>
                    <div>
                        <h4 class="text-lg font-bold">100% Quality & Survival Assurance</h4>
                        <p class="text-xs text-slate-200 mt-0.5">We supply authentic, hardened saplings with high field survival rates and expert guidance.</p>
                    </div>
                </div>
                <a href="#contact" class="bg-forest-500 hover:bg-forest-400 text-forest-900 font-bold px-6 py-3 rounded-xl text-sm whitespace-nowrap transition-colors">
                    Consult Our Agro Experts
                </a>
            </div>
        </div>
    </section>

    <!-- ABOUT US & CREDENTIALS -->
    <section id="about" class="py-16 md:py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <div class="lg:col-span-6 space-y-6">
                    <span class="text-forest-600 font-bold text-xs uppercase tracking-wider">About Dewdrop Nursery</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-slate-900 leading-tight">
                        Rooted in Excellence, Cultivating Northeast India's Green Wealth
                    </h2>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Situated at Bordoloi Pathar, Tiniali Bazar in Lanka, Hojai district (Assam), Dewdrop Nursery operates under the leadership of <strong>Proprietor Imrazur Rahman</strong>. We have grown into one of Central Assam's primary centers for commercial forestry, high-value timber, exotic grafted fruit crops, sericulture host plants, and ornamental landscaping species.
                    </p>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        Our nursery enforces rigorous root hardening, organic disease management, and climate-acclimation techniques to guarantee top performance when planted across agricultural grounds or commercial timber lots.
                    </p>

                    <!-- Official Credentials Box -->
                    <div class="bg-slate-50 border border-slate-200 rounded-2xl p-6 space-y-4">
                        <h4 class="font-bold text-slate-800 text-sm uppercase tracking-wider text-forest-800 border-b border-slate-200 pb-2">
                            Official Business Credentials
                        </h4>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 text-xs">
                            <div>
                                <span class="text-slate-500 block">Proprietorship:</span>
                                <strong class="text-slate-800 text-sm">Imrazur Rahman</strong>
                            </div>
                            <div>
                                <span class="text-slate-500 block">GSTIN Registration:</span>
                                <strong class="text-slate-800 text-sm">18DLEPR2353R1ZC</strong>
                            </div>
                            <div>
                                <span class="text-slate-500 block">MSME Udyam Number:</span>
                                <strong class="text-slate-800 text-sm">UDYAM-AS-30-0032621</strong>
                            </div>
                            <div>
                                <span class="text-slate-500 block">Primary Nursery Location:</span>
                                <strong class="text-slate-800 text-sm">Lanka, Hojai, Assam</strong>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="lg:col-span-6 grid grid-cols-2 gap-4">
                    <div class="space-y-4">
                        <img src="https://images.unsplash.com/photo-1592417817098-8f3d6eb16115?auto=format&fit=crop&w=600&q=80" 
                             alt="Nursery Saplings" class="rounded-2xl shadow-md w-full h-48 sm:h-64 object-cover"
                             onerror="this.src='https://placehold.co/600x400/2d6a4f/ffffff?text=Greenery'">
                        <div class="bg-forest-100 p-6 rounded-2xl text-center">
                            <span class="text-3xl font-extrabold text-forest-800 block">100%</span>
                            <span class="text-xs font-semibold text-forest-700 mt-1 block">Disease Free & Field Hardened Stocks</span>
                        </div>
                    </div>
                    <div class="space-y-4 pt-8">
                        <div class="bg-amber-50 border border-amber-200 p-6 rounded-2xl text-center">
                            <span class="text-3xl font-extrabold text-amber-700 block">High Yield</span>
                            <span class="text-xs font-semibold text-amber-800 mt-1 block">Grafted Fruit Rootstock</span>
                        </div>
                        <img src="https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=600&q=80" 
                             alt="Fruit Orchard" class="rounded-2xl shadow-md w-full h-48 sm:h-64 object-cover"
                             onerror="this.src='https://placehold.co/600x400/52b788/ffffff?text=Orchard'">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT & ORDER INQUIRY SECTION -->
    <section id="contact" class="py-16 md:py-24 bg-slate-50 border-t border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-forest-600 font-bold text-xs uppercase tracking-wider">Get In Touch</span>
                <h2 class="text-3xl font-extrabold text-slate-900 mt-1">Contact & Official Quote Request</h2>
                <p class="text-slate-600 text-sm mt-2">Have specific inquiries or require wholesale price quotes? Submit your details directly below.</p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
                <!-- Inquiry Form -->
                <div class="lg:col-span-7 bg-white p-6 sm:p-8 rounded-2xl border border-slate-200 shadow-sm">
                    <form id="inquiry-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Your Full Name *</label>
                                <input type="text" id="form-name" required placeholder="e.g. Rahul Sharma" 
                                       class="w-full bg-slate-50 border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Phone / WhatsApp *</label>
                                <input type="tel" id="form-phone" required placeholder="+91 98765 43210" 
                                       class="w-full bg-slate-50 border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                            </div>
                        </div>

                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Delivery Location / District</label>
                                <input type="text" id="form-location" placeholder="e.g. Nagaon, Assam / Itanagar, AP" 
                                       class="w-full bg-slate-50 border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Primary Plant Category</label>
                                <select id="form-category" class="w-full bg-slate-50 border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none">
                                    <option>Forestry & Timber Saplings</option>
                                    <option>Fruit-Bearing Grafted Saplings</option>
                                    <option>Indoor & Landscaping Plants</option>
                                    <option>Medicinal & High-Value Plants</option>
                                    <option>Sericulture Host Plants & Spices</option>
                                    <option>Commercial Afforestation Contracting</option>
                                </select>
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-700 uppercase mb-1">Plant Details & Quantity Specifications</label>
                            <textarea id="form-message" rows="4" placeholder="Mention required plant names, quantities, preferred sizes, or field planting requirements..." 
                                      class="w-full bg-slate-50 border border-slate-300 rounded-xl p-3 text-sm focus:ring-2 focus:ring-forest-600 focus:outline-none"></textarea>
                        </div>

                        <button type="submit" class="w-full bg-forest-800 hover:bg-forest-700 text-white font-bold py-3.5 px-6 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                            <i data-lucide="send" class="w-4 h-4"></i> Submit Inquiry via WhatsApp
                        </button>
                    </form>
                </div>

                <!-- Contact Info Card & Map Highlight -->
                <div class="lg:col-span-5 space-y-6">
                    <div class="bg-forest-800 text-white p-6 sm:p-8 rounded-2xl shadow-md space-y-6">
                        <h3 class="text-xl font-bold border-b border-forest-600 pb-3">Dewdrop Nursery Contact Details</h3>

                        <div class="space-y-4 text-sm">
                            <div class="flex items-start gap-3">
                                <i data-lucide="map-pin" class="w-5 h-5 text-forest-400 flex-shrink-0 mt-0.5"></i>
                                <div>
                                    <strong class="block text-white">Nursery Address:</strong>
                                    <p class="text-slate-200">Bordoloi Pathar, Tiniali Bazar, Lanka, Hojai District, Assam - 782446</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3">
                                <i data-lucide="phone" class="w-5 h-5 text-forest-400 flex-shrink-0 mt-0.5"></i>
                                <div>
                                    <strong class="block text-white">Phone & WhatsApp:</strong>
                                    <p class="text-slate-200">+91 97074 67445</p>
                                    <p class="text-slate-200">+91 84866 86503</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3">
                                <i data-lucide="mail" class="w-5 h-5 text-forest-400 flex-shrink-0 mt-0.5"></i>
                                <div>
                                    <strong class="block text-white">Email Address:</strong>
                                    <p class="text-slate-200">dewdropnursary01@gmail.com</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-3">
                                <i data-lucide="clock" class="w-5 h-5 text-forest-400 flex-shrink-0 mt-0.5"></i>
                                <div>
                                    <strong class="block text-white">Working Hours:</strong>
                                    <p class="text-slate-200">Monday - Saturday: 7:00 AM - 6:00 PM</p>
                                    <p class="text-slate-200">Sunday: Open by appointment</p>
                                </div>
                            </div>
                        </div>

                        <div class="pt-2">
                            <a href="https://wa.me/919707467445?text=Hi%20Dewdrop%20Nursery,%20I%20would%20like%20to%20visit%20your%20nursery%20in%20Lanka." 
                               target="_blank" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white font-bold py-2.5 px-4 rounded-xl text-center text-xs flex items-center justify-center gap-2 transition-colors">
                                <i data-lucide="navigation" class="w-4 h-4"></i> Get Directions & Visit Nursery
                            </a>
                        </div>
                    </div>

                    <!-- Map Location Placeholder Container -->
                    <div class="bg-white p-4 rounded-2xl border border-slate-200 shadow-sm">
                        <div class="flex items-center justify-between mb-3 px-1">
                            <span class="text-xs font-bold text-slate-700 uppercase">Nursery Location Map</span>
                            <span class="text-[11px] text-forest-600 font-semibold">Lanka, Assam</span>
                        </div>
                        <div class="w-full h-48 bg-slate-200 rounded-xl overflow-hidden relative flex items-center justify-center text-center p-4">
                            <div class="absolute inset-0 opacity-40 bg-[radial-gradient(#1b4332_1px,transparent_1px)] [background-size:12px_12px]"></div>
                            <div class="relative z-10 space-y-2">
                                <div class="w-10 h-10 bg-forest-800 text-white rounded-full mx-auto flex items-center justify-center shadow-lg animate-bounce">
                                    <i data-lucide="map-pin" class="w-5 h-5"></i>
                                </div>
                                <p class="text-xs font-bold text-slate-800">Dewdrop Nursery Hub</p>
                                <p class="text-[11px] text-slate-600">Bordoloi Pathar, Tiniali Bazar, Lanka, Assam</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-slate-900 text-slate-400 py-12 border-t border-slate-800 text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div class="space-y-3">
                    <div class="flex items-center gap-2 text-white">
                        <i data-lucide="sprout" class="w-5 h-5 text-forest-400"></i>
                        <span class="text-base font-bold">Dewdrop Nursery</span>
                    </div>
                    <p class="text-slate-400 leading-relaxed">
                        Commercial plant nursery, forestry species producer, and agricultural contractor based in Lanka, Hojai, Assam.
                    </p>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-3 uppercase tracking-wider text-xs">Quick Navigation</h4>
                    <ul class="space-y-2">
                        <li><a href="#home" class="hover:text-white transition-colors">Home</a></li>
                        <li><a href="#about" class="hover:text-white transition-colors">About Us</a></li>
                        <li><a href="#catalog" class="hover:text-white transition-colors">Plant Catalog</a></li>
                        <li><a href="#calculator" class="hover:text-white transition-colors">Requirement Builder</a></li>
                        <li><a href="#contact" class="hover:text-white transition-colors">Contact</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-3 uppercase tracking-wider text-xs">Major Varieties</h4>
                    <ul class="space-y-2">
                        <li>Agarwood & Sandalwood</li>
                        <li>Teak & Mahogany Timber</li>
                        <li>Grafted Macadamia & Hass Avocado</li>
                        <li>Khasi Mandarin & Miyazaki Mango</li>
                        <li>Som & Soalu (Sericulture Hosts)</li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-3 uppercase tracking-wider text-xs">Government Registration</h4>
                    <div class="space-y-2 text-slate-300">
                        <p><strong class="text-slate-100">Proprietor:</strong> Imrazur Rahman</p>
                        <p><strong class="text-slate-100">GSTIN:</strong> 18DLEPR2353R1ZC</p>
                        <p><strong class="text-slate-100">MSME:</strong> UDYAM-AS-30-0032621</p>
                    </div>
                </div>
            </div>

            <div class="pt-8 border-t border-slate-800 flex flex-col sm:flex-row items-center justify-between gap-4 text-center sm:text-left">
                <p>&copy; 2026 Dewdrop Nursery. All Rights Reserved. Bordoloi Pathar, Tiniali Bazar, Lanka, Hojai, Assam - 782446.</p>
                <p class="text-slate-500">Commercial Agro-Forestry & Landscaping Specialists</p>
            </div>
        </div>
    </footer>

    <!-- SLIDE-OVER INQUIRY CART DRAWER -->
    <div id="cart-drawer" class="fixed inset-0 z-50 overflow-hidden hidden" aria-labelledby="slide-over-title" role="dialog" aria-modal="true">
        <div class="absolute inset-0 bg-slate-900/50 backdrop-blur-xs transition-opacity" onclick="toggleCartDrawer()"></div>

        <div class="pointer-events-none fixed inset-y-0 right-0 flex max-w-full pl-10">
            <div class="pointer-events-auto w-screen max-w-md bg-white shadow-2xl flex flex-col">
                <!-- Drawer Header -->
                <div class="bg-forest-800 text-white p-6 flex items-center justify-between">
                    <div class="flex items-center gap-2">
                        <i data-lucide="clipboard-list" class="w-5 h-5 text-emerald-300"></i>
                        <h2 class="text-lg font-bold" id="slide-over-title">Selected Requirement List</h2>
                    </div>
                    <button onclick="toggleCartDrawer()" class="text-slate-300 hover:text-white p-1">
                        <i data-lucide="x" class="w-6 h-6"></i>
                    </button>
                </div>

                <!-- Drawer Content List -->
                <div class="flex-1 overflow-y-auto p-6 space-y-4 custom-scrollbar" id="cart-items-container">
                    <!-- Dynamic Cart Items -->
                </div>

                <!-- Drawer Footer -->
                <div class="p-6 border-t border-slate-200 bg-slate-50 space-y-4">
                    <div class="flex justify-between items-center font-bold text-slate-800 text-sm">
                        <span>Total Items Summary:</span>
                        <span id="cart-total-quantity" class="text-forest-800 font-extrabold text-base">0 Units Across 0 Varieties</span>
                    </div>

                    <button onclick="submitMultiQuoteWhatsApp()" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-3 px-4 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                        <i data-lucide="message-square" class="w-5 h-5"></i> Request Official Quote via WhatsApp
                    </button>
                    <button onclick="clearQuoteCart()" class="w-full bg-slate-200 hover:bg-slate-300 text-slate-700 font-semibold py-2 px-4 rounded-xl text-xs transition-all">
                        Clear Selected Items
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- PLANT DETAIL MODAL -->
    <div id="plant-modal" class="fixed inset-0 z-50 hidden flex items-center justify-center p-4 bg-slate-900/60 backdrop-blur-xs">
        <div class="bg-white w-full max-w-2xl rounded-2xl shadow-2xl overflow-hidden relative animate-in fade-in zoom-in duration-200">
            <button onclick="closePlantModal()" class="absolute top-4 right-4 z-10 bg-slate-900/50 hover:bg-slate-900 text-white p-2 rounded-full transition-colors">
                <i data-lucide="x" class="w-5 h-5"></i>
            </button>
            <div id="modal-body">
                <!-- Modal details rendered dynamically -->
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // MASTER PLANT DATABASE
        const plantCatalog = [
            // FORESTRY & TIMBER
            {
                id: 'teak',
                name: 'Teak Wood (Tectona grandis)',
                category: 'forestry',
                badge: 'Timber Class A',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1542601906990-b4d3fb778b09?auto=format&fit=crop&w=600&q=80',
                desc: 'High-value timber tree renowned for exceptional durability, straight grain, and weather resistance.',
                details: 'Teak is ideal for long-term commercial forestry plantations in Assam soil. Mature trees yield high-grade timber suitable for furniture, construction, and export.'
            },
            {
                id: 'white-sandalwood',
                name: 'White Sandalwood (Santalum album)',
                category: 'forestry',
                badge: 'High Commercial Value',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1513836279014-a89f7a76ae86?auto=format&fit=crop&w=600&q=80',
                desc: 'Aromatic hardwood species prized for sandalwood essential oil and premium wood carving.',
                details: 'Requires host plants like Cajanus cajan or Acacia for initial growth. Excellent long-term investment crop.'
            },
            {
                id: 'red-sandalwood',
                name: 'Red Sandalwood (Pterocarpus santalinus)',
                category: 'forestry',
                badge: 'High Demand Timber',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1502082553048-f009c37129b9?auto=format&fit=crop&w=600&q=80',
                desc: 'Highly prized red wood tree with intense international timber demand.',
                details: 'Grows rapidly in well-drained soils. Drought tolerant once established, providing high security timber yields.'
            },
            {
                id: 'gamari',
                name: 'Gamari / Gmelina arborea',
                category: 'forestry',
                badge: 'Fast Growing Timber',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?auto=format&fit=crop&w=600&q=80',
                desc: 'Fast-growing timber species light in weight, strong, and highly used in carpentry and paneling.',
                details: 'Reaches harvestable size significantly faster than hardwood species. High resistance to decay.'
            },
            {
                id: 'kadam',
                name: 'Kadam (Neolamarckia cadamba)',
                category: 'forestry',
                badge: 'Pulp & Plyboard',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1511497584788-8767611136f6?auto=format&fit=crop&w=600&q=80',
                desc: 'Rapidly growing tree for plyboard manufacturing and shade cover in plantations.',
                details: 'Ideal for boundary planting, paper pulp industry, and quick canopy development.'
            },
            {
                id: 'mahogany',
                name: 'African / Swietenia Mahogany',
                category: 'forestry',
                badge: 'Hardwood Timber',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=600&q=80',
                desc: 'Premium hardwood species producing rich reddish-brown furniture timber.',
                details: 'Extremely popular for commercial forestry. Adaptable to humid sub-tropical conditions.'
            },
            {
                id: 'burma-teak',
                name: 'Burma Teak Variety',
                category: 'forestry',
                badge: 'Premium Grade Timber',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1542601906990-b4d3fb778b09?auto=format&fit=crop&w=600&q=80',
                desc: 'Selected seed variety of Teak known for dense grain structural timber.',
                details: 'Bred for straight vertical trunk formation with minimal branching in plantation setups.'
            },
            {
                id: 'eucalyptus',
                name: 'Hybrid Eucalyptus (Clonal)',
                category: 'forestry',
                badge: 'Short Rotation Crop',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1473448912268-2022ce9509d8?auto=format&fit=crop&w=600&q=80',
                desc: 'High yield clonal eucalyptus for pole timber and paper pulp industries.',
                details: 'Very fast growth cycle, allowing quick financial turnaround for commercial growers.'
            },
            {
                id: 'subabul',
                name: 'Subabul (Leucaena leucocephala)',
                category: 'forestry',
                badge: 'Fodder & Biomass',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1500382017468-9049fed747ef?auto=format&fit=crop&w=600&q=80',
                desc: 'Multi-purpose nitrogen-fixing leguminous tree used for biomass, fodder, and soil improvement.',
                details: 'Rapid biomass production makes it ideal for soil regeneration and bio-energy plantations.'
            },
            {
                id: 'bamboo-tulda',
                name: 'Jati Bamboo (Bambusa tulda)',
                category: 'forestry',
                badge: 'Commercial Bamboo',
                unit: 'rhizome / seedling',
                img: 'https://images.unsplash.com/photo-1516214104703-d870798883c5?auto=format&fit=crop&w=600&q=80',
                desc: 'The essential commercial bamboo of Assam used for construction, scaffolding, and handicrafts.',
                details: 'Strong, thick-walled culms with high structural integrity and rapid regrowth post harvest.'
            },
            {
                id: 'bamboo-strictus',
                name: 'Solid Bamboo (Dendrocalamus strictus)',
                category: 'forestry',
                badge: 'Heavy Structural',
                unit: 'rhizome / seedling',
                img: 'https://images.unsplash.com/photo-1508873696983-2df515122519?auto=format&fit=crop&w=600&q=80',
                desc: 'Male bamboo variety with nearly solid culms, ideal for heavy construction and structural poles.',
                details: 'Drought-hardy variety suitable for rocky or degraded soils across North-East India.'
            },
            {
                id: 'sal-tree',
                name: 'Sal Tree (Shorea robusta)',
                category: 'forestry',
                badge: 'Native Hardwood',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=600&q=80',
                desc: 'Dense structural hardwood native to Northeast forests, producing high-grade railway and beam timber.',
                details: 'Extremely durable hardwood resistant to termite attacks.'
            },
            {
                id: 'hollong',
                name: 'Hollong (Dipterocarpus retusus)',
                category: 'forestry',
                badge: 'Assam State Tree',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1511497584788-8767611136f6?auto=format&fit=crop&w=600&q=80',
                desc: 'Tall majestic timber tree, famous as the official State Tree of Assam and vital for ply timber.',
                details: 'Grows into impressive tall straight trunks; ideal for ecological conservation and forestry.'
            },
            {
                id: 'neem',
                name: 'Neem Tree (Azadirachta indica)',
                category: 'forestry',
                badge: 'Medicinal & Timber',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1500382017468-9049fed747ef?auto=format&fit=crop&w=600&q=80',
                desc: 'Hardy tree with natural pest-repellent properties, bio-pesticide raw material, and durable wood.',
                details: 'Improves surrounding air quality and soil health while providing medicinal leaves and seed oil.'
            },

            // FRUIT-BEARING SAPLINGS
            {
                id: 'macadamia',
                name: 'Grafted Macadamia Nut',
                category: 'fruit',
                badge: 'High Value Exotic',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1599599810769-bcde5a160d32?auto=format&fit=crop&w=600&q=80',
                desc: 'Commercial nut variety with exceptional yield potential in Northeast agro-climates.',
                details: 'Grafted stocks ensure early fruiting within 3 to 4 years. Produces high-value gourmet nuts.'
            },
            {
                id: 'avocado',
                name: 'Hass & Lamb Hass Avocado',
                category: 'fruit',
                badge: 'Grafted Premium',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1523049673857-eb18f1d7b578?auto=format&fit=crop&w=600&q=80',
                desc: 'High demand nutrient-dense fruit adapted for warm humid conditions.',
                details: 'Grafted from heavy-bearing mother plants. Highly suitable for commercial orchards in Assam.'
            },
            {
                id: 'khasi-mandarin',
                name: 'Khasi Mandarin Orange',
                category: 'fruit',
                badge: 'Regional Specialty',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1611080626919-7cf5a9dbab5b?auto=format&fit=crop&w=600&q=80',
                desc: 'Famous juicy sweet citrus variety endemic to Northeast India.',
                details: 'High sugar content and distinct flavor profile. Certified disease-free budded stock.'
            },
            {
                id: 'areca-nut',
                name: 'Areca Nut / Supari (High Yield)',
                category: 'fruit',
                badge: 'Cash Crop Staple',
                unit: 'seedling',
                img: 'https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=600&q=80',
                desc: 'Selected mother-palm seeds for heavy cluster production.',
                details: 'Essential cash crop for Assam farmers with dependable annual harvest returns.'
            },
            {
                id: 'hrmn-apple',
                name: 'HRMN-99 Low-Chill Apple',
                category: 'fruit',
                badge: 'Warm Climate Variety',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1560806887-1e4cd0b6cbd6?auto=format&fit=crop&w=600&q=80',
                desc: 'Special low-chill apple variety engineered to fruit in plain and warm climates.',
                details: 'Does not require intense winter chilling. Fruits reliably in Assam plains and foothills.'
            },
            {
                id: 'mango-amrapali',
                name: 'Amrapali Grafted Mango',
                category: 'fruit',
                badge: 'High Yield Dwarf',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1553279768-865429fa0078?auto=format&fit=crop&w=600&q=80',
                desc: 'Dwarf grafted mango variety known for sweet deep-orange pulp and heavy bearing.',
                details: 'Ideal for high-density orchard planting where space efficiency is required.'
            },
            {
                id: 'mango-miyazaki',
                name: 'Miyazaki Japanese Mango',
                category: 'fruit',
                badge: 'Exotic Premium',
                unit: 'grafted sapling',
                img: 'https://images.unsplash.com/photo-1591073113125-e46713c829ed?auto=format&fit=crop&w=600&q=80',
                desc: 'World famous ruby-red luxury mango variety with exceptionally high sugar content.',
                details: 'Grafted from verified mother plants. High potential exotic crop for fruit enthusiasts.'
            },
            {
                id: 'rambutan',
                name: 'Grafted Rambutan',
                category: 'fruit',
                badge: 'Exotic Tropical',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1567306226416-28f0efdc88ce?auto=format&fit=crop&w=600&q=80',
                desc: 'Tropical fruit tree bearing sweet, juicy hairy-shelled red fruits in clusters.',
                details: 'Thrives in humid tropical climates like Assam with consistent rainfall.'
            },
            {
                id: 'dragon-fruit',
                name: 'Red & White Dragon Fruit',
                category: 'fruit',
                badge: 'Commercial Cactus',
                unit: 'cutting / rooted plant',
                img: 'https://images.unsplash.com/photo-1527325678964-549216468488?auto=format&fit=crop&w=600&q=80',
                desc: 'High-earning climbing vine fruit with antioxidant-rich flesh.',
                details: 'Requires trellis support. Early fruiting within 12-18 months of establishment.'
            },
            {
                id: 'guava-thai',
                name: 'Thai Pink & L-49 Guava',
                category: 'fruit',
                badge: 'Heavy Bearing',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1536511135890-53b6d2e67f2e?auto=format&fit=crop&w=600&q=80',
                desc: 'Large-sized crispy guava varieties with small seed cores and sweet aromatic flesh.',
                details: 'Yields fruit multiple times a year under good irrigation management.'
            },
            {
                id: 'litchi-shahi',
                name: 'Shahi & Bombai Litchi',
                category: 'fruit',
                badge: 'Juicy Summer Fruit',
                unit: 'air-layered sapling',
                img: 'https://images.unsplash.com/photo-1543528176-a17a57939ab8?auto=format&fit=crop&w=600&q=80',
                desc: 'Famous juicy sweet litchi varieties adapted for Assam alluvial soils.',
                details: 'Propagated through air-layering (Gootee) to guarantee early fruiting and variety purity.'
            },
            {
                id: 'jackfruit-allseason',
                name: 'All-Season Grafted Jackfruit',
                category: 'fruit',
                badge: 'Continuous Bearing',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1587049352847-4a222e784d38?auto=format&fit=crop&w=600&q=80',
                desc: 'Special grafted variety yielding medium-sized jackfruit almost round the year.',
                details: 'Dwarf growth habit allowing easy harvesting without climbing tall trees.'
            },
            {
                id: 'kazi-nemi',
                name: 'Assam Kazi Nemi / Lemon',
                category: 'fruit',
                badge: 'GI Tagged Favorite',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1534531141161-e4ecc2c77607?auto=format&fit=crop&w=600&q=80',
                desc: 'Aromatic oblong lemon unique to Assam with distinct citrus fragrance and juice.',
                details: 'High market demand across local and national markets. Continuous flowering variety.'
            },

            // INDOOR & LANDSCAPING
            {
                id: 'snake-plant',
                name: 'Snake Plant (Sansevieria)',
                category: 'indoor',
                badge: 'Air Purifying',
                unit: 'potted / root clump',
                img: 'https://images.unsplash.com/photo-1509423350716-97f9360b4e09?auto=format&fit=crop&w=600&q=80',
                desc: 'Hardy indoor ornamental plant requiring minimal maintenance and indirect sunlight.',
                details: 'Removes indoor toxins like benzene and formaldehyde. Perfect for corporate office landscaping.'
            },
            {
                id: 'zz-plant',
                name: 'ZZ Plant (Zamioculcas zamiifolia)',
                category: 'indoor',
                badge: 'Low Light Hardy',
                unit: 'potted',
                img: 'https://images.unsplash.com/photo-1632207691143-643e2a9a9361?auto=format&fit=crop&w=600&q=80',
                desc: 'Glossy dark green foliage that thrives in low light indoor environments.',
                details: 'Drought tolerant and resistant to common pests. Great decorative appeal for interiors.'
            },
            {
                id: 'peace-lily',
                name: 'Peace Lily (Spathiphyllum)',
                category: 'indoor',
                badge: 'Flowering Shade',
                unit: 'potted',
                img: 'https://images.unsplash.com/photo-1593691509543-c55fb32e7355?auto=format&fit=crop&w=600&q=80',
                desc: 'Elegantly blooming shade plant with striking white spathes.',
                details: 'Ideal for indoor lobbies, homes, and shaded landscaped gardens.'
            },
            {
                id: 'areca-palm',
                name: 'Areca Palm (Indoor/Outdoor)',
                category: 'indoor',
                badge: 'Landscape Favorite',
                unit: 'potted / cluster',
                img: 'https://images.unsplash.com/photo-1545241047-6083a3684587?auto=format&fit=crop&w=600&q=80',
                desc: 'Feathery green fronds providing lush tropical aesthetic for avenues, homes, and gardens.',
                details: 'Acts as natural humidifier and air purifier. Fast-growing landscape ornamental.'
            },
            {
                id: 'money-plant',
                name: 'Golden Pothos / Money Plant',
                category: 'indoor',
                badge: 'Easy Care Vine',
                unit: 'potted / vine',
                img: 'https://images.unsplash.com/photo-1614594975525-e45190c55d0b?auto=format&fit=crop&w=600&q=80',
                desc: 'Vibrant green and yellow variegated foliage climber for indoor walls and desks.',
                details: 'Extremely resilient indoor plant that grows well in both soil and water containers.'
            },
            {
                id: 'monstera',
                name: 'Monstera Deliciosa (Swiss Cheese)',
                category: 'indoor',
                badge: 'Modern Interior Decorative',
                unit: 'potted',
                img: 'https://images.unsplash.com/photo-1617173944883-6ffbd35d584d?auto=format&fit=crop&w=600&q=80',
                desc: 'Iconic wide leaves with natural split perforations, highly popular for aesthetic interiors.',
                details: 'Thrives in bright indirect light with moderate watering.'
            },
            {
                id: 'song-of-india',
                name: 'Song of India (Dracaena reflexa)',
                category: 'indoor',
                badge: 'Ornamental Shrub',
                unit: 'potted',
                img: 'https://images.unsplash.com/photo-1512428559087-560fa5ceab42?auto=format&fit=crop&w=600&q=80',
                desc: 'Eye-catching yellow-green striped foliage suitable for garden borders and indoor pots.',
                details: 'Slow-growing compact ornamental that retains its bright colors year round.'
            },

            // MEDICINAL & HIGH-VALUE
            {
                id: 'agarwood',
                name: 'Agarwood / Xylocarp (Aquilaria malaccensis)',
                category: 'medicinal',
                badge: 'Assam Oud Speciality',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=600&q=80',
                desc: 'Famous fragrant resin-producing tree native to Assam & Northeast India.',
                details: 'Produces valuable Oud resin after natural or artificial fungal inoculation. Dewdrop provides authentic nursery-hardened seedlings.'
            },
            {
                id: 'tulsi',
                name: 'Holy Basil / Shyama Tulsi',
                category: 'medicinal',
                badge: 'Ayurvedic Herb',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1615485290382-441e4d049cb5?auto=format&fit=crop&w=600&q=80',
                desc: 'Revered medicinal herb rich in essential oils and immunity boosting properties.',
                details: 'Essential plant for medicinal gardens, herbal extraction, and sacred home gardens.'
            },
            {
                id: 'ashwagandha',
                name: 'Ashwagandha (Withania somnifera)',
                category: 'medicinal',
                badge: 'Adaptogenic Herb',
                unit: 'seedling',
                img: 'https://images.unsplash.com/photo-1509423350716-97f9360b4e09?auto=format&fit=crop&w=600&q=80',
                desc: 'Vital Ayurvedic shrub grown for its restorative roots and wellness benefits.',
                details: 'Requires well-drained soil and full sunlight. High demand in pharmaceutical sectors.'
            },

            // SERICULTURE & SPICES
            {
                id: 'mulberry',
                name: 'Mulberry Saplings (Sericulture Grade)',
                category: 'sericulture',
                badge: 'Silk Worm Host',
                unit: 'cutting / sapling',
                img: 'https://images.unsplash.com/photo-1500382017468-9049fed747ef?auto=format&fit=crop&w=600&q=80',
                desc: 'High leaf yield mulberry selection engineered for Eri & Mulberry silkworm rearing.',
                details: 'Produces lush foliage suitable for continuous harvesting for silk farmers.'
            },
            {
                id: 'som-plant',
                name: 'Som Plant (Machilus bombycina)',
                category: 'sericulture',
                badge: 'Muga Silk Host Tree',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=600&q=80',
                desc: 'Primary food plant tree for the world famous Assam Golden Muga Silkworm.',
                details: 'Crucial forestry species for sericulture development across Assam.'
            },
            {
                id: 'soalu-plant',
                name: 'Soalu Plant (Litsea polyantha)',
                category: 'sericulture',
                badge: 'Muga Silk Host Variety',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?auto=format&fit=crop&w=600&q=80',
                desc: 'Secondary primary host plant for Muga silkworm culture with rapid leaf production.',
                details: 'Adaptable to various soil types across valley and hill regions of Northeast India.'
            },
            {
                id: 'black-pepper',
                name: 'Panniyur-1 Black Pepper Vine',
                category: 'sericulture',
                badge: 'High Yield Spice',
                unit: 'rooted vine',
                img: 'https://images.unsplash.com/photo-1599599810769-bcde5a160d32?auto=format&fit=crop&w=600&q=80',
                desc: 'High yielding black pepper variety ideal for intercropping on Areca nut or Teak trees.',
                details: 'Double crop potential by trailing vines on existing timber or nut tree trunks.'
            },
            {
                id: 'cardamom',
                name: 'Bhutan & Large Cardamom',
                category: 'sericulture',
                badge: 'Shade Spice',
                unit: 'sucker / seedling',
                img: 'https://images.unsplash.com/photo-1509423350716-97f9360b4e09?auto=format&fit=crop&w=600&q=80',
                desc: 'Aromatic spice crop thriving under forest canopy and shade tree plantations.',
                details: 'Ideal high-value understory crop for agro-forestry setups in Northeast India.'
            },
            {
                id: 'cinnamon',
                name: 'Cinnamon / Dalchini Plant',
                category: 'sericulture',
                badge: 'Aromatic Spice Tree',
                unit: 'sapling',
                img: 'https://images.unsplash.com/photo-1513836279014-a89f7a76ae86?auto=format&fit=crop&w=600&q=80',
                desc: 'Tree cultivated for fragrant inner bark and cinnamon essential leaf oil.',
                details: 'Evergreen spice tree suitable for mixed commercial orchards.'
            }
        ];

        // STATE MANAGEMENT
        let currentCategory = 'all';
        let quoteCart = [];

        // INITIALIZE APP
        document.addEventListener('DOMContentLoaded', () => {
            renderPlantCatalog();
            populateCalcSelect();
            updateCalcPreview();
            lucide.createIcons();
        });

        // RENDER CATALOG
        function renderPlantCatalog() {
            const grid = document.getElementById('plant-grid');
            const searchVal = document.getElementById('catalog-search').value.toLowerCase();
            const noResults = document.getElementById('no-results');

            grid.innerHTML = '';
            let count = 0;

            plantCatalog.forEach(plant => {
                const matchesCat = (currentCategory === 'all' || plant.category === currentCategory);
                const matchesSearch = plant.name.toLowerCase().includes(searchVal) || plant.desc.toLowerCase().includes(searchVal);

                if (matchesCat && matchesSearch) {
                    count++;
                    const card = document.createElement('div');
                    card.className = 'bg-white rounded-2xl border border-slate-200 overflow-hidden shadow-xs hover:shadow-lg transition-all duration-300 flex flex-col justify-between group';
                    card.innerHTML = `
                        <div>
                            <div class="relative h-48 overflow-hidden bg-slate-100">
                                <img src="${plant.img}" alt="${plant.name}" 
                                     class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
                                     onerror="this.src='https://placehold.co/600x400/2d6a4f/ffffff?text=${encodeURIComponent(plant.name)}'">
                                <span class="absolute top-3 left-3 bg-forest-800/90 text-emerald-200 text-[11px] font-bold px-2.5 py-1 rounded-md backdrop-blur-xs">
                                    ${plant.badge}
                                </span>
                                <span class="absolute bottom-3 right-3 bg-white/90 text-slate-800 text-[11px] font-bold px-2.5 py-1 rounded-md shadow-xs border border-slate-200">
                                    Unit: ${plant.unit}
                                </span>
                            </div>
                            <div class="p-5">
                                <h3 class="font-bold text-slate-800 text-base group-hover:text-forest-700 transition-colors">${plant.name}</h3>
                                <p class="text-xs text-slate-500 mt-2 line-clamp-2 leading-relaxed">${plant.desc}</p>
                            </div>
                        </div>
                        <div class="p-5 pt-0 flex items-center gap-2">
                            <button onclick="openPlantModal('${plant.id}')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-semibold py-2.5 rounded-xl transition-colors">
                                View Details
                            </button>
                            <button onclick="quickAddToCart('${plant.id}')" class="bg-forest-800 hover:bg-forest-700 text-white p-2.5 rounded-xl transition-colors shadow-xs" title="Add to Inquiry List">
                                <i data-lucide="plus" class="w-4 h-4"></i>
                            </button>
                        </div>
                    `;
                    grid.appendChild(card);
                }
            });

            if (count === 0) {
                noResults.classList.remove('hidden');
            } else {
                noResults.classList.add('hidden');
            }
            lucide.createIcons();
        }

        // CATEGORY FILTERING
        function setCategory(cat) {
            currentCategory = cat;
            document.querySelectorAll('.cat-btn').forEach(btn => {
                btn.className = 'cat-btn bg-white hover:bg-slate-100 text-slate-700 border border-slate-200 px-4 py-2 rounded-xl text-sm font-medium whitespace-nowrap transition-colors';
            });
            const activeBtn = document.getElementById(`cat-${cat}`);
            if (activeBtn) {
                activeBtn.className = 'cat-btn bg-forest-800 text-white px-4 py-2 rounded-xl text-sm font-semibold whitespace-nowrap transition-colors shadow-xs';
            }
            renderPlantCatalog();
        }

        function filterPlants() {
            renderPlantCatalog();
        }

        // POPULATE CALCULATOR SELECT OPTIONS
        function populateCalcSelect() {
            const select = document.getElementById('calc-plant-select');
            select.innerHTML = '';
            plantCatalog.forEach(plant => {
                const opt = document.createElement('option');
                opt.value = plant.id;
                opt.textContent = `${plant.name} (${plant.unit})`;
                select.appendChild(opt);
            });
        }

        // CALCULATOR PREVIEW
        function getCalcState() {
            const plantId = document.getElementById('calc-plant-select').value;
            const plant = plantCatalog.find(p => p.id === plantId) || plantCatalog[0];
            const qty = Math.max(1, parseInt(document.getElementById('calc-qty').value) || 100);
            const stage = document.getElementById('calc-stage').value;
            const region = document.getElementById('calc-region').value;

            return { plant, qty, stage, region };
        }

        function updateCalcPreview() {
            const state = getCalcState();
            document.getElementById('summary-plant-name').textContent = state.plant.name;
            document.getElementById('summary-qty').textContent = `${state.qty} ${state.plant.unit}s`;
            document.getElementById('summary-stage').textContent = state.stage;
            document.getElementById('summary-region').textContent = state.region;
        }

        // CALCULATOR WHATSAPP DIRECT SEND
        function sendCalcToWhatsApp() {
            const state = getCalcState();
            const msg = `Hello Dewdrop Nursery,%0A%0AI would like to request an official wholesale price quotation for:%0A- Variety: ${encodeURIComponent(state.plant.name)}%0A- Quantity: ${state.qty} ${state.plant.unit}s%0A- Plant Stage: ${encodeURIComponent(state.stage)}%0A- Delivery Location: ${encodeURIComponent(state.region)}%0A%0APlease provide stock availability and official pricing options. Thank you!`;
            window.open(`https://wa.me/919707467445?text=${msg}`, '_blank');
        }

        function copyQuoteToClipboard() {
            const state = getCalcState();
            const text = `Dewdrop Nursery Plant Requirement Inquiry:\nPlant Variety: ${state.plant.name}\nQuantity: ${state.qty} ${state.plant.unit}s\nPlant Form: ${state.stage}\nDestination: ${state.region}\nAddress: Lanka, Hojai, Assam | Ph: +91 97074 67445`;
            
            const tempInput = document.createElement('textarea');
            tempInput.value = text;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);

            showToast('Requirement details copied to clipboard!');
        }

        // QUOTE CART SYSTEM
        function quickAddToCart(plantId) {
            const plant = plantCatalog.find(p => p.id === plantId);
            if (!plant) return;

            const existing = quoteCart.find(item => item.id === plantId);
            if (existing) {
                existing.qty += 50;
            } else {
                quoteCart.push({
                    id: plant.id,
                    name: plant.name,
                    qty: 50,
                    unit: plant.unit
                });
            }
            updateCartUI();
            toggleCartDrawer(true);
            showToast(`Added ${plant.name} to inquiry list!`);
        }

        function addCurrentCalcToCart() {
            const state = getCalcState();
            const existing = quoteCart.find(item => item.id === state.plant.id);
            if (existing) {
                existing.qty += state.qty;
            } else {
                quoteCart.push({
                    id: state.plant.id,
                    name: state.plant.name,
                    qty: state.qty,
                    unit: state.plant.unit
                });
            }
            updateCartUI();
            toggleCartDrawer(true);
            showToast(`Added to inquiry list!`);
        }

        function updateCartUI() {
            const badge = document.getElementById('cart-badge');
            const badgeMobile = document.getElementById('cart-badge-mobile');
            const container = document.getElementById('cart-items-container');
            const totalQtyEl = document.getElementById('cart-total-quantity');

            const totalQuantity = quoteCart.reduce((sum, item) => sum + item.qty, 0);
            
            if (quoteCart.length > 0) {
                badge.classList.remove('hidden');
                badgeMobile.classList.remove('hidden');
                badge.textContent = quoteCart.length;
                badgeMobile.textContent = quoteCart.length;
            } else {
                badge.classList.add('hidden');
                badgeMobile.classList.add('hidden');
            }

            container.innerHTML = '';

            if (quoteCart.length === 0) {
                container.innerHTML = `
                    <div class="text-center py-12 text-slate-400">
                        <i data-lucide="clipboard-list" class="w-12 h-12 mx-auto mb-3 text-slate-300"></i>
                        <p class="font-medium">Your inquiry list is empty.</p>
                        <p class="text-xs text-slate-400 mt-1">Add plants from the catalog to request pricing.</p>
                    </div>
                `;
            } else {
                quoteCart.forEach((item, index) => {
                    const div = document.createElement('div');
                    div.className = 'bg-slate-50 border border-slate-200 rounded-xl p-4 flex items-center justify-between gap-3';
                    div.innerHTML = `
                        <div class="flex-1">
                            <h4 class="font-bold text-slate-800 text-sm">${item.name}</h4>
                            <div class="text-xs text-slate-500 mt-0.5">Unit type: ${item.unit}</div>
                        </div>
                        <div class="flex items-center gap-2">
                            <input type="number" min="10" step="10" value="${item.qty}" onchange="updateCartItemQty(${index}, this.value)"
                                   class="w-16 bg-white border border-slate-300 rounded-lg text-center text-xs p-1">
                            <button onclick="removeCartItem(${index})" class="text-red-500 hover:text-red-700 p-1" title="Remove">
                                <i data-lucide="trash-2" class="w-4 h-4"></i>
                            </button>
                        </div>
                    `;
                    container.appendChild(div);
                });
            }

            totalQtyEl.textContent = `${totalQuantity.toLocaleString('en-IN')} Units across ${quoteCart.length} Varieties`;
            lucide.createIcons();
        }

        function updateCartItemQty(index, qty) {
            const val = parseInt(qty);
            if (val > 0) {
                quoteCart[index].qty = val;
                updateCartUI();
            }
        }

        function removeCartItem(index) {
            quoteCart.splice(index, 1);
            updateCartUI();
        }

        function clearQuoteCart() {
            quoteCart = [];
            updateCartUI();
        }

        function submitMultiQuoteWhatsApp() {
            if (quoteCart.length === 0) {
                alert('Your requirement list is empty. Please add items before submitting.');
                return;
            }

            let text = `Hello Dewdrop Nursery,%0A%0AI would like to request an official wholesale price quotation for the following plant requirements:%0A`;

            quoteCart.forEach((item, idx) => {
                text += `${idx + 1}. ${encodeURIComponent(item.name)} - ${item.qty} ${item.unit}s%0A`;
            });

            text += `%0APlease share stock availability, estimated pricing, and delivery schedule. Thank you!`;
            window.open(`https://wa.me/919707467445?text=${text}`, '_blank');
        }

        function toggleCartDrawer(open) {
            const drawer = document.getElementById('cart-drawer');
            if (open === true) {
                drawer.classList.remove('hidden');
            } else if (open === false) {
                drawer.classList.add('hidden');
            } else {
                drawer.classList.toggle('hidden');
            }
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        // PLANT MODAL
        function openPlantModal(plantId) {
            const plant = plantCatalog.find(p => p.id === plantId);
            if (!plant) return;

            const modalBody = document.getElementById('modal-body');
            modalBody.innerHTML = `
                <div class="grid grid-cols-1 md:grid-cols-2">
                    <div class="h-64 md:h-full bg-slate-100 relative">
                        <img src="${plant.img}" alt="${plant.name}" class="w-full h-full object-cover"
                             onerror="this.src='https://placehold.co/600x600/2d6a4f/ffffff?text=${encodeURIComponent(plant.name)}'">
                        <span class="absolute top-4 left-4 bg-forest-800 text-emerald-200 text-xs font-bold px-3 py-1 rounded-md">
                            ${plant.badge}
                        </span>
                    </div>
                    <div class="p-6 md:p-8 flex flex-col justify-between space-y-4">
                        <div>
                            <span class="text-xs font-bold text-forest-600 uppercase tracking-wider">${plant.category} category</span>
                            <h3 class="text-xl font-bold text-slate-900 mt-1">${plant.name}</h3>
                            <div class="text-xs text-slate-500 font-semibold mt-1">Available Form: ${plant.unit}</div>
                            <p class="text-slate-600 text-xs mt-3 leading-relaxed">${plant.details}</p>
                        </div>
                        <div class="space-y-2 pt-4 border-t border-slate-100">
                            <button onclick="quickAddToCart('${plant.id}'); closePlantModal();" class="w-full bg-forest-800 hover:bg-forest-700 text-white font-bold py-3 px-4 rounded-xl text-xs shadow-md transition-all flex items-center justify-center gap-2">
                                <i data-lucide="plus-circle" class="w-4 h-4"></i> Add to Requirement List
                            </button>
                            <a href="https://wa.me/919707467445?text=Hello%20Dewdrop%20Nursery,%20I%20would%20like%20to%20inquire%20about%20pricing%20and%20stock%20for%20${encodeURIComponent(plant.name)}" 
                               target="_blank" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-2.5 px-4 rounded-xl text-xs transition-all text-center block">
                                Inquire Stock via WhatsApp
                            </a>
                        </div>
                    </div>
                </div>
            `;
            document.getElementById('plant-modal').classList.remove('hidden');
            lucide.createIcons();
        }

        function closePlantModal() {
            document.getElementById('plant-modal').classList.add('hidden');
        }

        // CONTACT FORM SUBMISSION
        function handleFormSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('form-name').value;
            const phone = document.getElementById('form-phone').value;
            const location = document.getElementById('form-location').value;
            const category = document.getElementById('form-category').value;
            const msg = document.getElementById('form-message').value;

            const waText = `Hello Dewdrop Nursery,%0A%0AInquiry from Website Form:%0A- Name: ${encodeURIComponent(name)}%0A- Phone: ${encodeURIComponent(phone)}%0A- Location: ${encodeURIComponent(location)}%0A- Category: ${encodeURIComponent(category)}%0A- Requirements: ${encodeURIComponent(msg)}`;
            window.open(`https://wa.me/919707467445?text=${waText}`, '_blank');
        }

        // TOAST NOTIFICATION HELPER
        function showToast(message) {
            const toast = document.createElement('div');
            toast.className = 'fixed bottom-5 right-5 z-50 bg-slate-900 text-white text-xs font-semibold px-4 py-3 rounded-xl shadow-xl border border-slate-700 animate-in slide-in-from-bottom duration-300 flex items-center gap-2';
            toast.innerHTML = `<i data-lucide="check-circle" class="w-4 h-4 text-emerald-400"></i> ${message}`;
            document.body.appendChild(toast);
            lucide.createIcons();

            setTimeout(() => {
                toast.classList.add('opacity-0');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }
    </script>
</body>
</html>
```
