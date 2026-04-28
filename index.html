<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FoodVerse — 3D Food Ordering</title>
<script src="https://cdn.tailwindcss.com"></script>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800;900&family=DM+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
<style>
:root{--bg:#0a0a0a;--surface:#141414;--surface2:#1e1e1e;--border:#2a2a2a;--text:#f0ece4;--text-muted:#8a8478;--accent:#ff6b35;--accent-glow:rgba(255,107,53,0.3);--gold:#ffc857;--success:#2ecc71;--danger:#e74c3c;--card-bg:#181818}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden}
h1,h2,h3,h4,h5,h6{font-family:'Outfit',sans-serif}
::-webkit-scrollbar{width:6px}::-webkit-scrollbar-track{background:var(--bg)}::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px}::-webkit-scrollbar-thumb:hover{background:var(--accent)}
.scene-wrap{perspective:1200px;perspective-origin:50% 50%}
.scene-inner{transform-style:preserve-3d;transition:transform 0.6s cubic-bezier(0.23,1,0.32,1)}
.card-3d{transform-style:preserve-3d;transition:all 0.5s cubic-bezier(0.23,1,0.32,1);will-change:transform}
.card-3d:hover{transform:translateY(-12px) rotateX(5deg) rotateY(-3deg) scale(1.02);box-shadow:0 25px 60px rgba(255,107,53,0.15),0 0 0 1px rgba(255,107,53,0.1)}
.hero-3d{transform-style:preserve-3d;animation:heroFloat 6s ease-in-out infinite}
@keyframes heroFloat{0%,100%{transform:rotateY(-8deg) rotateX(5deg) translateZ(0)}50%{transform:rotateY(8deg) rotateX(-3deg) translateZ(30px)}}
.particle{position:fixed;border-radius:50%;pointer-events:none;z-index:0;animation:particleFloat linear infinite}
@keyframes particleFloat{0%{transform:translateY(100vh) scale(0);opacity:0}10%{opacity:1}90%{opacity:1}100%{transform:translateY(-10vh) scale(1);opacity:0}}
.glow-accent{box-shadow:0 0 30px var(--accent-glow),0 0 60px rgba(255,107,53,0.1)}
.toast-container{position:fixed;top:20px;right:20px;z-index:9999;display:flex;flex-direction:column;gap:10px;max-width:400px;width:calc(100% - 40px)}
.toast{background:var(--surface2);border:1px solid var(--border);border-radius:16px;padding:16px 20px;transform:translateX(120%);transition:all 0.4s cubic-bezier(0.23,1,0.32,1);backdrop-filter:blur(20px)}
.toast.show{transform:translateX(0)}
.toast.new-order{border-left:4px solid var(--accent)}.toast.success{border-left:4px solid var(--success)}.toast.error{border-left:4px solid var(--danger)}.toast.info{border-left:4px solid var(--gold)}.toast.otp{border-left:4px solid #9b59b6}
.modal-overlay{position:fixed;inset:0;background:rgba(0,0,0,0.7);backdrop-filter:blur(8px);z-index:8000;display:flex;align-items:center;justify-content:center;opacity:0;pointer-events:none;transition:opacity 0.3s}
.modal-overlay.active{opacity:1;pointer-events:all}
.modal-box{background:var(--surface);border:1px solid var(--border);border-radius:20px;padding:32px;max-width:500px;width:90%;transform:scale(0.9) translateY(20px);transition:transform 0.4s cubic-bezier(0.23,1,0.32,1);max-height:90vh;overflow-y:auto}
.modal-overlay.active .modal-box{transform:scale(1) translateY(0)}
.input-field{width:100%;padding:12px 16px;background:var(--bg);border:1px solid var(--border);border-radius:12px;color:var(--text);font-family:'DM Sans',sans-serif;font-size:14px;transition:all 0.3s;outline:none}
.input-field:focus{border-color:var(--accent);box-shadow:0 0 0 3px var(--accent-glow)}
.input-field.error{border-color:var(--danger);box-shadow:0 0 0 3px rgba(231,76,60,0.2)}
.error-msg{color:var(--danger);font-size:12px;margin-top:4px;display:none}
.error-msg.show{display:block}
.btn-primary{background:linear-gradient(135deg,var(--accent),#e85d2a);color:white;padding:12px 28px;border:none;border-radius:12px;font-family:'Outfit',sans-serif;font-weight:600;font-size:15px;cursor:pointer;transition:all 0.3s;position:relative;overflow:hidden}
.btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 25px var(--accent-glow)}
.btn-primary:active{transform:translateY(0)}
.btn-secondary{background:var(--surface2);color:var(--text);padding:12px 28px;border:1px solid var(--border);border-radius:12px;font-family:'Outfit',sans-serif;font-weight:600;font-size:15px;cursor:pointer;transition:all 0.3s}
.btn-secondary:hover{border-color:var(--accent);color:var(--accent)}
.btn-danger{background:linear-gradient(135deg,var(--danger),#c0392b);color:white;padding:10px 24px;border:none;border-radius:12px;font-family:'Outfit',sans-serif;font-weight:600;font-size:14px;cursor:pointer;transition:all 0.3s}
.btn-danger:hover{transform:translateY(-2px);box-shadow:0 8px 25px rgba(231,76,60,0.3)}
.btn-success{background:linear-gradient(135deg,var(--success),#27ae60);color:white;padding:10px 24px;border:none;border-radius:12px;font-family:'Outfit',sans-serif;font-weight:600;font-size:14px;cursor:pointer;transition:all 0.3s}
.btn-success:hover{transform:translateY(-2px);box-shadow:0 8px 25px rgba(46,204,113,0.3)}
.tab-btn{padding:10px 20px;border:1px solid var(--border);background:transparent;color:var(--text-muted);border-radius:10px;cursor:pointer;font-family:'DM Sans',sans-serif;font-size:14px;transition:all 0.3s}
.tab-btn.active{background:var(--accent);color:white;border-color:var(--accent)}
.tab-btn:hover:not(.active){border-color:var(--accent);color:var(--accent)}
.badge{position:absolute;top:-6px;right:-6px;background:var(--accent);color:white;font-size:11px;font-weight:700;width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center;animation:badgePop 0.3s cubic-bezier(0.68,-0.55,0.27,1.55)}
@keyframes badgePop{0%{transform:scale(0)}100%{transform:scale(1)}}
.stat-card{background:var(--card-bg);border:1px solid var(--border);border-radius:20px;padding:24px;transform-style:preserve-3d;transition:all 0.4s cubic-bezier(0.23,1,0.32,1)}
.stat-card:hover{transform:translateY(-8px) rotateX(3deg);box-shadow:0 20px 50px rgba(0,0,0,0.3)}
.cat-pill{padding:10px 24px;border-radius:50px;border:1px solid var(--border);background:transparent;color:var(--text-muted);cursor:pointer;font-family:'DM Sans',sans-serif;font-size:14px;transition:all 0.3s;white-space:nowrap}
.cat-pill.active{background:var(--accent);color:white;border-color:var(--accent)}
.cat-pill:hover:not(.active){border-color:var(--accent);color:var(--accent)}
.cart-sidebar{position:fixed;top:0;right:0;bottom:0;width:400px;max-width:90vw;background:var(--surface);border-left:1px solid var(--border);z-index:7000;transform:translateX(100%);transition:transform 0.4s cubic-bezier(0.23,1,0.32,1);display:flex;flex-direction:column}
.cart-sidebar.open{transform:translateX(0)}
.cart-overlay{position:fixed;inset:0;background:rgba(0,0,0,0.5);z-index:6999;opacity:0;pointer-events:none;transition:opacity 0.3s}
.cart-overlay.open{opacity:1;pointer-events:all}
.noise-overlay{position:fixed;inset:0;z-index:1;pointer-events:none;opacity:0.03;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E")}
.radio-card{border:2px solid var(--border);border-radius:14px;padding:16px;cursor:pointer;transition:all 0.3s;display:flex;align-items:center;gap:12px}
.radio-card.selected{border-color:var(--accent);background:rgba(255,107,53,0.05)}
.radio-dot{width:20px;height:20px;border-radius:50%;border:2px solid var(--border);transition:all 0.3s;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.radio-card.selected .radio-dot{border-color:var(--accent)}
.radio-card.selected .radio-dot::after{content:'';width:10px;height:10px;border-radius:50%;background:var(--accent)}
.admin-table{width:100%;border-collapse:separate;border-spacing:0}
.admin-table th{background:var(--surface2);padding:12px 16px;text-align:left;font-family:'Outfit',sans-serif;font-weight:600;font-size:13px;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.05em}
.admin-table td{padding:14px 16px;border-bottom:1px solid var(--border);font-size:14px;vertical-align:middle}
.admin-table tr:hover td{background:rgba(255,107,53,0.03)}
.pulse-ring{animation:pulseRing 2s ease-out infinite}
@keyframes pulseRing{0%{box-shadow:0 0 0 0 var(--accent-glow)}100%{box-shadow:0 0 0 20px rgba(255,107,53,0)}}
.page{display:none;animation:pageIn 0.4s ease}
.page.active{display:block}
@keyframes pageIn{0%{opacity:0;transform:translateY(20px)}100%{opacity:1;transform:translateY(0)}}
.otp-input{width:48px;height:56px;text-align:center;font-size:24px;font-weight:700;font-family:'Outfit',sans-serif;background:var(--bg);border:2px solid var(--border);border-radius:12px;color:var(--text);outline:none;transition:all 0.3s}
.otp-input:focus{border-color:var(--accent);box-shadow:0 0 0 3px var(--accent-glow)}
.otp-input.error{border-color:var(--danger);box-shadow:0 0 0 3px rgba(231,76,60,0.2)}
@media(max-width:768px){.hero-3d{animation:none;transform:none}.card-3d:hover{transform:translateY(-6px)}.stat-card:hover{transform:translateY(-4px)}.otp-input{width:40px;height:48px;font-size:20px}}
</style>
</head>
<body>
<div class="noise-overlay"></div>
<div id="particles"></div>
<div class="toast-container" id="toastContainer"></div>

<!-- Cart Sidebar -->
<div class="cart-overlay" id="cartOverlay"></div>
<div class="cart-sidebar" id="cartSidebar">
  <div class="p-6 border-b border-[var(--border)] flex items-center justify-between">
    <h3 class="text-xl font-bold" style="font-family:'Outfit'">Your Cart</h3>
    <button id="closeCartBtn" class="w-10 h-10 rounded-full flex items-center justify-center hover:bg-[var(--surface2)] transition-colors"><i class="fas fa-times text-[var(--text-muted)]"></i></button>
  </div>
  <div class="flex-1 overflow-y-auto p-6" id="cartItems"></div>
  <div class="p-6 border-t border-[var(--border)]" id="cartFooter" style="display:none">
    <div class="flex justify-between mb-2 text-sm text-[var(--text-muted)]"><span>Subtotal</span><span id="cartSubtotal">$0.00</span></div>
    <div class="flex justify-between mb-4 text-lg font-bold" style="font-family:'Outfit'"><span>Total</span><span id="cartTotal" class="text-[var(--accent)]">$0.00</span></div>
    <button id="checkoutBtn" class="btn-primary w-full text-center">Proceed to Checkout <i class="fas fa-arrow-right ml-2"></i></button>
  </div>
</div>

<!-- Navbar -->
<nav class="fixed top-0 left-0 right-0 z-[6000] transition-all duration-300" id="navbar">
  <div class="max-w-7xl mx-auto px-4 sm:px-6">
    <div class="flex items-center justify-between h-16 sm:h-20">
      <div id="logoBtn" class="flex items-center gap-2 cursor-pointer group">
        <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-[var(--accent)] to-[#e85d2a] flex items-center justify-center transform group-hover:rotate-12 transition-transform"><i class="fas fa-fire text-white text-lg"></i></div>
        <span class="text-xl font-bold" style="font-family:'Outfit'">FoodVerse</span>
      </div>
      <div class="hidden md:flex items-center gap-1" id="navLinks">
        <a href="javascript:void(0)" class="nav-link px-4 py-2 rounded-xl text-sm font-medium transition-all hover:bg-[var(--surface2)] hover:text-[var(--accent)]" data-page="home">Home</a>
        <a href="javascript:void(0)" class="nav-link px-4 py-2 rounded-xl text-sm font-medium transition-all hover:bg-[var(--surface2)] hover:text-[var(--accent)]" data-page="menu">Menu</a>
      </div>
      <div class="flex items-center gap-3">
        <button id="cartBtn" class="relative w-10 h-10 rounded-xl bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] transition-all"><i class="fas fa-shopping-bag text-sm"></i><span class="badge" id="cartBadge" style="display:none">0</span></button>
        <div id="authButtons"></div>
      </div>
    </div>
  </div>
</nav>

<!-- HOME PAGE -->
<div class="page active" id="page-home">
  <section class="min-h-screen flex items-center relative overflow-hidden pt-20">
    <div class="absolute inset-0 z-0">
      <div class="absolute top-20 left-10 w-72 h-72 rounded-full bg-[var(--accent)] opacity-[0.07] blur-[100px]"></div>
      <div class="absolute bottom-20 right-10 w-96 h-96 rounded-full bg-[var(--gold)] opacity-[0.05] blur-[120px]"></div>
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] rounded-full border border-[var(--border)] opacity-20"></div>
    </div>
    <div class="max-w-7xl mx-auto px-4 sm:px-6 w-full relative z-10">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <div>
          <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-[var(--surface2)] border border-[var(--border)] mb-6 text-sm"><span class="w-2 h-2 rounded-full bg-[var(--success)] animate-pulse"></span><span class="text-[var(--text-muted)]">Free delivery on orders above $30</span></div>
          <h1 class="text-5xl sm:text-6xl lg:text-7xl font-black leading-[0.95] mb-6" style="font-family:'Outfit'">Taste The<br><span class="bg-gradient-to-r from-[var(--accent)] to-[var(--gold)] bg-clip-text text-transparent">Future</span> Of<br>Food</h1>
          <p class="text-[var(--text-muted)] text-lg mb-8 max-w-md leading-relaxed">Experience culinary excellence delivered to your doorstep. Handcrafted dishes from the finest kitchens in the city.</p>
          <div class="flex flex-wrap gap-4">
            <button id="heroMenuBtn" class="btn-primary text-base px-8 py-4">Explore Menu <i class="fas fa-arrow-right ml-2"></i></button>
            <button id="heroStoryBtn" class="btn-secondary text-base px-8 py-4">Our Story</button>
          </div>
          <div class="flex gap-8 mt-10">
            <div><span class="text-2xl font-black text-[var(--accent)]" style="font-family:'Outfit'">500+</span><p class="text-xs text-[var(--text-muted)] mt-1">Dishes</p></div>
            <div><span class="text-2xl font-black text-[var(--gold)]" style="font-family:'Outfit'">50k+</span><p class="text-xs text-[var(--text-muted)] mt-1">Happy Customers</p></div>
            <div><span class="text-2xl font-black text-[var(--success)]" style="font-family:'Outfit'">4.9</span><p class="text-xs text-[var(--text-muted)] mt-1">Rating</p></div>
          </div>
        </div>
        <div class="scene-wrap hidden lg:block">
          <div class="hero-3d relative">
            <div class="relative rounded-3xl overflow-hidden shadow-2xl glow-accent">
              <img src="https://picsum.photos/seed/heroburger/600/500.jpg" alt="Hero Food" class="w-full h-[500px] object-cover">
              <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"></div>
              <div class="absolute bottom-6 left-6 right-6"><div class="bg-black/50 backdrop-blur-xl rounded-2xl p-4 border border-white/10"><div class="flex items-center justify-between"><div><p class="font-bold text-lg" style="font-family:'Outfit'">Signature Wagyu Burger</p><p class="text-sm text-white/60">Premium angus beef, truffle aioli</p></div><span class="text-2xl font-black text-[var(--accent)]" style="font-family:'Outfit'">$24.99</span></div></div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="py-20 relative z-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="text-center mb-12"><h2 class="text-3xl sm:text-4xl font-black mb-3" style="font-family:'Outfit'">Browse Categories</h2><p class="text-[var(--text-muted)]">From sizzling appetizers to divine desserts</p></div>
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 scene-wrap" id="homeCatGrid"></div>
    </div>
  </section>
  <section class="py-20 relative z-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="flex items-end justify-between mb-12">
        <div><h2 class="text-3xl sm:text-4xl font-black mb-3" style="font-family:'Outfit'">Popular Right Now</h2><p class="text-[var(--text-muted)]">Most ordered dishes this week</p></div>
        <button id="viewAllMenuBtn" class="hidden sm:flex btn-secondary text-sm">View All <i class="fas fa-arrow-right ml-2"></i></button>
      </div>
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6 scene-wrap" id="popularGrid"></div>
    </div>
  </section>
  <section class="py-20 relative z-10" id="about-section">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="grid lg:grid-cols-2 gap-16 items-center">
        <div class="scene-wrap"><div class="scene-inner"><div class="card-3d rounded-3xl overflow-hidden glow-accent"><img src="https://picsum.photos/seed/chefcook/600/450.jpg" alt="Our Kitchen" class="w-full h-[400px] object-cover"></div></div></div>
        <div>
          <span class="text-[var(--accent)] font-semibold text-sm uppercase tracking-wider">Our Story</span>
          <h2 class="text-4xl font-black mt-3 mb-6" style="font-family:'Outfit'">Crafted With Passion Since 2020</h2>
          <p class="text-[var(--text-muted)] leading-relaxed mb-6">FoodVerse was born from a simple idea: everyone deserves restaurant-quality food without the restaurant wait. Our team of world-class chefs prepares each dish with premium ingredients, traditional techniques, and a modern twist.</p>
          <p class="text-[var(--text-muted)] leading-relaxed mb-8">From sourcing the freshest produce to perfecting every sauce, we obsess over details so you don't have to.</p>
          <div class="grid grid-cols-3 gap-6">
            <div class="text-center p-4 bg-[var(--surface2)] rounded-2xl border border-[var(--border)]"><i class="fas fa-leaf text-[var(--success)] text-xl mb-2"></i><p class="text-xs font-semibold">Fresh Ingredients</p></div>
            <div class="text-center p-4 bg-[var(--surface2)] rounded-2xl border border-[var(--border)]"><i class="fas fa-award text-[var(--gold)] text-xl mb-2"></i><p class="text-xs font-semibold">Top Chefs</p></div>
            <div class="text-center p-4 bg-[var(--surface2)] rounded-2xl border border-[var(--border)]"><i class="fas fa-bolt text-[var(--accent)] text-xl mb-2"></i><p class="text-xs font-semibold">Fast Delivery</p></div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <footer class="py-12 border-t border-[var(--border)] relative z-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-8 mb-8">
        <div><div class="flex items-center gap-2 mb-4"><div class="w-8 h-8 rounded-lg bg-gradient-to-br from-[var(--accent)] to-[#e85d2a] flex items-center justify-center"><i class="fas fa-fire text-white text-sm"></i></div><span class="text-lg font-bold" style="font-family:'Outfit'">FoodVerse</span></div><p class="text-sm text-[var(--text-muted)] leading-relaxed">Premium food delivery experience.</p></div>
        <div><h4 class="font-bold mb-4 text-sm" style="font-family:'Outfit'">Quick Links</h4><div class="flex flex-col gap-2"><a href="javascript:void(0)" class="nav-link text-sm text-[var(--text-muted)] hover:text-[var(--accent)] transition-colors" data-page="home">Home</a><a href="javascript:void(0)" class="nav-link text-sm text-[var(--text-muted)] hover:text-[var(--accent)] transition-colors" data-page="menu">Menu</a></div></div>
        <div><h4 class="font-bold mb-4 text-sm" style="font-family:'Outfit'">Support</h4><div class="flex flex-col gap-2"><a href="javascript:void(0)" class="text-sm text-[var(--text-muted)]">Help Center</a><a href="javascript:void(0)" class="text-sm text-[var(--text-muted)]">Contact Us</a></div></div>
        <div><h4 class="font-bold mb-4 text-sm" style="font-family:'Outfit'">Follow Us</h4><div class="flex gap-3"><a href="javascript:void(0)" class="w-10 h-10 rounded-xl bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] hover:text-[var(--accent)] transition-all"><i class="fab fa-instagram"></i></a><a href="javascript:void(0)" class="w-10 h-10 rounded-xl bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] hover:text-[var(--accent)] transition-all"><i class="fab fa-twitter"></i></a></div></div>
      </div>
      <div class="pt-8 border-t border-[var(--border)] text-center text-sm text-[var(--text-muted)]">2025 FoodVerse. All rights reserved.</div>
    </div>
  </footer>
</div>

<!-- MENU PAGE -->
<div class="page" id="page-menu">
  <section class="pt-28 pb-20 min-h-screen">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="text-center mb-10"><h2 class="text-4xl font-black mb-3" style="font-family:'Outfit'">Our Menu</h2><p class="text-[var(--text-muted)]">Discover dishes crafted to perfection</p></div>
      <div class="flex gap-3 overflow-x-auto pb-4 mb-8 justify-center flex-wrap" id="categoryPills"></div>
      <div class="grid sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 scene-wrap" id="menuGrid"></div>
    </div>
  </section>
</div>

<!-- CHECKOUT PAGE -->
<div class="page" id="page-checkout">
  <section class="pt-28 pb-20 min-h-screen">
    <div class="max-w-4xl mx-auto px-4 sm:px-6">
      <div class="flex items-center gap-4 mb-8"><button id="backToMenuBtn" class="w-10 h-10 rounded-xl bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] transition-all"><i class="fas fa-arrow-left"></i></button><h2 class="text-3xl font-black" style="font-family:'Outfit'">Checkout</h2></div>
      <div class="grid lg:grid-cols-5 gap-8">
        <div class="lg:col-span-3 space-y-6">
          <div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl p-6">
            <h3 class="font-bold text-lg mb-4" style="font-family:'Outfit'"><i class="fas fa-map-marker-alt text-[var(--accent)] mr-2"></i>Delivery Address</h3>
            <div class="space-y-4">
              <div><label class="text-sm text-[var(--text-muted)] mb-1 block">Full Name</label><input type="text" class="input-field" id="checkName" placeholder="John Doe"><p class="error-msg" id="checkNameErr">Please enter your full name</p></div>
              <div><label class="text-sm text-[var(--text-muted)] mb-1 block">Phone Number</label><input type="tel" class="input-field" id="checkPhone" placeholder="+1 234 567 8900"><p class="error-msg" id="checkPhoneErr">Please enter a valid phone number</p></div>
              <div><label class="text-sm text-[var(--text-muted)] mb-1 block">Address</label><textarea class="input-field" id="checkAddress" rows="2" placeholder="123 Main St, Apt 4B"></textarea><p class="error-msg" id="checkAddressErr">Please enter your delivery address</p></div>
            </div>
          </div>
          <div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl p-6">
            <h3 class="font-bold text-lg mb-4" style="font-family:'Outfit'"><i class="fas fa-credit-card text-[var(--accent)] mr-2"></i>Payment Method</h3>
            <div class="space-y-3" id="paymentMethods">
              <div class="radio-card selected" data-method="upi"><div class="radio-dot"></div><i class="fas fa-mobile-alt text-[var(--accent)]"></i><div><p class="font-semibold text-sm">UPI</p><p class="text-xs text-[var(--text-muted)]">Pay using any UPI app</p></div></div>
              <div class="radio-card" data-method="credit"><div class="radio-dot"></div><i class="fas fa-credit-card text-[var(--gold)]"></i><div><p class="font-semibold text-sm">Credit Card</p><p class="text-xs text-[var(--text-muted)]">Visa, Mastercard, Amex</p></div></div>
              <div class="radio-card" data-method="debit"><div class="radio-dot"></div><i class="fas fa-credit-card text-[var(--success)]"></i><div><p class="font-semibold text-sm">Debit Card</p><p class="text-xs text-[var(--text-muted)]">All major banks accepted</p></div></div>
            </div>
            <div class="mt-4 space-y-4" id="cardFields" style="display:none">
              <div><label class="text-sm text-[var(--text-muted)] mb-1 block">Card Number</label><input type="text" class="input-field" id="cardNumber" placeholder="1234 5678 9012 3456" maxlength="19"><p class="error-msg" id="cardNumberErr">Please enter a valid card number</p></div>
              <div class="grid grid-cols-2 gap-4"><div><label class="text-sm text-[var(--text-muted)] mb-1 block">Expiry</label><input type="text" class="input-field" id="cardExpiry" placeholder="MM/YY" maxlength="5"><p class="error-msg" id="cardExpiryErr">Invalid expiry date</p></div><div><label class="text-sm text-[var(--text-muted)] mb-1 block">CVV</label><input type="text" class="input-field" id="cardCvv" placeholder="123" maxlength="4"><p class="error-msg" id="cardCvvErr">Invalid CVV</p></div></div>
            </div>
            <div id="upiField" class="mt-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">UPI ID</label><input type="text" class="input-field" id="upiId" placeholder="yourname@upi"><p class="error-msg" id="upiIdErr">Please enter a valid UPI ID (e.g. name@upi)</p></div>
          </div>
        </div>
        <div class="lg:col-span-2">
          <div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl p-6 sticky top-28">
            <h3 class="font-bold text-lg mb-4" style="font-family:'Outfit'">Order Summary</h3>
            <div class="space-y-3 mb-4 max-h-[300px] overflow-y-auto" id="checkoutItems"></div>
            <div class="border-t border-[var(--border)] pt-4 space-y-2">
              <div class="flex justify-between text-sm text-[var(--text-muted)]"><span>Subtotal</span><span id="checkSubtotal">$0.00</span></div>
              <div class="flex justify-between text-sm text-[var(--text-muted)]"><span>Delivery Fee</span><span>$2.99</span></div>
              <div class="flex justify-between text-lg font-bold pt-2 border-t border-[var(--border)]" style="font-family:'Outfit'"><span>Total</span><span class="text-[var(--accent)]" id="checkTotal">$0.00</span></div>
            </div>
            <button id="placeOrderBtn" class="btn-primary w-full mt-6 py-4"><i class="fas fa-paper-plane mr-2"></i>Place Order</button>
            <p class="text-xs text-[var(--text-muted)] text-center mt-3">Order requires admin approval</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- ORDERS PAGE -->
<div class="page" id="page-orders">
  <section class="pt-28 pb-20 min-h-screen">
    <div class="max-w-4xl mx-auto px-4 sm:px-6">
      <div class="flex items-center gap-4 mb-8"><button id="backFromOrdersBtn" class="w-10 h-10 rounded-xl bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] transition-all"><i class="fas fa-arrow-left"></i></button><h2 class="text-3xl font-black" style="font-family:'Outfit'">My Orders</h2></div>
      <div id="userOrdersList"></div>
    </div>
  </section>
</div>

<!-- ADMIN PAGE -->
<div class="page" id="page-admin">
  <section class="pt-28 pb-20 min-h-screen">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="flex items-center justify-between mb-8 flex-wrap gap-4">
        <div class="flex items-center gap-4"><button id="adminBackBtn" class="w-10 h-10 rounded-xl bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] transition-all"><i class="fas fa-arrow-left"></i></button><h2 class="text-3xl font-black" style="font-family:'Outfit'">Admin Dashboard</h2></div>
        <button id="addItemBtn" class="btn-primary"><i class="fas fa-plus mr-2"></i>Add Menu Item</button>
      </div>
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-4 mb-8 scene-wrap">
        <div class="scene-inner"><div class="stat-card"><div class="flex items-center justify-between mb-3"><div class="w-12 h-12 rounded-xl bg-[rgba(255,107,53,0.1)] flex items-center justify-center"><i class="fas fa-shopping-bag text-[var(--accent)] text-xl"></i></div><span class="text-xs text-[var(--success)] font-semibold"><i class="fas fa-arrow-up mr-1"></i>12%</span></div><p class="text-3xl font-black" style="font-family:'Outfit'" id="statOrders">0</p><p class="text-sm text-[var(--text-muted)]">Total Orders</p></div></div>
        <div class="scene-inner"><div class="stat-card"><div class="flex items-center justify-between mb-3"><div class="w-12 h-12 rounded-xl bg-[rgba(255,200,87,0.1)] flex items-center justify-center"><i class="fas fa-dollar-sign text-[var(--gold)] text-xl"></i></div><span class="text-xs text-[var(--success)] font-semibold"><i class="fas fa-arrow-up mr-1"></i>8%</span></div><p class="text-3xl font-black" style="font-family:'Outfit'" id="statRevenue">$0</p><p class="text-sm text-[var(--text-muted)]">Total Revenue</p></div></div>
        <div class="scene-inner"><div class="stat-card"><div class="flex items-center justify-between mb-3"><div class="w-12 h-12 rounded-xl bg-[rgba(46,204,113,0.1)] flex items-center justify-center"><i class="fas fa-check-circle text-[var(--success)] text-xl"></i></div></div><p class="text-3xl font-black" style="font-family:'Outfit'" id="statAccepted">0</p><p class="text-sm text-[var(--text-muted)]">Accepted Orders</p></div></div>
        <div class="scene-inner"><div class="stat-card"><div class="flex items-center justify-between mb-3"><div class="w-12 h-12 rounded-xl bg-[rgba(231,76,60,0.1)] flex items-center justify-center"><i class="fas fa-clock text-[var(--danger)] text-xl"></i></div></div><p class="text-3xl font-black" style="font-family:'Outfit'" id="statPending">0</p><p class="text-sm text-[var(--text-muted)]">Pending Orders</p></div></div>
      </div>
      <div class="flex gap-2 mb-6 overflow-x-auto pb-2" id="adminTabs">
        <button class="tab-btn active" data-tab="orders">Orders</button>
        <button class="tab-btn" data-tab="items">Menu Items</button>
        <button class="tab-btn" data-tab="users">Users</button>
      </div>
      <div class="admin-tab" id="adminTab-orders">
        <div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl overflow-hidden"><div class="overflow-x-auto"><table class="admin-table"><thead><tr><th>Order ID</th><th>Customer</th><th>Items</th><th>Total</th><th>Status</th><th>Actions</th></tr></thead><tbody id="adminOrdersBody"></tbody></table></div></div>
      </div>
      <div class="admin-tab" id="adminTab-items" style="display:none">
        <div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl overflow-hidden"><div class="overflow-x-auto"><table class="admin-table"><thead><tr><th>Item</th><th>Category</th><th>Price</th><th>Status</th><th>Actions</th></tr></thead><tbody id="adminItemsBody"></tbody></table></div></div>
      </div>
      <div class="admin-tab" id="adminTab-users" style="display:none">
        <div class="flex justify-end mb-4"><button id="addUserBtn" class="btn-primary text-sm py-2 px-4"><i class="fas fa-user-plus mr-2"></i>Add User</button></div>
        <div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl overflow-hidden"><div class="overflow-x-auto"><table class="admin-table"><thead><tr><th>Name</th><th>Email</th><th>Phone</th><th>Role</th><th>Orders</th><th>Actions</th></tr></thead><tbody id="adminUsersBody"></tbody></table></div></div>
      </div>
    </div>
  </section>
</div>

<!-- LOGIN MODAL -->
<div class="modal-overlay" id="loginModal">
  <div class="modal-box">
    <div class="flex items-center justify-between mb-6">
      <h2 class="text-2xl font-black" style="font-family:'Outfit'">Welcome Back</h2>
      <button class="close-modal-btn w-10 h-10 rounded-full flex items-center justify-center hover:bg-[var(--surface2)] transition-colors" data-modal="loginModal"><i class="fas fa-times text-[var(--text-muted)]"></i></button>
    </div>
    <form id="loginForm" novalidate>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Email Address</label><input type="email" class="input-field" id="loginEmail" placeholder="you@example.com"><p class="error-msg" id="loginEmailErr">Please enter a valid email address</p></div>
      <div class="mb-6"><label class="text-sm text-[var(--text-muted)] mb-1 block">Password</label><div class="relative"><input type="password" class="input-field pr-12" id="loginPassword" placeholder="Enter your password"><button type="button" class="toggle-pw-btn absolute right-3 top-1/2 -translate-y-1/2 text-[var(--text-muted)] hover:text-[var(--text)] transition-colors" data-target="loginPassword"><i class="fas fa-eye"></i></button></div><p class="error-msg" id="loginPasswordErr">Password must be at least 6 characters</p></div>
      <button type="submit" class="btn-primary w-full py-4">Sign In</button>
    </form>
    <p class="text-center text-sm text-[var(--text-muted)] mt-5">Don't have an account? <a href="javascript:void(0)" id="goToRegister" class="text-[var(--accent)] font-semibold hover:underline">Sign Up</a></p>
  </div>
</div>

<!-- REGISTER MODAL -->
<div class="modal-overlay" id="registerModal">
  <div class="modal-box">
    <div class="flex items-center justify-between mb-6">
      <h2 class="text-2xl font-black" style="font-family:'Outfit'">Create Account</h2>
      <button class="close-modal-btn w-10 h-10 rounded-full flex items-center justify-center hover:bg-[var(--surface2)] transition-colors" data-modal="registerModal"><i class="fas fa-times text-[var(--text-muted)]"></i></button>
    </div>
    <form id="registerForm" novalidate>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Full Name</label><input type="text" class="input-field" id="regName" placeholder="John Doe"><p class="error-msg" id="regNameErr">Name must be at least 2 characters (letters and spaces only)</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Email Address</label><input type="email" class="input-field" id="regEmail" placeholder="you@example.com"><p class="error-msg" id="regEmailErr">Please enter a valid email address</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Phone Number</label><input type="tel" class="input-field" id="regPhone" placeholder="+1 234 567 8900"><p class="error-msg" id="regPhoneErr">Please enter a valid phone number (10+ digits)</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Password</label><div class="relative"><input type="password" class="input-field pr-12" id="regPassword" placeholder="Min 6 characters with a number"><button type="button" class="toggle-pw-btn absolute right-3 top-1/2 -translate-y-1/2 text-[var(--text-muted)] hover:text-[var(--text)] transition-colors" data-target="regPassword"><i class="fas fa-eye"></i></button></div><p class="error-msg" id="regPasswordErr">Password must be at least 6 characters with a number</p></div>
      <div class="mb-6"><label class="text-sm text-[var(--text-muted)] mb-1 block">Confirm Password</label><div class="relative"><input type="password" class="input-field pr-12" id="regConfirm" placeholder="Re-enter password"><button type="button" class="toggle-pw-btn absolute right-3 top-1/2 -translate-y-1/2 text-[var(--text-muted)] hover:text-[var(--text)] transition-colors" data-target="regConfirm"><i class="fas fa-eye"></i></button></div><p class="error-msg" id="regConfirmErr">Passwords do not match</p></div>
      <button type="submit" class="btn-primary w-full py-4">Create Account</button>
    </form>
    <p class="text-center text-sm text-[var(--text-muted)] mt-5">Already have an account? <a href="javascript:void(0)" id="goToLogin" class="text-[var(--accent)] font-semibold hover:underline">Sign In</a></p>
  </div>
</div>

<!-- OTP MODAL -->
<div class="modal-overlay" id="otpModal">
  <div class="modal-box text-center">
    <div class="w-16 h-16 rounded-full bg-[rgba(155,89,182,0.1)] flex items-center justify-center mx-auto mb-4"><i class="fas fa-shield-alt text-purple-400 text-2xl"></i></div>
    <h2 class="text-2xl font-black mb-2" style="font-family:'Outfit'">Verify Your Email</h2>
    <p class="text-sm text-[var(--text-muted)] mb-1">We sent a 6-digit OTP to</p>
    <p class="text-sm font-bold text-[var(--accent)] mb-6" id="otpEmailDisplay">—</p>
    <p class="text-xs text-[var(--gold)] mb-6 bg-[rgba(255,200,87,0.1)] rounded-xl p-3"><i class="fas fa-info-circle mr-1"></i>Demo mode: check the toast notification for your OTP code</p>
    <div class="flex justify-center gap-2 mb-4" id="otpInputs">
      <input type="text" class="otp-input" maxlength="1" data-idx="0">
      <input type="text" class="otp-input" maxlength="1" data-idx="1">
      <input type="text" class="otp-input" maxlength="1" data-idx="2">
      <input type="text" class="otp-input" maxlength="1" data-idx="3">
      <input type="text" class="otp-input" maxlength="1" data-idx="4">
      <input type="text" class="otp-input" maxlength="1" data-idx="5">
    </div>
    <p class="error-msg text-center mb-4" id="otpErr">Incorrect OTP. Please try again.</p>
    <button id="verifyOtpBtn" class="btn-primary w-full py-4 mb-3">Verify OTP</button>
    <button id="resendOtpBtn" class="btn-secondary w-full py-3 text-sm">Resend OTP</button>
    <button id="cancelOtpBtn" class="text-sm text-[var(--text-muted)] mt-3 hover:text-[var(--danger)] transition-colors">Cancel Registration</button>
  </div>
</div>

<!-- ADD/EDIT ITEM MODAL -->
<div class="modal-overlay" id="itemModal">
  <div class="modal-box">
    <div class="flex items-center justify-between mb-6">
      <h2 class="text-2xl font-black" style="font-family:'Outfit'" id="itemModalTitle">Add Menu Item</h2>
      <button class="close-modal-btn w-10 h-10 rounded-full flex items-center justify-center hover:bg-[var(--surface2)] transition-colors" data-modal="itemModal"><i class="fas fa-times text-[var(--text-muted)]"></i></button>
    </div>
    <form id="itemForm" novalidate>
      <input type="hidden" id="editItemId" value="">
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Item Name</label><input type="text" class="input-field" id="itemName" placeholder="e.g. Classic Burger"><p class="error-msg" id="itemNameErr">Please enter an item name</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Description</label><textarea class="input-field" id="itemDesc" rows="2" placeholder="Brief description..."></textarea><p class="error-msg" id="itemDescErr">Please enter a description</p></div>
      <div class="grid grid-cols-2 gap-4 mb-4">
        <div><label class="text-sm text-[var(--text-muted)] mb-1 block">Price ($)</label><input type="number" step="0.01" min="0.01" class="input-field" id="itemPrice" placeholder="12.99"><p class="error-msg" id="itemPriceErr">Enter a valid price</p></div>
        <div><label class="text-sm text-[var(--text-muted)] mb-1 block">Category</label><select class="input-field" id="itemCategory"><option value="Burgers">Burgers</option><option value="Pizza">Pizza</option><option value="Sushi">Sushi</option><option value="Pasta">Pasta</option><option value="Desserts">Desserts</option><option value="Drinks">Drinks</option></select></div>
      </div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Image URL (optional)</label><input type="text" class="input-field" id="itemImage" placeholder="https://picsum.photos/seed/food/400/300.jpg"></div>
      <div class="flex items-center gap-3 mb-6"><input type="checkbox" id="itemActive" checked class="w-5 h-5 accent-[var(--accent)]"><label for="itemActive" class="text-sm">Item is active and visible</label></div>
      <div class="flex gap-3"><button type="button" class="close-modal-btn btn-secondary flex-1" data-modal="itemModal">Cancel</button><button type="submit" class="btn-primary flex-1">Save Item</button></div>
    </form>
  </div>
</div>

<!-- ADD USER MODAL (Admin) -->
<div class="modal-overlay" id="addUserModal">
  <div class="modal-box">
    <div class="flex items-center justify-between mb-6">
      <h2 class="text-2xl font-black" style="font-family:'Outfit'">Add New User</h2>
      <button class="close-modal-btn w-10 h-10 rounded-full flex items-center justify-center hover:bg-[var(--surface2)] transition-colors" data-modal="addUserModal"><i class="fas fa-times text-[var(--text-muted)]"></i></button>
    </div>
    <form id="addUserForm" novalidate>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Full Name</label><input type="text" class="input-field" id="auName" placeholder="John Doe"><p class="error-msg" id="auNameErr">Name must be at least 2 characters</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Email Address</label><input type="email" class="input-field" id="auEmail" placeholder="you@example.com"><p class="error-msg" id="auEmailErr">Please enter a valid email</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Phone Number</label><input type="tel" class="input-field" id="auPhone" placeholder="+1 234 567 8900"><p class="error-msg" id="auPhoneErr">Enter a valid phone number</p></div>
      <div class="mb-4"><label class="text-sm text-[var(--text-muted)] mb-1 block">Password</label><input type="text" class="input-field" id="auPassword" placeholder="Min 6 characters with a number"><p class="error-msg" id="auPasswordErr">Min 6 characters with a number</p></div>
      <div class="mb-6"><label class="text-sm text-[var(--text-muted)] mb-1 block">Role</label><select class="input-field" id="auRole"><option value="user">User</option><option value="admin">Admin</option></select></div>
      <div class="flex gap-3"><button type="button" class="close-modal-btn btn-secondary flex-1" data-modal="addUserModal">Cancel</button><button type="submit" class="btn-primary flex-1">Add User</button></div>
    </form>
  </div>
</div>

<!-- ORDER NOTIFICATION MODAL -->
<div class="modal-overlay" id="orderNotifModal">
  <div class="modal-box">
    <div class="text-center mb-4">
      <div class="w-16 h-16 rounded-full bg-[rgba(255,107,53,0.1)] flex items-center justify-center mx-auto mb-3 pulse-ring"><i class="fas fa-bell text-[var(--accent)] text-2xl"></i></div>
      <h2 class="text-2xl font-black" style="font-family:'Outfit'">New Order Received</h2>
      <p class="text-sm text-[var(--text-muted)] mt-1">A customer just placed an order</p>
    </div>
    <div class="bg-[var(--bg)] rounded-xl p-4 mb-4" id="notifOrderDetails"></div>
    <div class="flex gap-3">
      <button id="declineOrderBtn" class="btn-danger flex-1"><i class="fas fa-times mr-2"></i>Decline</button>
      <button id="acceptOrderBtn" class="btn-success flex-1"><i class="fas fa-check mr-2"></i>Accept</button>
    </div>
  </div>
</div>

<!-- DELETE CONFIRM MODAL -->
<div class="modal-overlay" id="deleteConfirmModal">
  <div class="modal-box text-center">
    <div class="w-16 h-16 rounded-full bg-[rgba(231,76,60,0.1)] flex items-center justify-center mx-auto mb-4"><i class="fas fa-exclamation-triangle text-[var(--danger)] text-2xl"></i></div>
    <h2 class="text-xl font-black mb-2" style="font-family:'Outfit'">Confirm Deletion</h2>
    <p class="text-sm text-[var(--text-muted)] mb-6" id="deleteConfirmText">Are you sure you want to delete this?</p>
    <div class="flex gap-3">
      <button class="close-modal-btn btn-secondary flex-1" data-modal="deleteConfirmModal">Cancel</button>
      <button id="confirmDeleteBtn" class="btn-danger flex-1"><i class="fas fa-trash mr-2"></i>Delete</button>
    </div>
  </div>
</div>

<script>
/* =============================================
   DATA
============================================= */
var DEFAULT_MENU = [
  {id:1,name:"Classic Smash Burger",desc:"Double smashed patties, American cheese, pickles, special sauce",price:12.99,category:"Burgers",image:"https://picsum.photos/seed/burger1/400/300.jpg",active:true,rating:4.8,orders:234},
  {id:2,name:"Wagyu Deluxe Burger",desc:"Premium wagyu beef, truffle aioli, caramelized onions, aged cheddar",price:24.99,category:"Burgers",image:"https://picsum.photos/seed/burger2/400/300.jpg",active:true,rating:4.9,orders:189},
  {id:3,name:"Spicy Chicken Burger",desc:"Crispy fried chicken, sriracha mayo, jalapenos, coleslaw",price:14.99,category:"Burgers",image:"https://picsum.photos/seed/burger3/400/300.jpg",active:true,rating:4.7,orders:312},
  {id:4,name:"Margherita Pizza",desc:"San Marzano tomatoes, fresh mozzarella, basil, olive oil",price:15.99,category:"Pizza",image:"https://picsum.photos/seed/pizza1/400/300.jpg",active:true,rating:4.8,orders:456},
  {id:5,name:"Pepperoni Supreme",desc:"Double pepperoni, mozzarella, oregano, tomato sauce",price:17.99,category:"Pizza",image:"https://picsum.photos/seed/pizza2/400/300.jpg",active:true,rating:4.6,orders:387},
  {id:6,name:"BBQ Chicken Pizza",desc:"Grilled chicken, BBQ sauce, red onion, cilantro",price:18.99,category:"Pizza",image:"https://picsum.photos/seed/pizza3/400/300.jpg",active:true,rating:4.7,orders:278},
  {id:7,name:"Salmon Nigiri Set",desc:"8 pieces premium salmon over seasoned rice",price:22.99,category:"Sushi",image:"https://picsum.photos/seed/sushi1/400/300.jpg",active:true,rating:4.9,orders:198},
  {id:8,name:"Dragon Roll",desc:"Tempura shrimp, avocado, eel sauce, tobiko",price:19.99,category:"Sushi",image:"https://picsum.photos/seed/sushi2/400/300.jpg",active:true,rating:4.8,orders:245},
  {id:9,name:"Spicy Tuna Roll",desc:"Fresh tuna, spicy mayo, cucumber, sesame seeds",price:16.99,category:"Sushi",image:"https://picsum.photos/seed/sushi3/400/300.jpg",active:true,rating:4.7,orders:167},
  {id:10,name:"Carbonara",desc:"Guanciale, pecorino romano, egg yolk, black pepper",price:16.99,category:"Pasta",image:"https://picsum.photos/seed/pasta1/400/300.jpg",active:true,rating:4.8,orders:321},
  {id:11,name:"Truffle Mushroom Pasta",desc:"Wild mushrooms, truffle oil, parmesan, fresh herbs",price:19.99,category:"Pasta",image:"https://picsum.photos/seed/pasta2/400/300.jpg",active:true,rating:4.9,orders:189},
  {id:12,name:"Spicy Arrabbiata",desc:"Penne, tomato sauce, chili flakes, garlic, basil",price:13.99,category:"Pasta",image:"https://picsum.photos/seed/pasta3/400/300.jpg",active:true,rating:4.6,orders:267},
  {id:13,name:"Chocolate Lava Cake",desc:"Molten dark chocolate center, vanilla ice cream, berry compote",price:10.99,category:"Desserts",image:"https://picsum.photos/seed/dessert1/400/300.jpg",active:true,rating:4.9,orders:412},
  {id:14,name:"Tiramisu",desc:"Espresso-soaked ladyfingers, mascarpone, cocoa dust",price:9.99,category:"Desserts",image:"https://picsum.photos/seed/dessert2/400/300.jpg",active:true,rating:4.8,orders:356},
  {id:15,name:"Matcha Cheesecake",desc:"Japanese matcha, creamy cheesecake, graham crust",price:11.99,category:"Desserts",image:"https://picsum.photos/seed/dessert3/400/300.jpg",active:true,rating:4.7,orders:198},
  {id:16,name:"Mango Smoothie",desc:"Fresh mango, banana, yogurt, honey blend",price:7.99,category:"Drinks",image:"https://picsum.photos/seed/drink1/400/300.jpg",active:true,rating:4.6,orders:534},
  {id:17,name:"Iced Caramel Latte",desc:"Espresso, caramel syrup, cold milk, ice",price:6.99,category:"Drinks",image:"https://picsum.photos/seed/drink2/400/300.jpg",active:true,rating:4.7,orders:678},
  {id:18,name:"Berry Blast Cooler",desc:"Mixed berries, lime, sparkling water, mint",price:8.99,category:"Drinks",image:"https://picsum.photos/seed/drink3/400/300.jpg",active:true,rating:4.5,orders:289}
];

var DEFAULT_USERS = [
  {id:1,name:"Admin",email:"admin@foodverse.com",password:"admin123",phone:"+1 000 000 0000",role:"admin",orderCount:0,joined:"2024-01-01"}
];

/* =============================================
   STATE
============================================= */
var state = {
  currentUser: null,
  users: [],
  menu: [],
  orders: [],
  cart: [],
  currentPage: 'home',
  selectedCategory: 'All',
  selectedPayment: 'upi',
  pendingNotifOrderId: null,
  pendingRegData: null,
  currentOtp: null,
  nextOrderId: 1001,
  nextItemId: 100,
  nextUserId: 10,
  deleteCallback: null
};

/* =============================================
   LOCAL STORAGE (simulated database)
============================================= */
function loadState() {
  try {
    var saved = localStorage.getItem('foodverse_db');
    if (saved) {
      var p = JSON.parse(saved);
      state.users = p.users || JSON.parse(JSON.stringify(DEFAULT_USERS));
      state.menu = p.menu || JSON.parse(JSON.stringify(DEFAULT_MENU));
      state.orders = p.orders || [];
      state.currentUser = p.currentUser || null;
      state.nextOrderId = p.nextOrderId || 1001;
      state.nextItemId = p.nextItemId || 100;
      state.nextUserId = p.nextUserId || 10;
    } else {
      state.users = JSON.parse(JSON.stringify(DEFAULT_USERS));
      state.menu = JSON.parse(JSON.stringify(DEFAULT_MENU));
      state.orders = [];
      state.currentUser = null;
    }
  } catch(e) {
    state.users = JSON.parse(JSON.stringify(DEFAULT_USERS));
    state.menu = JSON.parse(JSON.stringify(DEFAULT_MENU));
    state.orders = [];
    state.currentUser = null;
  }
}

function saveState() {
  try {
    localStorage.setItem('foodverse_db', JSON.stringify({
      users: state.users,
      menu: state.menu,
      orders: state.orders,
      currentUser: state.currentUser,
      nextOrderId: state.nextOrderId,
      nextItemId: state.nextItemId,
      nextUserId: state.nextUserId
    }));
  } catch(e) { console.warn('Storage full'); }
}

/* =============================================
   UTILITIES
============================================= */
function showToast(message, type) {
  type = type || 'info';
  var container = document.getElementById('toastContainer');
  var toast = document.createElement('div');
  toast.className = 'toast ' + type;
  var icons = {'new-order':'fa-bell','success':'fa-check-circle','error':'fa-exclamation-circle','info':'fa-info-circle','otp':'fa-key'};
  var colors = {'new-order':'var(--accent)','success':'var(--success)','error':'var(--danger)','info':'var(--gold)','otp':'#9b59b6'};
  toast.innerHTML = '<div class="flex items-start gap-3"><i class="fas '+(icons[type]||icons.info)+' mt-0.5" style="color:'+(colors[type]||colors.info)+'"></i><div class="flex-1"><p class="text-sm font-medium">'+message+'</p><button class="toast-dismiss text-xs text-[var(--text-muted)] mt-1 hover:text-[var(--text)]">Dismiss</button></div></div>';
  container.appendChild(toast);
  setTimeout(function(){ toast.classList.add('show'); }, 10);
  var dismissBtn = toast.querySelector('.toast-dismiss');
  dismissBtn.addEventListener('click', function(){ removeToast(toast); });
  setTimeout(function(){ removeToast(toast); }, 10000);
}

function removeToast(toast) {
  if (!toast.parentNode) return;
  toast.classList.remove('show');
  setTimeout(function(){ if(toast.parentNode) toast.parentNode.removeChild(toast); }, 400);
}

function openModal(id) {
  document.getElementById(id).classList.add('active');
  document.body.style.overflow = 'hidden';
}
function closeModal(id) {
  document.getElementById(id).classList.remove('active');
  // Only restore scroll if no other modals are open
  var anyOpen = document.querySelector('.modal-overlay.active');
  if (!anyOpen) document.body.style.overflow = '';
}

function showFieldError(fid, eid) {
  document.getElementById(fid).classList.add('error');
  document.getElementById(eid).classList.add('show');
}
function clearFieldError(fid, eid) {
  document.getElementById(fid).classList.remove('error');
  document.getElementById(eid).classList.remove('show');
}
function clearAllErrors(formId) {
  var form = document.getElementById(formId);
  if (!form) return;
  var fields = form.querySelectorAll('.input-field');
  for (var i = 0; i < fields.length; i++) fields[i].classList.remove('error');
  var errs = form.querySelectorAll('.error-msg');
  for (var i = 0; i < errs.length; i++) errs[i].classList.remove('show');
}

function isValidEmail(e) { return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(e); }
function isValidPhone(p) { return p.replace(/\D/g,'').length >= 10; }
function isValidName(n) { return /^[a-zA-Z\s]{2,}$/.test(n.trim()); }
function isValidPassword(p) { return p.length >= 6 && /\d/.test(p); }

function generateOtp() {
  var otp = '';
  for (var i = 0; i < 6; i++) otp += Math.floor(Math.random() * 10);
  return otp;
}

/* =============================================
   NAVIGATION
============================================= */
function navigate(page, extra) {
  if ((page === 'checkout' || page === 'orders') && !state.currentUser) {
    showToast('Please login to continue', 'error');
    openModal('loginModal');
    return;
  }
  if (page === 'admin' && (!state.currentUser || state.currentUser.role !== 'admin')) {
    showToast('Access denied. Admin only.', 'error');
    return;
  }
  state.currentPage = page;
  var pages = document.querySelectorAll('.page');
  for (var i = 0; i < pages.length; i++) pages[i].classList.remove('active');
  var target = document.getElementById('page-' + page);
  if (target) target.classList.add('active');
  var links = document.querySelectorAll('.nav-link');
  for (var i = 0; i < links.length; i++) {
    var lp = links[i].getAttribute('data-page');
    if (lp === page) {
      links[i].classList.add('text-[var(--accent)]');
      links[i].classList.add('bg-[rgba(255,107,53,0.1)]');
    } else {
      links[i].classList.remove('text-[var(--accent)]');
      links[i].classList.remove('bg-[rgba(255,107,53,0.1)]');
    }
  }
  if (page === 'menu') {
    if (extra) state.selectedCategory = extra;
    renderMenu();
  }
  if (page === 'checkout') renderCheckout();
  if (page === 'orders') renderUserOrders();
  if (page === 'admin') renderAdmin();
  window.scrollTo({top:0, behavior:'smooth'});
}

/* =============================================
   AUTH UI
============================================= */
function updateAuthUI() {
  var container = document.getElementById('authButtons');
  if (state.currentUser) {
    var isAdmin = state.currentUser.role === 'admin';
    var html = '<div class="hidden md:flex items-center gap-2">';
    if (isAdmin) html += '<button class="nav-link px-4 py-2 rounded-xl text-sm font-medium transition-all hover:bg-[rgba(255,107,53,0.1)] hover:text-[var(--accent)]" data-page="admin">Dashboard</button>';
    if (!isAdmin) html += '<button class="nav-link px-4 py-2 rounded-xl text-sm font-medium transition-all hover:bg-[rgba(255,107,53,0.1)] hover:text-[var(--accent)]" data-page="orders">Orders</button>';
    html += '</div>';
    html += '<div class="relative group"><button class="flex items-center gap-2 px-3 py-2 rounded-xl bg-[var(--surface2)] border border-[var(--border)] hover:border-[var(--accent)] transition-all"><div class="w-8 h-8 rounded-lg bg-gradient-to-br from-[var(--accent)] to-[var(--gold)] flex items-center justify-center text-white text-sm font-bold">'+state.currentUser.name.charAt(0).toUpperCase()+'</div><span class="hidden sm:block text-sm font-medium max-w-[100px] truncate">'+state.currentUser.name.split(' ')[0]+'</span><i class="fas fa-chevron-down text-xs text-[var(--text-muted)]"></i></button>';
    html += '<div class="absolute right-0 top-full mt-2 w-56 bg-[var(--surface)] border border-[var(--border)] rounded-xl shadow-2xl opacity-0 pointer-events-none group-hover:opacity-100 group-hover:pointer-events-all transition-all z-50 overflow-hidden"><div class="p-4 border-b border-[var(--border)]"><p class="font-bold text-sm">'+state.currentUser.name+'</p><p class="text-xs text-[var(--text-muted)]">'+state.currentUser.email+'</p><span class="inline-block mt-1 px-2 py-0.5 rounded-full text-[10px] font-bold uppercase tracking-wider '+(isAdmin?'bg-[rgba(255,107,53,0.1)] text-[var(--accent)]':'bg-[rgba(46,204,113,0.1)] text-[var(--success)]')+'">'+state.currentUser.role+'</span></div><div class="p-2"><button class="logout-btn w-full text-left px-3 py-2 rounded-lg text-sm hover:bg-[var(--surface2)] transition-colors text-[var(--danger)]"><i class="fas fa-sign-out-alt mr-2"></i>Logout</button></div></div></div>';
    container.innerHTML = html;
    // Bind nav links in auth
    bindNavLinks();
    // Bind logout
    var lb = container.querySelector('.logout-btn');
    if (lb) lb.addEventListener('click', handleLogout);
  } else {
    container.innerHTML = '<button id="signInBtn" class="btn-secondary text-sm py-2 px-5">Sign In</button><button id="signUpBtn" class="btn-primary text-sm py-2 px-5 hidden sm:block">Sign Up</button>';
    document.getElementById('signInBtn').addEventListener('click', function(){ openModal('loginModal'); });
    document.getElementById('signUpBtn').addEventListener('click', function(){ openModal('registerModal'); });
  }
}

function bindNavLinks() {
  var links = document.querySelectorAll('.nav-link');
  for (var i = 0; i < links.length; i++) {
    (function(link){
      link.removeEventListener('click', link._navHandler);
      link._navHandler = function(e) {
        e.preventDefault();
        e.stopPropagation();
        var page = link.getAttribute('data-page');
        if (page) navigate(page);
      };
      link.addEventListener('click', link._navHandler);
    })(links[i]);
  }
}

function handleLogout() {
  state.currentUser = null;
  saveState();
  updateAuthUI();
  navigate('home');
  showToast('Logged out successfully', 'info');
}

/* =============================================
   LOGIN
============================================= */
function handleLogin(e) {
  e.preventDefault();
  clearAllErrors('loginForm');
  var valid = true;
  var email = document.getElementById('loginEmail').value.trim();
  var password = document.getElementById('loginPassword').value;

  if (!isValidEmail(email)) { showFieldError('loginEmail','loginEmailErr'); valid = false; }
  if (!isValidPassword(password)) { showFieldError('loginPassword','loginPasswordErr'); valid = false; }
  if (!valid) return false;

  // Find user
  var user = null;
  for (var i = 0; i < state.users.length; i++) {
    if (state.users[i].email === email && state.users[i].password === password) {
      user = state.users[i];
      break;
    }
  }

  if (!user) {
    document.getElementById('loginEmailErr').textContent = 'Invalid email or password';
    document.getElementById('loginEmailErr').classList.add('show');
    document.getElementById('loginEmail').classList.add('error');
    return false;
  }

  state.currentUser = {id:user.id, name:user.name, email:user.email, phone:user.phone, role:user.role, password:user.password};
  saveState();
  closeModal('loginModal');
  updateAuthUI();
  showToast('Welcome back, ' + user.name + '!', 'success');
  document.getElementById('loginForm').reset();
  // Reset error text
  document.getElementById('loginEmailErr').textContent = 'Please enter a valid email address';

  if (user.role === 'admin') {
    var pending = [];
    for (var i = 0; i < state.orders.length; i++) { if(state.orders[i].status==='pending') pending.push(state.orders[i]); }
    if (pending.length > 0) {
      setTimeout(function(){ showToast('You have ' + pending.length + ' pending order(s)', 'new-order'); }, 500);
    }
  }
  return false;
}

/* =============================================
   REGISTER + OTP
============================================= */
function handleRegister(e) {
  e.preventDefault();
  clearAllErrors('registerForm');
  var valid = true;
  var name = document.getElementById('regName').value.trim();
  var email = document.getElementById('regEmail').value.trim();
  var phone = document.getElementById('regPhone').value.trim();
  var password = document.getElementById('regPassword').value;
  var confirm = document.getElementById('regConfirm').value;

  // Reset custom error text
  document.getElementById('regEmailErr').textContent = 'Please enter a valid email address';

  if (!isValidName(name)) { showFieldError('regName','regNameErr'); valid = false; }
  if (!isValidEmail(email)) { showFieldError('regEmail','regEmailErr'); valid = false; }
  if (!isValidPhone(phone)) { showFieldError('regPhone','regPhoneErr'); valid = false; }
  if (!isValidPassword(password)) { showFieldError('regPassword','regPasswordErr'); valid = false; }
  if (password !== confirm) { showFieldError('regConfirm','regConfirmErr'); valid = false; }
  if (!valid) return false;

  // Check duplicate email ONLY after all other validations pass
  var dup = false;
  for (var i = 0; i < state.users.length; i++) {
    if (state.users[i].email.toLowerCase() === email.toLowerCase()) { dup = true; break; }
  }
  if (dup) {
    document.getElementById('regEmailErr').textContent = 'This email is already registered. Try another or sign in.';
    document.getElementById('regEmailErr').classList.add('show');
    document.getElementById('regEmail').classList.add('error');
    return false;
  }

  // Store pending registration data and send OTP
  state.pendingRegData = {name:name, email:email, phone:phone, password:password};
  sendOtp(email);
  return false;
}

function sendOtp(email) {
  var otp = generateOtp();
  state.currentOtp = otp;
  document.getElementById('otpEmailDisplay').textContent = email;
  // Clear OTP inputs
  var inputs = document.querySelectorAll('#otpInputs .otp-input');
  for (var i = 0; i < inputs.length; i++) { inputs[i].value = ''; inputs[i].classList.remove('error'); }
  document.getElementById('otpErr').classList.remove('show');
  closeModal('registerModal');
  openModal('otpModal');
  showToast('Your OTP code is: ' + otp, 'otp');
  // Focus first input
  setTimeout(function(){ inputs[0].focus(); }, 300);
}

function handleVerifyOtp() {
  var inputs = document.querySelectorAll('#otpInputs .otp-input');
  var entered = '';
  for (var i = 0; i < inputs.length; i++) entered += inputs[i].value;
  document.getElementById('otpErr').classList.remove('show');

  if (entered.length !== 6) {
    document.getElementById('otpErr').textContent = 'Please enter all 6 digits';
    document.getElementById('otpErr').classList.add('show');
    for (var i = 0; i < inputs.length; i++) { if(!inputs[i].value) inputs[i].classList.add('error'); }
    return;
  }

  if (entered !== state.currentOtp) {
    document.getElementById('otpErr').textContent = 'Incorrect OTP. Please try again.';
    document.getElementById('otpErr').classList.add('show');
    for (var i = 0; i < inputs.length; i++) inputs[i].classList.add('error');
    return;
  }

  // OTP correct — create user
  var d = state.pendingRegData;
  var newUser = {
    id: state.nextUserId++,
    name: d.name, email: d.email, password: d.password,
    phone: d.phone, role: 'user', orderCount: 0,
    joined: new Date().toISOString().split('T')[0]
  };
  state.users.push(newUser);
  state.currentUser = {id:newUser.id, name:newUser.name, email:newUser.email, phone:newUser.phone, role:newUser.role, password:newUser.password};
  saveState();
  closeModal('otpModal');
  updateAuthUI();
  showToast('Welcome to FoodVerse, ' + d.name + '!', 'success');
  document.getElementById('registerForm').reset();
  state.pendingRegData = null;
  state.currentOtp = null;
}

function handleResendOtp() {
  if (!state.pendingRegData) return;
  var otp = generateOtp();
  state.currentOtp = otp;
  var inputs = document.querySelectorAll('#otpInputs .otp-input');
  for (var i = 0; i < inputs.length; i++) { inputs[i].value = ''; inputs[i].classList.remove('error'); }
  document.getElementById('otpErr').classList.remove('show');
  showToast('New OTP: ' + otp, 'otp');
  setTimeout(function(){ inputs[0].focus(); }, 200);
}

function handleCancelOtp() {
  closeModal('otpModal');
  state.pendingRegData = null;
  state.currentOtp = null;
  openModal('registerModal');
}

/* =============================================
   MENU RENDERING
============================================= */
var catIcons = {Burgers:'fa-hamburger',Pizza:'fa-pizza-slice',Sushi:'fa-fish',Pasta:'fa-utensils',Desserts:'fa-ice-cream',Drinks:'fa-glass-martini-alt'};
var catColors = {Burgers:'var(--accent)',Pizza:'var(--gold)',Sushi:'#00bcd4',Pasta:'#e91e63',Desserts:'#9c27b0',Drinks:'var(--success)'};

function renderHomeCategories() {
  var cats = ['Burgers','Pizza','Sushi','Pasta','Desserts','Drinks'];
  var grid = document.getElementById('homeCatGrid');
  var html = '';
  for (var i = 0; i < cats.length; i++) {
    var c = cats[i];
    html += '<div class="scene-inner"><div class="card-3d bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl p-6 text-center cursor-pointer home-cat-btn" data-cat="'+c+'"><div class="text-3xl mb-3"><i class="fas '+(catIcons[c]||'fa-utensils')+' text-'+(catColors[c]||'var(--accent)')+'"></i></div><p class="font-semibold text-sm" style="font-family:Outfit">'+c+'</p></div></div>';
  }
  grid.innerHTML = html;
  var btns = grid.querySelectorAll('.home-cat-btn');
  for (var i = 0; i < btns.length; i++) {
    btns[i].addEventListener('click', function(){ navigate('menu', this.getAttribute('data-cat')); });
  }
}

function renderCategoryPills() {
  var catSet = {};
  catSet['All'] = true;
  for (var i = 0; i < state.menu.length; i++) {
    if (state.menu[i].active) catSet[state.menu[i].category] = true;
  }
  var cats = Object.keys(catSet);
  var container = document.getElementById('categoryPills');
  var html = '';
  for (var i = 0; i < cats.length; i++) {
    html += '<button class="cat-pill '+(state.selectedCategory===cats[i]?'active':'')+'" data-cat="'+cats[i]+'">'+cats[i]+'</button>';
  }
  container.innerHTML = html;
  var btns = container.querySelectorAll('.cat-pill');
  for (var i = 0; i < btns.length; i++) {
    btns[i].addEventListener('click', function(){
      state.selectedCategory = this.getAttribute('data-cat');
      renderMenu();
    });
  }
}

function renderMenu() {
  renderCategoryPills();
  var items = [];
  for (var i = 0; i < state.menu.length; i++) {
    var it = state.menu[i];
    if (it.active && (state.selectedCategory === 'All' || it.category === state.selectedCategory)) items.push(it);
  }
  var grid = document.getElementById('menuGrid');
  grid.innerHTML = renderFoodCards(items);
  bindCartButtons(grid);
}

function renderPopularGrid() {
  var sorted = state.menu.filter(function(i){return i.active;}).slice().sort(function(a,b){return (b.orders||0)-(a.orders||0);}).slice(0,4);
  var grid = document.getElementById('popularGrid');
  grid.innerHTML = renderFoodCards(sorted);
  bindCartButtons(grid);
}

function renderFoodCards(items) {
  var html = '';
  for (var i = 0; i < items.length; i++) {
    var item = items[i];
    var inCart = null;
    for (var j = 0; j < state.cart.length; j++) { if(state.cart[j].id===item.id){inCart=state.cart[j];break;} }
    var qty = inCart ? inCart.qty : 0;
    html += '<div class="scene-inner"><div class="card-3d bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl overflow-hidden group"><div class="relative overflow-hidden"><img src="'+item.image+'" alt="'+item.name+'" class="w-full h-48 object-cover transition-transform duration-500 group-hover:scale-110" loading="lazy"><div class="absolute top-3 left-3 px-2 py-1 rounded-lg bg-black/60 backdrop-blur-sm text-xs font-semibold"><i class="fas fa-star text-[var(--gold)] mr-1"></i>'+(item.rating||'4.7')+'</div><div class="absolute top-3 right-3 px-2 py-1 rounded-lg bg-black/60 backdrop-blur-sm text-xs">'+item.category+'</div></div><div class="p-5"><h3 class="font-bold text-base mb-1" style="font-family:Outfit">'+item.name+'</h3><p class="text-xs text-[var(--text-muted)] mb-3 line-clamp-2 leading-relaxed">'+item.desc+'</p><div class="flex items-center justify-between"><span class="text-xl font-black text-[var(--accent)]" style="font-family:Outfit">$'+item.price.toFixed(2)+'</span>';
    if (qty === 0) {
      html += '<button class="add-cart-btn btn-primary text-xs py-2 px-4" data-itemid="'+item.id+'"><i class="fas fa-plus mr-1"></i>Add</button>';
    } else {
      html += '<div class="flex items-center gap-2"><button class="cart-qty-btn w-8 h-8 rounded-lg bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] transition-colors text-sm" data-itemid="'+item.id+'" data-delta="-1"><i class="fas fa-minus text-xs"></i></button><span class="font-bold text-sm w-5 text-center">'+qty+'</span><button class="cart-qty-btn w-8 h-8 rounded-lg bg-[var(--accent)] flex items-center justify-center text-white text-sm" data-itemid="'+item.id+'" data-delta="1"><i class="fas fa-plus text-xs"></i></button></div>';
    }
    html += '</div></div></div></div>';
  }
  return html;
}

function bindCartButtons(container) {
  var addBtns = container.querySelectorAll('.add-cart-btn');
  for (var i = 0; i < addBtns.length; i++) {
    addBtns[i].addEventListener('click', function(e){
      e.preventDefault(); e.stopPropagation();
      addToCart(parseInt(this.getAttribute('data-itemid')));
    });
  }
  var qtyBtns = container.querySelectorAll('.cart-qty-btn');
  for (var i = 0; i < qtyBtns.length; i++) {
    qtyBtns[i].addEventListener('click', function(e){
      e.preventDefault(); e.stopPropagation();
      updateCartQty(parseInt(this.getAttribute('data-itemid')), parseInt(this.getAttribute('data-delta')));
    });
  }
}

/* =============================================
   CART
============================================= */
function addToCart(itemId) {
  if (!state.currentUser) {
    showToast('Please login to add items to cart', 'error');
    openModal('loginModal');
    return;
  }
  var found = false;
  for (var i = 0; i < state.cart.length; i++) {
    if (state.cart[i].id === itemId) { state.cart[i].qty++; found = true; break; }
  }
  if (!found) {
    var item = null;
    for (var i = 0; i < state.menu.length; i++) { if(state.menu[i].id===itemId){item=state.menu[i];break;} }
    if (item) state.cart.push({id: itemId, qty: 1});
  }
  updateCartUI();
  refreshFoodCards();
  showToast('Item added to cart', 'success');
}

function updateCartQty(itemId, delta) {
  for (var i = 0; i < state.cart.length; i++) {
    if (state.cart[i].id === itemId) {
      state.cart[i].qty += delta;
      if (state.cart[i].qty <= 0) state.cart.splice(i, 1);
      break;
    }
  }
  updateCartUI();
  refreshFoodCards();
  if (state.currentPage === 'checkout') renderCheckout();
}

function removeFromCart(itemId) {
  for (var i = 0; i < state.cart.length; i++) {
    if (state.cart[i].id === itemId) { state.cart.splice(i, 1); break; }
  }
  updateCartUI();
  if (state.currentPage === 'checkout') renderCheckout();
}

function getCartTotal() {
  var sum = 0;
  for (var i = 0; i < state.cart.length; i++) {
    var item = null;
    for (var j = 0; j < state.menu.length; j++) { if(state.menu[j].id===state.cart[i].id){item=state.menu[j];break;} }
    if (item) sum += item.price * state.cart[i].qty;
  }
  return sum;
}

function refreshFoodCards() {
  renderPopularGrid();
  if (state.currentPage === 'menu') renderMenu();
}

function updateCartUI() {
  var badge = document.getElementById('cartBadge');
  var totalItems = 0;
  for (var i = 0; i < state.cart.length; i++) totalItems += state.cart[i].qty;
  badge.style.display = totalItems > 0 ? 'flex' : 'none';
  badge.textContent = totalItems;

  var container = document.getElementById('cartItems');
  var footer = document.getElementById('cartFooter');

  if (state.cart.length === 0) {
    container.innerHTML = '<div class="text-center text-[var(--text-muted)] py-12"><i class="fas fa-shopping-bag text-4xl mb-4 opacity-30"></i><p>Your cart is empty</p></div>';
    footer.style.display = 'none';
    return;
  }

  footer.style.display = 'block';
  var total = getCartTotal();
  document.getElementById('cartSubtotal').textContent = '$' + total.toFixed(2);
  document.getElementById('cartTotal').textContent = '$' + total.toFixed(2);

  var html = '';
  for (var i = 0; i < state.cart.length; i++) {
    var c = state.cart[i];
    var item = null;
    for (var j = 0; j < state.menu.length; j++) { if(state.menu[j].id===c.id){item=state.menu[j];break;} }
    if (!item) continue;
    html += '<div class="flex gap-3 mb-4 pb-4 border-b border-[var(--border)]"><img src="'+item.image+'" alt="'+item.name+'" class="w-16 h-16 rounded-xl object-cover flex-shrink-0"><div class="flex-1 min-w-0"><p class="font-semibold text-sm truncate">'+item.name+'</p><p class="text-[var(--accent)] font-bold text-sm">$'+(item.price*c.qty).toFixed(2)+'</p><div class="flex items-center gap-2 mt-1"><button class="cart-sidebar-qty w-6 h-6 rounded-md bg-[var(--surface2)] flex items-center justify-center text-xs hover:bg-[var(--border)] transition-colors" data-id="'+item.id+'" data-d="-1"><i class="fas fa-minus" style="font-size:10px"></i></button><span class="text-xs font-bold w-4 text-center">'+c.qty+'</span><button class="cart-sidebar-qty w-6 h-6 rounded-md bg-[var(--surface2)] flex items-center justify-center text-xs hover:bg-[var(--border)] transition-colors" data-id="'+item.id+'" data-d="1"><i class="fas fa-plus" style="font-size:10px"></i></button><button class="cart-sidebar-remove ml-auto text-[var(--text-muted)] hover:text-[var(--danger)] transition-colors" data-id="'+item.id+'"><i class="fas fa-trash" style="font-size:12px"></i></button></div></div></div>';
  }
  container.innerHTML = html;

  // Bind sidebar cart buttons
  var qtyBtns = container.querySelectorAll('.cart-sidebar-qty');
  for (var i = 0; i < qtyBtns.length; i++) {
    qtyBtns[i].addEventListener('click', function(){
      updateCartQty(parseInt(this.getAttribute('data-id')), parseInt(this.getAttribute('data-d')));
    });
  }
  var remBtns = container.querySelectorAll('.cart-sidebar-remove');
  for (var i = 0; i < remBtns.length; i++) {
    remBtns[i].addEventListener('click', function(){
      removeFromCart(parseInt(this.getAttribute('data-id')));
    });
  }
}

function toggleCart(open) {
  document.getElementById('cartSidebar').classList.toggle('open', open);
  document.getElementById('cartOverlay').classList.toggle('open', open);
  if (open) updateCartUI();
}

/* =============================================
   CHECKOUT & PAYMENT
============================================= */
function renderCheckout() {
  var container = document.getElementById('checkoutItems');
  var html = '';
  for (var i = 0; i < state.cart.length; i++) {
    var c = state.cart[i];
    var item = null;
    for (var j = 0; j < state.menu.length; j++) { if(state.menu[j].id===c.id){item=state.menu[j];break;} }
    if (!item) continue;
    html += '<div class="flex justify-between items-center"><div class="flex items-center gap-3"><img src="'+item.image+'" alt="'+item.name+'" class="w-10 h-10 rounded-lg object-cover"><div><p class="text-sm font-medium">'+item.name+'</p><p class="text-xs text-[var(--text-muted)]">x'+c.qty+'</p></div></div><span class="text-sm font-semibold">$'+(item.price*c.qty).toFixed(2)+'</span></div>';
  }
  container.innerHTML = html;
  var subtotal = getCartTotal();
  document.getElementById('checkSubtotal').textContent = '$' + subtotal.toFixed(2);
  document.getElementById('checkTotal').textContent = '$' + (subtotal + 2.99).toFixed(2);
  if (state.currentUser) {
    document.getElementById('checkName').value = state.currentUser.name || '';
    document.getElementById('checkPhone').value = state.currentUser.phone || '';
  }
}

function selectPayment(method) {
  state.selectedPayment = method;
  var cards = document.querySelectorAll('#paymentMethods .radio-card');
  for (var i = 0; i < cards.length; i++) {
    cards[i].classList.toggle('selected', cards[i].getAttribute('data-method') === method);
  }
  document.getElementById('cardFields').style.display = (method==='credit'||method==='debit') ? 'block' : 'none';
  document.getElementById('upiField').style.display = method==='upi' ? 'block' : 'none';
}

function placeOrder() {
  // Clear all checkout errors
  var ids = ['checkName','checkPhone','checkAddress','cardNumber','cardExpiry','cardCvv','upiId'];
  var eids = ['checkNameErr','checkPhoneErr','checkAddressErr','cardNumberErr','cardExpiryErr','cardCvvErr','upiIdErr'];
  for (var i = 0; i < ids.length; i++) {
    document.getElementById(ids[i]).classList.remove('error');
    document.getElementById(eids[i]).classList.remove('show');
  }

  var valid = true;
  var name = document.getElementById('checkName').value.trim();
  var phone = document.getElementById('checkPhone').value.trim();
  var address = document.getElementById('checkAddress').value.trim();

  if (!isValidName(name)) { showFieldError('checkName','checkNameErr'); valid = false; }
  if (!isValidPhone(phone)) { showFieldError('checkPhone','checkPhoneErr'); valid = false; }
  if (address.length < 5) { showFieldError('checkAddress','checkAddressErr'); valid = false; }

  if (state.selectedPayment === 'upi') {
    var upi = document.getElementById('upiId').value.trim();
    if (!/^[a-zA-Z0-9._-]+@[a-zA-Z]{2,}$/.test(upi)) { showFieldError('upiId','upiIdErr'); valid = false; }
  } else {
    var cardNum = document.getElementById('cardNumber').value.replace(/\s/g,'');
    var expiry = document.getElementById('cardExpiry').value;
    var cvv = document.getElementById('cardCvv').value;
    if (cardNum.length < 13 || !/^\d+$/.test(cardNum)) { showFieldError('cardNumber','cardNumberErr'); valid = false; }
    if (!/^\d{2}\/\d{2}$/.test(expiry)) { showFieldError('cardExpiry','cardExpiryErr'); valid = false; }
    if (cvv.length < 3 || !/^\d+$/.test(cvv)) { showFieldError('cardCvv','cardCvvErr'); valid = false; }
  }

  if (!valid) { showToast('Please fix the errors above', 'error'); return; }

  var subtotal = getCartTotal();
  var orderItems = [];
  for (var i = 0; i < state.cart.length; i++) {
    var c = state.cart[i];
    var item = null;
    for (var j = 0; j < state.menu.length; j++) { if(state.menu[j].id===c.id){item=state.menu[j];break;} }
    if (item) orderItems.push({name:item.name, price:item.price, qty:c.qty});
  }

  var order = {
    id: state.nextOrderId++,
    userId: state.currentUser.id,
    userName: name,
    userEmail: state.currentUser.email,
    userPhone: phone,
    address: address,
    items: orderItems,
    subtotal: subtotal,
    delivery: 2.99,
    total: subtotal + 2.99,
    payment: state.selectedPayment,
    status: 'pending',
    date: new Date().toISOString()
  };

  state.orders.push(order);
  state.cart = [];
  saveState();
  updateCartUI();
  refreshFoodCards();
  showToast('Order placed! Waiting for admin approval...', 'info');

  if (state.currentUser.role === 'admin') {
    setTimeout(function(){ showOrderNotification(order.id); }, 500);
  }

  navigate('orders');
}

/* =============================================
   ORDER NOTIFICATION
============================================= */
function showOrderNotification(orderId) {
  var order = null;
  for (var i = 0; i < state.orders.length; i++) { if(state.orders[i].id===orderId){order=state.orders[i];break;} }
  if (!order) return;
  state.pendingNotifOrderId = orderId;

  var itemsHtml = '';
  for (var i = 0; i < order.items.length; i++) {
    var it = order.items[i];
    itemsHtml += '<div class="flex justify-between text-sm"><span>'+it.name+' x'+it.qty+'</span><span>$'+(it.price*it.qty).toFixed(2)+'</span></div>';
  }

  document.getElementById('notifOrderDetails').innerHTML = '<div class="flex justify-between items-center mb-3"><span class="text-sm text-[var(--text-muted)]">Order #'+order.id+'</span><span class="text-xs px-2 py-1 rounded-full bg-[var(--gold)] text-black font-bold">Pending</span></div><p class="font-semibold">'+order.userName+'</p><p class="text-xs text-[var(--text-muted)] mb-2">'+order.address+'</p><div class="border-t border-[var(--border)] pt-2 mt-2 space-y-1">'+itemsHtml+'</div><div class="flex justify-between font-bold mt-2 pt-2 border-t border-[var(--border)]"><span>Total</span><span class="text-[var(--accent)]">$'+order.total.toFixed(2)+'</span></div><p class="text-xs text-[var(--text-muted)] mt-2"><i class="fas fa-mobile-alt mr-1"></i>Paid via '+order.payment.toUpperCase()+'</p>';

  openModal('orderNotifModal');
  showToast('New order #'+order.id+' from '+order.userName+' — $'+order.total.toFixed(2), 'new-order');
}

function handleOrderDecision(accept) {
  var order = null;
  for (var i = 0; i < state.orders.length; i++) { if(state.orders[i].id===state.pendingNotifOrderId){order=state.orders[i];break;} }
  if (order) {
    order.status = accept ? 'accepted' : 'declined';
    if (accept) {
      for (var i = 0; i < state.users.length; i++) {
        if (state.users[i].id === order.userId) { state.users[i].orderCount = (state.users[i].orderCount||0) + 1; break; }
      }
    }
    saveState();
    if (state.currentPage === 'admin') renderAdmin();
    if (state.currentPage === 'orders') renderUserOrders();
    showToast('Order #'+order.id+' '+(accept?'accepted':'declined'), accept?'success':'error');
  }
  closeModal('orderNotifModal');
  state.pendingNotifOrderId = null;
}

/* =============================================
   USER ORDERS
============================================= */
function renderUserOrders() {
  if (!state.currentUser) return;
  var userOrders = [];
  for (var i = 0; i < state.orders.length; i++) {
    if (state.orders[i].userId === state.currentUser.id) userOrders.push(state.orders[i]);
  }
  userOrders.sort(function(a,b){return new Date(b.date)-new Date(a.date);});
  var container = document.getElementById('userOrdersList');

  if (userOrders.length === 0) {
    container.innerHTML = '<div class="text-center py-20"><i class="fas fa-receipt text-5xl text-[var(--border)] mb-4"></i><p class="text-[var(--text-muted)] text-lg">No orders yet</p><button id="noOrdersMenuBtn" class="btn-primary mt-4">Browse Menu</button></div>';
    document.getElementById('noOrdersMenuBtn').addEventListener('click', function(){ navigate('menu'); });
    return;
  }

  var statusColors = {pending:'bg-[var(--gold)] text-black',accepted:'bg-[var(--success)] text-white',declined:'bg-[var(--danger)] text-white',delivered:'bg-[var(--accent)] text-white'};
  var statusIcons = {pending:'fa-clock',accepted:'fa-check-circle',declined:'fa-times-circle',delivered:'fa-truck'};

  var html = '';
  for (var i = 0; i < userOrders.length; i++) {
    var o = userOrders[i];
    var itemsHtml = '';
    for (var j = 0; j < o.items.length; j++) {
      itemsHtml += '<div class="flex justify-between text-sm"><span class="text-[var(--text-muted)]">'+o.items[j].name+' x'+o.items[j].qty+'</span><span>$'+(o.items[j].price*o.items[j].qty).toFixed(2)+'</span></div>';
    }
    var dateStr = new Date(o.date).toLocaleDateString('en-US',{month:'short',day:'numeric',year:'numeric',hour:'2-digit',minute:'2-digit'});
    html += '<div class="bg-[var(--card-bg)] border border-[var(--border)] rounded-2xl p-5 mb-4"><div class="flex items-center justify-between mb-3 flex-wrap gap-2"><div><span class="font-bold" style="font-family:Outfit">Order #'+o.id+'</span><span class="text-sm text-[var(--text-muted)] ml-2">'+dateStr+'</span></div><span class="px-3 py-1 rounded-full text-xs font-bold '+(statusColors[o.status]||statusColors.pending)+'"><i class="fas '+(statusIcons[o.status]||statusIcons.pending)+' mr-1"></i>'+o.status.charAt(0).toUpperCase()+o.status.slice(1)+'</span></div><div class="space-y-1 mb-3">'+itemsHtml+'</div><div class="flex justify-between items-center pt-3 border-t border-[var(--border)]"><span class="text-sm text-[var(--text-muted)]"><i class="fas fa-mobile-alt mr-1"></i>'+o.payment.toUpperCase()+'</span><span class="text-lg font-bold text-[var(--accent)]" style="font-family:Outfit">$'+o.total.toFixed(2)+'</span></div></div>';
  }
  container.innerHTML = html;
}

/* =============================================
   ADMIN DASHBOARD
============================================= */
function renderAdmin() {
  var allOrders = state.orders;
  var accepted = []; var pending = []; var revenue = 0;
  for (var i = 0; i < allOrders.length; i++) {
    if (allOrders[i].status === 'accepted' || allOrders[i].status === 'delivered') { accepted.push(allOrders[i]); revenue += allOrders[i].total; }
    if (allOrders[i].status === 'pending') pending.push(allOrders[i]);
  }
  document.getElementById('statOrders').textContent = allOrders.length;
  document.getElementById('statRevenue').textContent = '$' + revenue.toFixed(2);
  document.getElementById('statAccepted').textContent = accepted.length;
  document.getElementById('statPending').textContent = pending.length;
  renderAdminOrders();
  renderAdminItems();
  renderAdminUsers();
}

function switchAdminTab(tab) {
  var btns = document.querySelectorAll('#adminTabs .tab-btn');
  for (var i = 0; i < btns.length; i++) btns[i].classList.toggle('active', btns[i].getAttribute('data-tab')===tab);
  var tabs = document.querySelectorAll('.admin-tab');
  for (var i = 0; i < tabs.length; i++) tabs[i].style.display = 'none';
  document.getElementById('adminTab-'+tab).style.display = 'block';
}

function renderAdminOrders() {
  var body = document.getElementById('adminOrdersBody');
  var sorted = state.orders.slice().sort(function(a,b){return new Date(b.date)-new Date(a.date);});
  if (sorted.length === 0) { body.innerHTML = '<tr><td colspan="6" class="text-center py-12 text-[var(--text-muted)]">No orders yet</td></tr>'; return; }

  var statusColors = {pending:'bg-[var(--gold)] text-black',accepted:'bg-[var(--success)] text-white',declined:'bg-[var(--danger)] text-white',delivered:'bg-[var(--accent)] text-white'};
  var html = '';
  for (var i = 0; i < sorted.length; i++) {
    var o = sorted[i];
    var itemsStr = '';
    for (var j = 0; j < o.items.length; j++) itemsStr += o.items[j].name + ' x' + o.items[j].qty + ', ';
    itemsStr = itemsStr.slice(0,-2);
    var actions = '';
    if (o.status === 'pending') {
      actions = '<div class="flex gap-2"><button class="admin-accept btn-success text-xs py-1 px-3" data-oid="'+o.id+'"><i class="fas fa-check mr-1"></i>Accept</button><button class="admin-decline btn-danger text-xs py-1 px-3" data-oid="'+o.id+'"><i class="fas fa-times mr-1"></i>Decline</button></div>';
    } else if (o.status === 'accepted') {
      actions = '<button class="admin-deliver btn-primary text-xs py-1 px-3" data-oid="'+o.id+'"><i class="fas fa-truck mr-1"></i>Delivered</button>';
    } else {
      actions = '<span class="text-xs text-[var(--text-muted)]">—</span>';
    }
    html += '<tr><td class="font-mono text-sm">#'+o.id+'</td><td><p class="font-semibold text-sm">'+o.userName+'</p><p class="text-xs text-[var(--text-muted)]">'+o.userEmail+'</p></td><td class="text-sm max-w-[200px] truncate" title="'+itemsStr+'">'+itemsStr+'</td><td class="font-bold text-sm">$'+o.total.toFixed(2)+'</td><td><span class="px-2 py-1 rounded-full text-[10px] font-bold '+(statusColors[o.status]||'')+'">'+o.status.toUpperCase()+'</span></td><td>'+actions+'</td></tr>';
  }
  body.innerHTML = html;

  // Bind
  var acceptBtns = body.querySelectorAll('.admin-accept');
  for (var i = 0; i < acceptBtns.length; i++) {
    acceptBtns[i].addEventListener('click', function(){ adminDecideOrder(parseInt(this.getAttribute('data-oid')), true); });
  }
  var declineBtns = body.querySelectorAll('.admin-decline');
  for (var i = 0; i < declineBtns.length; i++) {
    declineBtns[i].addEventListener('click', function(){ adminDecideOrder(parseInt(this.getAttribute('data-oid')), false); });
  }
  var deliverBtns = body.querySelectorAll('.admin-deliver');
  for (var i = 0; i < deliverBtns.length; i++) {
    deliverBtns[i].addEventListener('click', function(){ markDelivered(parseInt(this.getAttribute('data-oid'))); });
  }
}

function adminDecideOrder(orderId, accept) {
  for (var i = 0; i < state.orders.length; i++) {
    if (state.orders[i].id === orderId) {
      state.orders[i].status = accept ? 'accepted' : 'declined';
      if (accept) {
        for (var j = 0; j < state.users.length; j++) {
          if (state.users[j].id === state.orders[i].userId) { state.users[j].orderCount = (state.users[j].orderCount||0)+1; break; }
        }
      }
      break;
    }
  }
  saveState(); renderAdmin();
  showToast('Order #'+orderId+' '+(accept?'accepted':'declined'), accept?'success':'error');
}

function markDelivered(orderId) {
  for (var i = 0; i < state.orders.length; i++) {
    if (state.orders[i].id === orderId) { state.orders[i].status = 'delivered'; break; }
  }
  saveState(); renderAdmin();
  showToast('Order #'+orderId+' marked as delivered', 'success');
}

function renderAdminItems() {
  var body = document.getElementById('adminItemsBody');
  var html = '';
  for (var i = 0; i < state.menu.length; i++) {
    var item = state.menu[i];
    html += '<tr><td><div class="flex items-center gap-3"><img src="'+item.image+'" alt="'+item.name+'" class="w-10 h-10 rounded-lg object-cover"><div><p class="font-semibold text-sm">'+item.name+'</p><p class="text-xs text-[var(--text-muted)] max-w-[200px] truncate">'+item.desc+'</p></div></div></td><td class="text-sm">'+item.category+'</td><td class="font-bold text-sm">$'+item.price.toFixed(2)+'</td><td><span class="px-2 py-1 rounded-full text-[10px] font-bold '+(item.active?'bg-[rgba(46,204,113,0.1)] text-[var(--success)]':'bg-[rgba(231,76,60,0.1)] text-[var(--danger)]')+'">'+(item.active?'Active':'Inactive')+'</span></td><td><div class="flex gap-2"><button class="admin-edit-btn w-8 h-8 rounded-lg bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--accent)] hover:text-[var(--accent)] transition-all text-xs" data-id="'+item.id+'"><i class="fas fa-edit"></i></button><button class="admin-toggle-btn w-8 h-8 rounded-lg bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--gold)] hover:text-[var(--gold)] transition-all text-xs" data-id="'+item.id+'"><i class="fas fa-eye'+(item.active?'-slash':'')+'"></i></button><button class="admin-delete-item-btn w-8 h-8 rounded-lg bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--danger)] hover:text-[var(--danger)] transition-all text-xs" data-id="'+item.id+'"><i class="fas fa-trash"></i></button></div></td></tr>';
  }
  body.innerHTML = html;

  var editBtns = body.querySelectorAll('.admin-edit-btn');
  for (var i = 0; i < editBtns.length; i++) { editBtns[i].addEventListener('click', function(){ editItem(parseInt(this.getAttribute('data-id'))); }); }
  var toggleBtns = body.querySelectorAll('.admin-toggle-btn');
  for (var i = 0; i < toggleBtns.length; i++) { toggleBtns[i].addEventListener('click', function(){ toggleItemActive(parseInt(this.getAttribute('data-id'))); }); }
  var delBtns = body.querySelectorAll('.admin-delete-item-btn');
  for (var i = 0; i < delBtns.length; i++) {
    delBtns[i].addEventListener('click', function(){
      var id = parseInt(this.getAttribute('data-id'));
      document.getElementById('deleteConfirmText').textContent = 'Are you sure you want to delete this menu item?';
      state.deleteCallback = function(){
        state.menu = state.menu.filter(function(it){return it.id!==id;});
        saveState(); renderAdmin();
        showToast('Item deleted', 'error');
      };
      openModal('deleteConfirmModal');
    });
  }
}

function renderAdminUsers() {
  var body = document.getElementById('adminUsersBody');
  var roleColors = {admin:'bg-[rgba(255,107,53,0.1)] text-[var(--accent)]',user:'bg-[rgba(46,204,113,0.1)] text-[var(--success)]'};
  var html = '';
  for (var i = 0; i < state.users.length; i++) {
    var u = state.users[i];
    var isSelf = state.currentUser && u.id === state.currentUser.id;
    html += '<tr><td><div class="flex items-center gap-3"><div class="w-9 h-9 rounded-lg bg-gradient-to-br from-[var(--accent)] to-[var(--gold)] flex items-center justify-center text-white text-sm font-bold flex-shrink-0">'+u.name.charAt(0).toUpperCase()+'</div><span class="font-semibold text-sm">'+u.name+'</span></div></td><td class="text-sm text-[var(--text-muted)]">'+u.email+'</td><td class="text-sm text-[var(--text-muted)]">'+u.phone+'</td><td><span class="px-2 py-1 rounded-full text-[10px] font-bold '+(roleColors[u.role]||'')+'">'+u.role.toUpperCase()+'</span></td><td class="text-sm font-bold">'+(u.orderCount||0)+'</td><td>'+(isSelf?'<span class="text-xs text-[var(--text-muted)]">You</span>':'<button class="admin-delete-user-btn w-8 h-8 rounded-lg bg-[var(--surface2)] border border-[var(--border)] flex items-center justify-center hover:border-[var(--danger)] hover:text-[var(--danger)] transition-all text-xs" data-uid="'+u.id+'"><i class="fas fa-trash"></i></button>')+'</td></tr>';
  }
  body.innerHTML = html;

  var delBtns = body.querySelectorAll('.admin-delete-user-btn');
  for (var i = 0; i < delBtns.length; i++) {
    delBtns[i].addEventListener('click', function(){
      var uid = parseInt(this.getAttribute('data-uid'));
      var user = null;
      for (var j = 0; j < state.users.length; j++) { if(state.users[j].id===uid){user=state.users[j];break;} }
      if (!user) return;
      document.getElementById('deleteConfirmText').textContent = 'Delete user "'+user.name+'"? This cannot be undone.';
      state.deleteCallback = function(){
        state.users = state.users.filter(function(u){return u.id!==uid;});
        // Also remove their orders
        state.orders = state.orders.filter(function(o){return o.userId!==uid;});
        saveState(); renderAdmin();
        showToast('User removed', 'error');
      };
      openModal('deleteConfirmModal');
    });
  }
}

/* =============================================
   ADMIN ITEM MANAGEMENT
============================================= */
function showAddItemModal() {
  document.getElementById('itemModalTitle').textContent = 'Add Menu Item';
  document.getElementById('editItemId').value = '';
  document.getElementById('itemForm').reset();
  document.getElementById('itemActive').checked = true;
  clearAllErrors('itemForm');
  openModal('itemModal');
}

function editItem(id) {
  var item = null;
  for (var i = 0; i < state.menu.length; i++) { if(state.menu[i].id===id){item=state.menu[i];break;} }
  if (!item) return;
  document.getElementById('itemModalTitle').textContent = 'Edit Menu Item';
  document.getElementById('editItemId').value = id;
  document.getElementById('itemName').value = item.name;
  document.getElementById('itemDesc').value = item.desc;
  document.getElementById('itemPrice').value = item.price;
  document.getElementById('itemCategory').value = item.category;
  document.getElementById('itemImage').value = item.image;
  document.getElementById('itemActive').checked = item.active;
  clearAllErrors('itemForm');
  openModal('itemModal');
}

function handleItemSubmit(e) {
  e.preventDefault();
  clearAllErrors('itemForm');
  var valid = true;
  var name = document.getElementById('itemName').value.trim();
  var desc = document.getElementById('itemDesc').value.trim();
  var price = parseFloat(document.getElementById('itemPrice').value);
  var category = document.getElementById('itemCategory').value;
  var image = document.getElementById('itemImage').value.trim() || 'https://picsum.photos/seed/'+Date.now()+'/400/300.jpg';
  var active = document.getElementById('itemActive').checked;
  var editId = document.getElementById('editItemId').value;

  if (name.length < 2) { showFieldError('itemName','itemNameErr'); valid = false; }
  if (desc.length < 5) { showFieldError('itemDesc','itemDescErr'); valid = false; }
  if (isNaN(price) || price <= 0) { showFieldError('itemPrice','itemPriceErr'); valid = false; }
  if (!valid) return false;

  if (editId) {
    for (var i = 0; i < state.menu.length; i++) {
      if (state.menu[i].id === parseInt(editId)) {
        state.menu[i].name = name; state.menu[i].desc = desc; state.menu[i].price = price;
        state.menu[i].category = category; state.menu[i].image = image; state.menu[i].active = active;
        break;
      }
    }
    showToast('Item updated successfully', 'success');
  } else {
    state.menu.push({id:state.nextItemId++, name:name, desc:desc, price:price, category:category, image:image, active:active, rating:4.5, orders:0});
    showToast('Item added to menu', 'success');
  }
  saveState(); closeModal('itemModal'); renderAdmin(); refreshFoodCards();
  return false;
}

function toggleItemActive(id) {
  for (var i = 0; i < state.menu.length; i++) {
    if (state.menu[i].id === id) { state.menu[i].active = !state.menu[i].active; break; }
  }
  saveState(); renderAdmin(); refreshFoodCards();
  showToast('Item status toggled', 'info');
}

/* =============================================
   ADMIN ADD USER
============================================= */
function handleAddUser(e) {
  e.preventDefault();
  clearAllErrors('addUserForm');
  var valid = true;
  var name = document.getElementById('auName').value.trim();
  var email = document.getElementById('auEmail').value.trim();
  var phone = document.getElementById('auPhone').value.trim();
  var password = document.getElementById('auPassword').value;
  var role = document.getElementById('auRole').value;

  document.getElementById('auEmailErr').textContent = 'Please enter a valid email';

  if (!isValidName(name)) { showFieldError('auName','auNameErr'); valid = false; }
  if (!isValidEmail(email)) { showFieldError('auEmail','auEmailErr'); valid = false; }
  if (!isValidPhone(phone)) { showFieldError('auPhone','auPhoneErr'); valid = false; }
  if (!isValidPassword(password)) { showFieldError('auPassword','auPasswordErr'); valid = false; }
  if (!valid) return false;

  // Check duplicate
  var dup = false;
  for (var i = 0; i < state.users.length; i++) {
    if (state.users[i].email.toLowerCase() === email.toLowerCase()) { dup = true; break; }
  }
  if (dup) {
    document.getElementById('auEmailErr').textContent = 'This email is already registered';
    document.getElementById('auEmailErr').classList.add('show');
    document.getElementById('auEmail').classList.add('error');
    return false;
  }

  state.users.push({
    id: state.nextUserId++, name:name, email:email, password:password,
    phone:phone, role:role, orderCount:0,
    joined: new Date().toISOString().split('T')[0]
  });
  saveState(); closeModal('addUserModal'); renderAdmin();
  showToast('User "'+name+'" added successfully', 'success');
  document.getElementById('addUserForm').reset();
  return false;
}

/* =============================================
   PARTICLES
============================================= */
function createParticles() {
  var container = document.getElementById('particles');
  var colors = ['var(--accent)','var(--gold)','var(--success)'];
  for (var i = 0; i < 15; i++) {
    var p = document.createElement('div');
    p.className = 'particle';
    var size = Math.random()*4+2;
    p.style.cssText = 'width:'+size+'px;height:'+size+'px;left:'+(Math.random()*100)+'%;background:'+colors[Math.floor(Math.random()*colors.length)]+';opacity:'+(Math.random()*0.3+0.1)+';animation-duration:'+(Math.random()*15+10)+'s;animation-delay:'+(Math.random()*10)+'s;';
    container.appendChild(p);
  }
}

/* =============================================
   3D EFFECTS
============================================= */
function init3DEffects() {
  document.addEventListener('mousemove', function(e) {
    var x = (e.clientX / window.innerWidth - 0.5) * 2;
    var y = (e.clientY / window.innerHeight - 0.5) * 2;
    var inners = document.querySelectorAll('.scene-wrap .scene-inner');
    for (var i = 0; i < inners.length; i++) {
      inners[i].style.transform = 'rotateY('+(x*5)+'deg) rotateX('+(-y*5)+'deg)';
    }
  });
}

/* =============================================
   NAVBAR SCROLL
============================================= */
function initNavbar() {
  window.addEventListener('scroll', function() {
    var nav = document.getElementById('navbar');
    if (window.scrollY > 50) {
      nav.style.background = 'rgba(10,10,10,0.85)';
      nav.style.backdropFilter = 'blur(20px)';
      nav.style.borderBottom = '1px solid var(--border)';
    } else {
      nav.style.background = 'transparent';
      nav.style.backdropFilter = 'none';
      nav.style.borderBottom = 'none';
    }
  });
}

/* =============================================
   CARD NUMBER FORMATTING
============================================= */
document.addEventListener('input', function(e) {
  if (e.target.id === 'cardNumber') {
    var val = e.target.value.replace(/\D/g,'').substring(0,16);
    e.target.value = val.replace(/(.{4})/g,'$1 ').trim();
  }
  if (e.target.id === 'cardExpiry') {
    var val = e.target.value.replace(/\D/g,'').substring(0,4);
    if (val.length >= 3) val = val.substring(0,2)+'/'+val.substring(2);
    e.target.value = val;
  }
});

/* =============================================
   BIND ALL EVENT LISTENERS
============================================= */
function bindAllEvents() {
  // Logo
  document.getElementById('logoBtn').addEventListener('dblclick', function(){
    if (confirm('Reset all data to defaults?')) { localStorage.removeItem('foodverse_db'); location.reload(); }
  });
  document.getElementById('logoBtn').addEventListener('click', function(){ navigate('home'); });

  // Nav links
  bindNavLinks();

  // Hero buttons
  document.getElementById('heroMenuBtn').addEventListener('click', function(){ navigate('menu'); });
  document.getElementById('heroStoryBtn').addEventListener('click', function(){
    document.getElementById('about-section').scrollIntoView({behavior:'smooth'});
  });
  document.getElementById('viewAllMenuBtn').addEventListener('click', function(){ navigate('menu'); });

  // Cart
  document.getElementById('cartBtn').addEventListener('click', function(){ toggleCart(true); });
  document.getElementById('closeCartBtn').addEventListener('click', function(){ toggleCart(false); });
  document.getElementById('cartOverlay').addEventListener('click', function(){ toggleCart(false); });
  document.getElementById('checkoutBtn').addEventListener('click', function(){ toggleCart(false); navigate('checkout'); });

  // Checkout
  document.getElementById('backToMenuBtn').addEventListener('click', function(){ navigate('menu'); });
  document.getElementById('placeOrderBtn').addEventListener('click', function(){ placeOrder(); });

  // Payment methods
  var payBtns = document.querySelectorAll('#paymentMethods .radio-card');
  for (var i = 0; i < payBtns.length; i++) {
    payBtns[i].addEventListener('click', function(){ selectPayment(this.getAttribute('data-method')); });
  }

  // Orders page
  document.getElementById('backFromOrdersBtn').addEventListener('click', function(){ navigate('home'); });

  // Admin page
  document.getElementById('adminBackBtn').addEventListener('click', function(){ navigate('home'); });
  document.getElementById('addItemBtn').addEventListener('click', function(){ showAddItemModal(); });
  var adminTabs = document.querySelectorAll('#adminTabs .tab-btn');
  for (var i = 0; i < adminTabs.length; i++) {
    adminTabs[i].addEventListener('click', function(){ switchAdminTab(this.getAttribute('data-tab')); });
  }
  document.getElementById('addUserBtn').addEventListener('click', function(){
    document.getElementById('addUserForm').reset();
    clearAllErrors('addUserForm');
    openModal('addUserModal');
  });

  // Login/Register modal switches
  document.getElementById('goToRegister').addEventListener('click', function(){ closeModal('loginModal'); setTimeout(function(){ openModal('registerModal'); },200); });
  document.getElementById('goToLogin').addEventListener('click', function(){ closeModal('registerModal'); setTimeout(function(){ openModal('loginModal'); },200); });

  // Forms
  document.getElementById('loginForm').addEventListener('submit', handleLogin);
  document.getElementById('registerForm').addEventListener('submit', handleRegister);
  document.getElementById('itemForm').addEventListener('submit', handleItemSubmit);
  document.getElementById('addUserForm').addEventListener('submit', handleAddUser);

  // OTP
  document.getElementById('verifyOtpBtn').addEventListener('click', handleVerifyOtp);
  document.getElementById('resendOtpBtn').addEventListener('click', handleResendOtp);
  document.getElementById('cancelOtpBtn').addEventListener('click', handleCancelOtp);

  // OTP input auto-focus
  var otpInputs = document.querySelectorAll('#otpInputs .otp-input');
  for (var i = 0; i < otpInputs.length; i++) {
    (function(input, idx){
      input.addEventListener('input', function(e){
        this.classList.remove('error');
        document.getElementById('otpErr').classList.remove('show');
        if (this.value.length === 1 && idx < otpInputs.length - 1) {
          otpInputs[idx + 1].focus();
        }
      });
      input.addEventListener('keydown', function(e){
        if (e.key === 'Backspace' && !this.value && idx > 0) {
          otpInputs[idx - 1].focus();
        }
        if (e.key === 'Enter') { handleVerifyOtp(); }
      });
      input.addEventListener('paste', function(e){
        e.preventDefault();
        var data = (e.clipboardData || window.clipboardData).getData('text').replace(/\D/g,'').substring(0,6);
        for (var j = 0; j < data.length && j < otpInputs.length; j++) {
          otpInputs[j].value = data[j];
        }
        if (data.length > 0) otpInputs[Math.min(data.length, otpInputs.length)-1].focus();
      });
    })(otpInputs[i], i);
  }

  // Order notification
  document.getElementById('acceptOrderBtn').addEventListener('click', function(){ handleOrderDecision(true); });
  document.getElementById('declineOrderBtn').addEventListener('click', function(){ handleOrderDecision(false); });

  // Delete confirm
  document.getElementById('confirmDeleteBtn').addEventListener('click', function(){
    if (state.deleteCallback) { state.deleteCallback(); state.deleteCallback = null; }
    closeModal('deleteConfirmModal');
  });

  // Close modal buttons
  var closeBtns = document.querySelectorAll('.close-modal-btn');
  for (var i = 0; i < closeBtns.length; i++) {
    closeBtns[i].addEventListener('click', function(){
      var modalId = this.getAttribute('data-modal');
      if (modalId) closeModal(modalId);
    });
  }

  // Click overlay to close modals
  var overlays = document.querySelectorAll('.modal-overlay');
  for (var i = 0; i < overlays.length; i++) {
    (function(overlay){
      overlay.addEventListener('click', function(e){
        if (e.target === overlay) { overlay.classList.remove('active'); var anyOpen = document.querySelector('.modal-overlay.active'); if(!anyOpen) document.body.style.overflow=''; }
      });
    })(overlays[i]);
  }

  // ESC key
  document.addEventListener('keydown', function(e){
    if (e.key === 'Escape') {
      var modals = document.querySelectorAll('.modal-overlay.active');
      for (var i = modals.length - 1; i >= 0; i--) modals[i].classList.remove('active');
      document.body.style.overflow = '';
      toggleCart(false);
    }
  });

  // Toggle password visibility
  var pwBtns = document.querySelectorAll('.toggle-pw-btn');
  for (var i = 0; i < pwBtns.length; i++) {
    pwBtns[i].addEventListener('click', function(){
      var targetId = this.getAttribute('data-target');
      var input = document.getElementById(targetId);
      var icon = this.querySelector('i');
      if (input.type === 'password') { input.type = 'text'; icon.classList.replace('fa-eye','fa-eye-slash'); }
      else { input.type = 'password'; icon.classList.replace('fa-eye-slash','fa-eye'); }
    });
  }

  // Clear input error on focus
  var allInputs = document.querySelectorAll('.input-field');
  for (var i = 0; i < allInputs.length; i++) {
    allInputs[i].addEventListener('focus', function(){
      this.classList.remove('error');
      var errEl = this.parentElement.querySelector('.error-msg') || this.parentNode.querySelector('.error-msg');
      if (errEl) errEl.classList.remove('show');
    });
  }
}

/* =============================================
   INIT
============================================= */
function init() {
  loadState();
  createParticles();
  init3DEffects();
  initNavbar();
  renderHomeCategories();
  renderPopularGrid();
  updateAuthUI();
  updateCartUI();
  bindAllEvents();

  // Check pending for admin
  if (state.currentUser && state.currentUser.role === 'admin') {
    var pending = 0;
    for (var i = 0; i < state.orders.length; i++) { if(state.orders[i].status==='pending') pending++; }
    if (pending > 0) {
      setTimeout(function(){ showToast(pending + ' pending order(s) need your attention', 'new-order'); }, 1500);
    }
  }
}

init();
</script>
</body>
</html>