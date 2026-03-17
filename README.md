<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TRIZZVIVET STORE</title>
<style>
/* --- GLOBAL --- */
* {margin:0; padding:0; box-sizing:border-box; font-family:Arial, Helvetica, sans-serif;}
body {background:white; color:#111;}

/* --- NAVBAR --- */
.navbar{display:flex; justify-content:space-between; align-items:center; padding:20px 40px; border-bottom:1px solid #eee; position:sticky; top:0; background:white; z-index:1000;}
.logo{font-size:24px; font-weight:800; letter-spacing:3px;}
.nav-links{display:flex; gap:25px; list-style:none; font-weight:600; cursor:pointer;}
.nav-links li:hover{opacity:.6;}

/* --- HERO --- */
.hero{height:80vh; background:url("https://images.unsplash.com/photo-1523381294911-8d3cead13475?q=80&w=1600") center/cover; display:flex; justify-content:center; align-items:center; text-align:center; color:white; padding:20px;}
.hero h1{font-size:60px; margin-bottom:10px;}
.hero button{margin-top:20px; padding:14px 28px; border:none; background:black; color:white; font-weight:bold; cursor:pointer; transition:.3s;}
.hero button:hover{background:#333;}

/* --- PRODUCTS --- */
.products{padding:80px 40px;}
.products h2{text-align:center; margin-bottom:40px;}
.grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:40px;}
.product{text-align:center; transition:.3s;}
.product:hover{transform:scale(1.05);}
.product img{width:100%; border-radius:8px;}
.product h3{margin:10px 0 5px 0;}
.product p{font-weight:bold; margin-bottom:10px;}
.product button{padding:12px 20px; background:black; color:white; border:none; cursor:pointer; transition:.3s;}
.product button:hover{background:#333;}

/* --- DESIGNER --- */
.designer{padding:80px 20px; background:#f5f5f5; text-align:center;}
.designer select{padding:10px; margin:10px;}
.designer button{padding:12px 20px; background:black; color:white; border:none; cursor:pointer;}
#designerPreview{margin-top:20px; display:flex; justify-content:center; gap:20px; flex-wrap:wrap;}
#designerPreview img{width:150px; border:2px solid #111; border-radius:6px;}

/* --- CART --- */
.cart-container{position:fixed; top:80px; right:20px; background:white; border:1px solid #ccc; padding:20px; width:300px; max-height:500px; overflow-y:auto; display:none; z-index:1001;}
.cart-container h3{text-align:center; margin-bottom:10px;}
.cart-item{display:flex; justify-content:space-between; margin-bottom:8px;}

/* --- INFO & FOOTER --- */
.info{padding:80px 20px; text-align:center;}
footer{padding:30px; text-align:center; border-top:1px solid #eee;}

/* --- MOBILE --- */
@media(max-width:768px){.hero h1{font-size:40px;}.nav-links{gap:15px;font-size:14px;}}
</style>
</head>
<body>

<!-- NAVBAR -->
<header class="navbar">
<div class="logo">TRIZZVIVET</div>
<ul class="nav-links">
<li onclick="scrollShop()">Shop</li>
<li onclick="scrollDesigner()">Designer</li>
<li onclick="toggleCart()">Cart (<span id="cartCount">0</span>)</li>
</ul>
</header>

<!-- HERO -->
<section class="hero">
<div>
<h1>TRIZZVIVET DROP</h1>
<p>Streetwear Digital Concepts</p>
<button onclick="scrollShop()">Shop Now</button>
</div>
</section>

<!-- PRODUCTS -->
<section class="products" id="shop">
<h2>Featured Concepts</h2>
<div class="grid">

<div class="product">
<img src="https://images.unsplash.com/photo-1520975922324-1d6db4b0d9d2">
<h3>Concept Tee</h3>
<p>$20</p>
<button onclick="addToCart('Concept Tee', 20)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1520974735194-7c6a1cbe0d03">
<h3>Concept Hoodie</h3>
<p>$30</p>
<button onclick="addToCart('Concept Hoodie', 30)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c">
