# Relex-bioskop
Bioskop
<!DOCTYPE html>
<html lang="id" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RELEX BIOSKOP - Cinema Food & Merchandise</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Rajdhani:wght@500;600;700&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            cyan: '#00f2fe',
                            pink: '#ff007f',
                            purple: '#7928ca',
                            dark: '#080914',
                            card: '#121426',
                            border: '#1f2442'
                        }
                    },
                    fontFamily: {
                        orbitron: ['Orbitron', 'sans-serif'],
                        rajdhani: ['Rajdhani', 'sans-serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        .neon-border-cyan { box-shadow: 0 0 15px rgba(0, 242, 254, 0.3); border-color: #00f2fe; }
        .neon-border-pink { box-shadow: 0 0 15px rgba(255, 0, 127, 0.3); border-color: #ff007f; }
        .neon-text-cyan { text-shadow: 0 0 10px rgba(0, 242, 254, 0.5); }
        .neon-text-pink { text-shadow: 0 0 10px rgba(255, 0, 127, 0.5); }
        .bg-gradient-neon { background: linear-gradient(135deg, #00f2fe 0%, #4facfe 30%, #7928ca 70%, #ff007f 100%); }
        .text-gradient-neon {
            background: linear-gradient(135deg, #00f2fe 0%, #ff007f 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>
<body class="bg-[#060710] text-gray-100 font-sans antialiased min-h-screen flex flex-col selection:bg-brand-pink selection:text-white pb-24 md:pb-8">
    <!-- HEADER & NAVBAR -->
    <header class="sticky top-0 z-40 bg-[#060710]/90 backdrop-blur-md border-b border-brand-border/60">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-xl bg-gradient-neon p-[2px] flex items-center justify-center shadow-[0_0_15px_rgba(0,242,254,0.4)]">
                    <div class="w-full h-full bg-brand-dark rounded-[10px] flex items-center justify-center">
                        <i class="fa-solid font-bold text-transparent bg-clip-text bg-gradient-to-r from-brand-cyan to-brand-pink font-orbitron text-xl">R</i>
                    </div>
                </div>
                <div>
                    <h1 class="font-orbitron font-extrabold text-2xl tracking-wider text-transparent bg-clip-text bg-gradient-to-r from-brand-cyan via-white to-brand-pink">
                        RELEX
                    </h1>
                    <p class="font-rajdhani tracking-[0.2em] text-xs text-brand-cyan font-semibold -mt-1">BIOSKOP</p>
                </div>
            </div>
            <div class="hidden md:flex items-center gap-6">
                <a href="#menu" class="text-sm font-medium text-gray-300 hover:text-brand-cyan transition-colors">Menu A la Carte</a>
                <a href="#kombo" class="text-sm font-medium text-gray-300 hover:text-brand-pink transition-colors">Paket Kombo</a>
                <a href="#info" class="text-sm font-medium text-gray-300 hover:text-brand-cyan transition-colors">Layanan Studio</a>
            </div>
            <button onclick="toggleCart()" class="relative bg-brand-card hover:bg-brand-border border border-brand-cyan/40 px-4 py-2.5 rounded-xl transition-all duration-300 flex items-center gap-3 shadow-[0_0_10px_rgba(0,242,254,0.15)] group">
                <i class="fa-solid fa-cart-shopping text-brand-cyan group-hover:scale-110 transition-transform"></i>
                <span class="font-rajdhani font-bold text-sm hidden sm:inline">PESANAN</span>
                <span id="cart-count" class="bg-gradient-to-r from-brand-cyan to-brand-pink text-black font-extrabold text-xs px-2 py-0.5 rounded-full">0</span>
            </button>
        </div>
    </header>
    <!-- HERO BANNER -->
    <section class="relative overflow-hidden py-12 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto w-full">
        <div class="absolute -top-24 -left-24 w-72 h-72 bg-brand-cyan/10 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute top-1/2 -right-24 w-80 h-80 bg-brand-pink/10 rounded-full blur-3xl pointer-events-none"></div>
        <div class="relative bg-gradient-to-r from-brand-card to-[#181b36] border border-brand-border/80 rounded-3xl p-6 md:p-10 flex flex-col md:flex-row items-center justify-between gap-8 shadow-2xl">
            <div class="space-y-4 max-w-xl text-center md:text-left">
                <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-brand-cyan/10 border border-brand-cyan/30 text-brand-cyan text-xs font-semibold tracking-wider uppercase">
                    <i class="fa-solid fa-clapperboard"></i> More Than Just A Movie
                </div>
                <h2 class="text-3xl md:text-5xl font-orbitron font-bold text-white leading-tight">
                    Nikmati Camilan & Merchandise <span class="text-gradient-neon">Eksklusif</span>
                </h2>
                <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                    Pesan Popcorn segar, minuman dingin, hingga merchandise resmi RELEX BIOSKOP langsung diantar ke kursi studio Anda!
                </p>
            </div>          
           <div class="grid grid-cols-3 gap-3 w-full md:w-auto">
                <div class="bg-brand-dark/80 border border-brand-border p-4 rounded-2xl text-center">
                    <i class="fa-solid fa-utensils text-brand-cyan text-xl mb-2"></i>
                    <p class="font-orbitron text-xs font-bold text-gray-200">Rasa Lezat</p>
                </div>
                <div class="bg-brand-dark/80 border border-brand-border p-4 rounded-2xl text-center">
                    <i class="fa-solid fa-star text-brand-pink text-xl mb-2"></i>
                    <p class="font-orbitron text-xs font-bold text-gray-200">Kualitas Terbaik</p>
                </div>
                <div class="bg-brand-dark/80 border border-brand-border p-4 rounded-2xl text-center">
                    <i class="fa-solid fa-film text-brand-cyan text-xl mb-2"></i>
                    <p class="font-orbitron text-xs font-bold text-gray-200">Pengalaman Seru</p>
                </div>
            </div>
        </div>
    </section>
    <!-- MAIN CONTENT -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 w-full flex-grow">
        <!-- FILTER TABS -->
        <div id="menu" class="flex items-center gap-2 overflow-x-auto pb-4 mb-8 scrollbar-none">
            <button onclick="filterCategory(event, 'all')" class="cat-btn active bg-brand-cyan text-black font-bold px-5 py-2.5 rounded-xl text-sm whitespace-nowrap transition-all">
                Semua Menu
            </button>
            <button onclick="filterCategory(event, 'popcorn')" class="cat-btn bg-brand-card hover:bg-brand-border text-gray-300 font-semibold px-5 py-2.5 rounded-xl text-sm whitespace-nowrap transition-all border border-brand-border">
                🍿 Popcorn
            </button>
            <button onclick="filterCategory(event, 'minuman')" class="cat-btn bg-brand-card hover:bg-brand-border text-gray-300 font-semibold px-5 py-2.5 rounded-xl text-sm whitespace-nowrap transition-all border border-brand-border">
                🥤 Minuman
            </button>
            <button onclick="filterCategory(event, 'snack')" class="cat-btn bg-brand-card hover:bg-brand-border text-gray-300 font-semibold px-5 py-2.5 rounded-xl text-sm whitespace-nowrap transition-all border border-brand-border">
                🌭 Makanan & Snack
            </button>
            <button onclick="filterCategory(event, 'merch')" class="cat-btn bg-brand-card hover:bg-brand-border text-gray-300 font-semibold px-5 py-2.5 rounded-xl text-sm whitespace-nowrap transition-all border border-brand-border">
                🧢 Merchandise
            </button>
        </div>
        <!-- ITEMS GRID -->
        <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4 md:gap-6" id="menu-grid">            <!-- Dynamic Content loaded by JS -->
        </div>
        <!-- PAKET KOMBO SECTION -->
        <div id="kombo" class="mt-16 pt-8 border-t border-brand-border">
            <div class="flex items-center gap-3 mb-6">
                <div class="w-3 h-8 bg-gradient-to-b from-brand-cyan to-brand-pink rounded-full"></div>
                <h3 class="font-orbitron font-bold text-2xl text-white tracking-wide">PAKET KOMBO SPECIAL</h3>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="combo-grid">
                <!-- Combo items loaded by JS -->
            </div>
        </div>
    </main>
    <!-- FOOTER -->
    <footer id="info" class="mt-auto bg-brand-dark border-t border-brand-border/60 py-8 text-center text-gray-500 text-xs">
        <div class="max-w-7xl mx-auto px-4">
            <p class="font-orbitron text-gray-400 mb-2">&copy; 2026 RELEX BIOSKOP. All Rights Reserved.</p>
            <p>Sistem Pemesanan Makanan & Merchandise Bioskop Online</p>
        </div>
    </footer>
    <!-- CART SIDEBAR DRAWER -->
    <div id="cart-drawer" class="fixed inset-0 z-50 overflow-hidden hidden">
        <div onclick="toggleCart()" class="absolute inset-0 bg-black/70 backdrop-blur-sm transition-opacity"></div>        
        <div class="fixed inset-y-0 right-0 max-w-full flex pl-10">
            <div class="w-screen max-w-md bg-brand-card border-l border-brand-border text-white p-6 flex flex-col justify-between shadow-2xl">
                <div>
                    <div class="flex items-center justify-between pb-4 border-b border-brand-border">
                        <div class="flex items-center gap-3">
                            <i class="fa-solid fa-shopping-bag text-brand-pink text-xl"></i>
                            <h3 class="font-orbitron font-bold text-lg">Keranjang Belanja</h3>
                        </div>
                        <button onclick="toggleCart()" class="text-gray-400 hover:text-white p-2">
                            <i class="fa-solid fa-xmark text-xl"></i>
                        </button>
                    </div>
                    <!-- CART ITEMS LIST -->
                    <div id="cart-items" class="py-4 space-y-4 max-h-[50vh] overflow-y-auto pr-1">
                        <!-- Dynamic items -->
                    </div>
                </div>
                <div class="border-t border-brand-border pt-4 space-y-4">
                    <!-- STUDIO & SEAT SELECTION -->
                    <div class="grid grid-cols-2 gap-3 bg-brand-dark p-3 rounded-xl border border-brand-border">
                        <div>
                            <label class="block text-[10px] font-orbitron text-gray-400 mb-1">STUDIO</label>
                            <select id="studio-select" class="w-full bg-brand-card border border-brand-border rounded-lg text-xs p-2 focus:outline-none focus:border-brand-cyan">
                                <option>Studio 1</option>
                                <option>Studio 2</option>
                                <option>Studio 3 (IMAX)</option>
                                <option>Studio Premiere</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-[10px] font-orbitron text-gray-400 mb-1">NOMOR KURSI</label>
                            <input type="text" id="seat-input" placeholder="Contoh: F12" class="w-full bg-brand-card border border-brand-border rounded-lg text-xs p-2 focus:outline-none focus:border-brand-pink uppercase">
                        </div>
                    </div>
                    <!-- TOTALS -->
                    <div class="space-y-2 text-sm">
                        <div class="flex justify-between text-gray-400">
                            <span>Subtotal</span>
                            <span id="cart-subtotal">Rp 0</span>
                        </div>
                        <div class="flex justify-between text-gray-400">
                            <span>Pajak (10%)</span>
                            <span id="cart-tax">Rp 0</span>
                        </div>
                        <div class="flex justify-between font-orbitron font-bold text-lg text-brand-cyan pt-2 border-t border-brand-border/40">
                            <span>Total</span>
                            <span id="cart-total">Rp 0</span>
                        </div>
                    </div>
                    <button onclick="checkout()" class="w-full bg-gradient-neon text-white font-orbitron font-bold py-3.5 rounded-xl hover:opacity-95 transition-opacity shadow-[0_0_20px_rgba(255,0,127,0.3)]">
                        BAYAR SEKARANG
                    </button>
                </div>
            </div>
        </div>
    </div>
    <!-- RECEIPT MODAL -->
    <div id="receipt-modal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md hidden">
        <div class="bg-brand-card border border-brand-cyan/50 w-full max-w-sm rounded-2xl p-6 text-center shadow-[0_0_30px_rgba(0,242,254,0.2)]">
            <div class="w-12 h-12 bg-green-500/20 text-green-400 rounded-full flex items-center justify-center mx-auto mb-3 border border-green-500/40">
                <i class="fa-solid fa-check text-2xl"></i>
            </div>
            <h3 class="font-orbitron font-bold text-xl text-white">PESANAN BERHASIL!</h3>
            <p class="text-xs text-gray-400 mt-1">Pesanan Anda sedang disiapkan oleh staf bioskop.</p>
            <div class="bg-brand-dark border border-brand-border rounded-xl p-4 my-4 text-left font-mono text-xs space-y-2">
                <div class="flex justify-between text-gray-400 border-b border-brand-border/40 pb-2">
                    <span>ID Order:</span>
                    <span id="receipt-id" class="text-brand-cyan">#RLX-9821</span>
                </div>
                <div class="flex justify-between text-gray-400">
                    <span>Lokasi Delivery:</span>
                    <span id="receipt-seat" class="text-white">Studio 1 (F12)</span>
                </div>
                <div class="flex justify-between text-gray-400 border-b border-brand-border/40 pb-2">
                    <span>Waktu:</span>
                    <span id="receipt-time" class="text-gray-300">21:45 WIB</span>
                </div>
                <div id="receipt-items-list" class="space-y-1 py-1 text-gray-300">
                    <!-- Items -->
                </div>
                <div class="flex justify-between font-bold text-brand-pink pt-2 border-t border-brand-border/40">
                    <span>TOTAL:</span>
                    <span id="receipt-total">Rp 0</span>
                </div>
            </div>
            <button onclick="closeReceipt()" class="w-full bg-brand-border hover:bg-brand-cyan hover:text-black text-white font-orbitron font-bold py-2.5 rounded-xl transition-all text-xs">
                TUTUP & KEMBALI
            </button>
        </div>
    </div>
    <!-- JAVASCRIPT LOGIC -->
    <script>
        const menuItems = [
            { id: 1, name: "Popcorn Original", category: "popcorn", price: 25000, icon: "🍿" },
            { id: 2, name: "Popcorn Caramel", category: "popcorn", price: 30000, icon: "🍿" },
            { id: 3, name: "Popcorn Keju", category: "popcorn", price: 30000, icon: "🧀" },
            { id: 4, name: "Minuman Soda", category: "minuman", price: 15000, icon: "🥤" },
            { id: 5, name: "Es Teh / Lemon Tea", category: "minuman", price: 12000, icon: "🍹" },
            { id: 6, name: "Jus Buah", category: "minuman", price: 15000, icon: "🧃" },
            { id: 7, name: "Hot Dog", category: "snack", price: 20000, icon: "🌭" },
            { id: 8, name: "Pizza Slice", category: "snack", price: 25000, icon: "🍕" },
            { id: 9, name: "Chicken Popcorn", category: "snack", price: 20000, icon: "🍗" },
            { id: 10, name: "French Fries", category: "snack", price: 18000, icon: "🍟" },
            { id: 11, name: "Cokelat Snack", category: "snack", price: 10000, icon: "🍫" },
            { id: 12, name: "Permen Gummy", category: "snack", price: 10000, icon: "🍬" },
            { id: 13, name: "Cookies", category: "snack", price: 12000, icon: "🍪" },
            { id: 14, name: "Pretzel", category: "snack", price: 15000, icon: "🥨" },
            { id: 15, name: "Es Krim", category: "snack", price: 15000, icon: "🍦" },
            { id: 16, name: "Sandwich", category: "snack", price: 22000, icon: "🥪" },
            { id: 17, name: "Mi Instan Cup", category: "snack", price: 15000, icon: "🍜" },
            { id: 18, name: "Topi RELEX", category: "merch", price: 75000, icon: "🧢" },
            { id: 19, name: "T-shirt RELEX", category: "merch", price: 120000, icon: "👕" },
            { id: 20, name: "Tumbler RELEX", category: "merch", price: 85000, icon: "🥤" }
        ];
        const comboItems = [
            { id: 101, name: "RELEX MOVIE COMBO", desc: "1 Popcorn Regular + 2 Minuman", price: 50000, badge: "HEMAT!", badgeColor: "from-green-500 to-emerald-600", icon: "🍿🥤" },
            { id: 102, name: "RELEX COUPLE COMBO", desc: "1 Popcorn Large + 2 Minuman + 1 Snack", price: 85000, badge: "LEBIH HEMAT!", badgeColor: "from-brand-cyan to-blue-600", icon: "🍿🥤🍕" },
            { id: 103, name: "RELEX FAMILY COMBO", desc: "1 Popcorn Large + 4 Minuman + 2 Snack", price: 150000, badge: "COCOK UNTUK KELUARGA!", badgeColor: "from-brand-pink to-purple-600", icon: "🍿🥤🍕🍟" },
            { id: 104, name: "RELEX MERCHANDISE PACK", desc: "1 T-Shirt + 1 Tumbler + 1 Topi", price: 200000, badge: "KOLEKSI SEKARANG!", badgeColor: "from-yellow-400 to-orange-500", icon: "👕🧢🥤" }
        ];
        let cart = [];
        function init() {
            renderMenu('all');
            renderCombos();
        }
        function renderMenu(category) {
            const grid = document.getElementById('menu-grid');
            grid.innerHTML = '';
            const filtered = category === 'all' ? menuItems : menuItems.filter(item => item.category === category);
            filtered.forEach(item => {
                const card = document.createElement('div');
                card.className = "bg-brand-card border border-brand-border/80 hover:border-brand-cyan/60 rounded-2xl p-4 transition-all duration-300 hover:-translate-y-1 hover:shadow-[0_0_15px_rgba(0,242,254,0.15)] flex flex-col justify-between group";
                card.innerHTML = `
                    <div>
                        <div class="relative bg-brand-dark rounded-xl h-28 flex items-center justify-center text-4xl mb-3 border border-brand-border group-hover:border-brand-cyan/30">
                            <span class="absolute top-2 left-2 text-[10px] font-orbitron text-gray-500 font-bold">#${item.id}</span>
                            ${item.icon}
                        </div>
                        <h4 class="font-semibold text-sm text-gray-100 group-hover:text-brand-cyan transition-colors">${item.name}</h4>
                        <p class="font-orbitron font-bold text-brand-cyan text-sm mt-1">Rp ${item.price.toLocaleString('id-ID')}</p>
                    </div>
                    <button onclick="addToCart(${item.id}, 'menu')" class="mt-3 w-full bg-brand-dark hover:bg-brand-cyan hover:text-black border border-brand-cyan/30 text-brand-cyan font-orbitron font-bold text-xs py-2 rounded-lg transition-all flex items-center justify-center gap-2">
                        <i class="fa-solid fa-plus"></i> Tambah
                    </button>
                `;
                grid.appendChild(card);
            });
        }
        function renderCombos() {
            const grid = document.getElementById('combo-grid');
            grid.innerHTML = '';
            comboItems.forEach(item => {
                const card = document.createElement('div');
                card.className = "bg-brand-card border border-brand-pink/40 rounded-2xl p-5 flex flex-col justify-between relative overflow-hidden shadow-[0_0_15px_rgba(255,0,127,0.1)] hover:border-brand-pink transition-all";
                card.innerHTML = `
                    <div>
                        <div class="inline-block bg-gradient-to-r ${item.badgeColor} text-white font-orbitron text-[10px] font-extrabold px-2.5 py-1 rounded-md mb-3 shadow-md">
                            ${item.badge}
                        </div>
                        <div class="text-3xl mb-2">${item.icon}</div>
                        <h4 class="font-orbitron font-bold text-base text-white">${item.name}</h4>
                        <p class="text-xs text-gray-400 mt-1 leading-relaxed">${item.desc}</p>
                    </div>
                    <div class="mt-4 pt-3 border-t border-brand-border/60 flex items-center justify-between">
                        <div>
                            <span class="text-[10px] text-gray-500 block font-orbitron">HARGA PAKET</span>
                            <span class="font-orbitron font-bold text-lg text-brand-pink">Rp ${item.price.toLocaleString('id-ID')}</span>
                        </div>
                        <button onclick="addToCart(${item.id}, 'combo')" class="bg-gradient-to-r from-brand-pink to-brand-purple hover:opacity-90 text-white font-orbitron font-bold text-xs px-4 py-2.5 rounded-xl transition-all shadow-md">
                            + Pesan
                        </button>
                    </div>
                `;
                grid.appendChild(card);
            });
        }
        function filterCategory(evt, cat) {
            document.querySelectorAll('.cat-btn').forEach(btn => {
                btn.classList.remove('bg-brand-cyan', 'text-black', 'font-bold');
                btn.classList.add('bg-brand-card', 'text-gray-300');
            });
            evt.currentTarget.classList.add('bg-brand-cyan', 'text-black', 'font-bold');
            evt.currentTarget.classList.remove('bg-brand-card', 'text-gray-300');
            renderMenu(cat);
        }
        function addToCart(id, type) {
            const item = type === 'menu' ? menuItems.find(i => i.id === id) : comboItems.find(i => i.id === id);
            const existing = cart.find(i => i.id === id && i.type === type);
            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...item, type, qty: 1 });
            }
            updateCartUI();
        }
        function updateCartQty(id, type, delta) {
            const item = cart.find(i => i.id === id && i.type === type);
            if (item) {
                item.qty += delta;
                if (item.qty <= 0) {
                    cart = cart.filter(i => !(i.id === id && i.type === type));
                }
            }
            updateCartUI();
        }
        function updateCartUI() {
            const container = document.getElementById('cart-items');
            const countBadge = document.getElementById('cart-count');
            container.innerHTML = '';
            let totalQty = 0;
            let subtotal = 0;
            cart.forEach(item => {
                totalQty += item.qty;
                subtotal += item.price * item.qty;
                const div = document.createElement('div');
                div.className = "flex items-center justify-between bg-brand-dark p-3 rounded-xl border border-brand-border";
                div.innerHTML = `
                    <div class="flex-1">
                        <h5 class="text-xs font-semibold text-white">${item.name}</h5>
                        <p class="text-[11px] text-brand-cyan font-orbitron">Rp ${item.price.toLocaleString('id-ID')}</p>
                    </div>
                    <div class="flex items-center gap-2 bg-brand-card px-2 py-1 rounded-lg border border-brand-border">
                        <button onclick="updateCartQty(${item.id}, '${item.type}', -1)" class="text-gray-400 hover:text-brand-pink text-xs px-1">-</button>
                        <span class="text-xs font-bold w-4 text-center">${item.qty}</span>
                        <button onclick="updateCartQty(${item.id}, '${item.type}', 1)" class="text-gray-400 hover:text-brand-cyan text-xs px-1">+</button>
                    </div>
                `;
                container.appendChild(div);
            });
            const tax = subtotal * 0.1;
            const total = subtotal + tax;
            countBadge.innerText = totalQty;
            document.getElementById('cart-subtotal').innerText = `Rp ${subtotal.toLocaleString('id-ID')}`;
            document.getElementById('cart-tax').innerText = `Rp ${tax.toLocaleString('id-ID')}`;
            document.getElementById('cart-total').innerText = `Rp ${total.toLocaleString('id-ID')}`;
        }
        function toggleCart() {
            document.getElementById('cart-drawer').classList.toggle('hidden');
        }
        function checkout() {
            if (cart.length === 0) {
                alert('Keranjang belanja Anda masih kosong!');
                return;
            }
            const seat = document.getElementById('seat-input').value.trim();
            if (!seat) {
                alert('Silakan masukkan nomor kursi Anda!');
                return;
            }
            const studio = document.getElementById('studio-select').value;
            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
            const total = subtotal * 1.1; 
          document.getElementById('receipt-id').innerText = `#RLX-${Math.floor(1000 + Math.random() * 9000)}`;
            document.getElementById('receipt-seat').innerText = `${studio} (${seat.toUpperCase()})`;
            document.getElementById('receipt-time').innerText = new Date().toLocaleTimeString('id-ID', { hour: '2-digit', minute: '2-digit' }) + " WIB";
            document.getElementById('receipt-total').innerText = `Rp ${total.toLocaleString('id-ID')}`;
            const receiptList = document.getElementById('receipt-items-list');
            receiptList.innerHTML = '';
            cart.forEach(item => {
                const row = document.createElement('div');
                row.className = "flex justify-between";
                row.innerHTML = `<span>${item.qty}x ${item.name}</span><span>Rp ${(item.price * item.qty).toLocaleString('id-ID')}</span>`;
                receiptList.appendChild(row);
            });
            toggleCart();
            document.getElementById('receipt-modal').classList.remove('hidden');
            cart = [];
            updateCartUI();
        }

        function closeReceipt() {
            document.getElementById('receipt-modal').classList.add('hidden');
        }

        window.onload = init;
    </script>
</body>
</html>
