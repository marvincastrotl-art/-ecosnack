# -ecosnack
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ECOSNACK | Premium</title>

<style>
body {margin:0;font-family:'Segoe UI';background:#eef5ee;}

header {
    background:linear-gradient(135deg,#1b5e20,#81c784);
    color:white;text-align:center;padding:70px 20px;
}

nav {
    background:#1b5e20;padding:15px;text-align:center;
    position:sticky;top:0;
}

nav a {
    color:white;margin:15px;text-decoration:none;font-weight:bold;
}

.container {
    max-width:1200px;margin:auto;padding:20px;
}

.grid {
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.card {
    background:white;
    padding:25px;
    border-radius:15px;
    box-shadow:0 10px 25px rgba(0,0,0,0.1);
    transition:0.3s;
}

.card:hover {
    transform:scale(1.05);
}

h2 {color:#2e7d32;}

button {
    background:#2e7d32;color:white;
    border:none;padding:12px 25px;
    border-radius:10px;cursor:pointer;
}

button:hover {
    background:#1b5e20;
}

footer {
    background:#1b5e20;color:white;
    text-align:center;padding:20px;
}

/* Animaciones */
.fade {
    opacity:0;
    transform:translateY(30px);
    transition:1s;
}

.fade.show {
    opacity:1;
    transform:translateY(0);
}

/* Carrito */
#carrito {
    position:fixed;
    right:20px;
    bottom:20px;
    background:#2e7d32;
    color:white;
    padding:15px;
    border-radius:50px;
    cursor:pointer;
}
</style>

</head>

<body>

<header>
<h1>ECOSNACK</h1>
<p>Nutrición real que impulsa tu día</p>
<button onclick="agregar()">Comprar ahora</button>
</header>

<nav>
<a href="#nosotros">Nosotros</a>
<a href="#producto">Producto</a>
<a href="#beneficios">Beneficios</a>
<a href="#contacto">Contacto</a>
</nav>

<div class="container">

<section id="nosotros" class="fade">
<div class="card">
<h2>Sobre nosotros</h2>
<p>Empresa innovadora de snacks saludables con proteína sustentable de chapulín.</p>
</div>
</section>

<section id="producto" class="fade">
<div class="grid">
<div class="card">
<h2>Producto</h2>
<p>Galletas nutritivas con proteína, fibra y sin conservadores.</p>
</div>

<div class="card">
<h2>Precio</h2>
<p>$15 MXN por pieza</p>
</div>

<div class="card">
<h2>Calidad</h2>
<p>Ingredientes naturales y proceso artesanal.</p>
</div>
</div>
</section>

<section id="beneficios" class="fade">
<div class="card">
<h2>Beneficios</h2>
<ul>
<li>💪 Energía</li>
<li>🌱 Sustentable</li>
<li>🥗 Saludable</li>
<li>⚡ Práctico</li>
</ul>
</div>
</section>

<section id="contacto" class="fade">
<div class="card">
<h2>Contacto</h2>
<p>Email: ecosnack@gmail.com</p>
<p>Instagram: @ecosnack</p>
</div>
</section>

</div>

<div id="carrito" onclick="verCarrito()">🛒 0</div>

<footer>
<p>© 2026 ECOSNACK Premium</p>
</footer>

<script>
let contador = 0;

function agregar(){
    contador++;
    document.getElementById("carrito").innerHTML = "🛒 " + contador;
    alert("Producto agregado al carrito");
}

function verCarrito(){
    alert("Tienes " + contador + " productos");
}

// Animación scroll
const faders = document.querySelectorAll('.fade');

window.addEventListener('scroll', () => {
    faders.forEach(el => {
        const rect = el.getBoundingClientRect();
        if(rect.top < window.innerHeight - 50){
            el.classList.add('show');
        }
    });
});
</script>

</body>
</html>
