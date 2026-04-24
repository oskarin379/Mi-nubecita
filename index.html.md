<!DOCTYPE html>  
<html lang="es">  
<head>  
<meta charset="UTF-8">  
<title>Para mi nubecita 🌷</title>  
  
<style>  
body {  
  margin: 0;  
  padding: 0;  
  background: #ffd6e0;  
  font-family: Arial, sans-serif;  
  text-align: center;  
  color: #6b1d2a;  
  overflow-x: hidden;  
}  
  
/* CORAZONES */  
.corazon {  
  position: fixed;  
  bottom: -10px;  
  color: #ff4d6d;  
  animation: subir 6s linear infinite;  
}  
  
@keyframes subir {  
  0% {transform: translateY(0); opacity: 1;}  
  100% {transform: translateY(-100vh); opacity: 0;}  
}  
  
/* ANIMACIONES */  
.anim {  
  opacity: 0;  
  transform: translateY(20px);  
  transition: all 1s ease;  
}  
  
.visible {  
  opacity: 1;  
  transform: translateY(0);  
}  
  
/* TEXTO FINAL */  
#final {  
  display: none;  
  font-size: 22px;  
  margin-top: 30px;  
}  
  
/* CIERRE */  
#cierre {  
  opacity: 0;  
  font-size: 26px;  
  margin-top: 25px;  
  font-weight: bold;  
  transition: opacity 2s ease;  
}  
  
.brillo {  
  text-shadow: 0 0 10px #ff4d6d, 0 0 20px #ff4d6d;  
}  
  
.container {  
  padding: 50px 20px;  
}  
  
h1 {  
  font-size: 36px;  
}  
  
.frase-principal {  
  font-size: 24px;  
  font-weight: bold;  
}  
  
p {  
  font-size: 20px;  
  margin: 15px;  
}  
  
.foto {  
  margin: 30px 0;  
}  
  
.foto img {  
  width: 280px;  
  border-radius: 15px;  
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);  
}  
  
.descripcion {  
  font-size: 18px;  
  opacity: 0.85;  
}  
  
button {  
  margin-top: 40px;  
  padding: 15px 30px;  
  border: none;  
  border-radius: 25px;  
  background: #ff4d6d;  
  color: white;  
  font-size: 20px;  
  cursor: pointer;  
}  
</style>  
</head>  
  
<body>  
  
<div class="container">  
  <h1 class="anim">Para “mi nubecita 🌷”</h1>  
  
  <div class="frase-principal anim">  
    Por esto y más te amo 💖  
  </div>  
  
  <p class="anim">Ojalá, amor, cada vez que te mires las manos</p>  
  <p class="anim">sientas que te faltan las mías.</p>  
  
  <div class="foto anim">  
    <img src="foto1.jpg.PNG">  
    <div class="descripcion">“La primera de nuestras tantas visitas &lt;3”</div>  
  </div>  
  
  <div class="foto anim">  
    <img src="foto2.jpg.HEIC">  
    <div class="descripcion">“Aquí veía a mi nubecita con sus nubecitas, estaban que me brillaban los ojos 🩷”</div>  
  </div>  
  
  <div class="foto anim">  
    <img src="foto3.jpg.jpg">  
    <div class="descripcion">“Este día nuestros cuerpos decidieron hablar antes que nuestra boca 😉”</div>  
  </div>  
  
  <button onclick="activar()">Toca aquí… 💌</button>  
  
  <div id="final">  
    Aun y con la distancia que hay en estos momentos,    
    te sigo sintiendo cerca de mi corazón… te amo 💖  
  </div>  
  
  <!-- CIERRE FINAL -->  
  <div id="cierre">Para siempre, tuyo… 💌</div>  
  
  <iframe id="yt"  
  width="0" height="0"  
  src=""  
  frameborder="0"  
  allow="autoplay">  
  </iframe>  
  
</div>  
  
<script>  
const elementos = document.querySelectorAll('.anim');  
  
window.onload = () => {  
  elementos.forEach((el, i) => {  
    setTimeout(() => {  
      el.classList.add('visible');  
    }, i * 800);  
  });  
};  
  
function activar() {  
  document.getElementById("final").style.display = "block";  
  
  document.getElementById("yt").src =  
  "https://www.youtube.com/embed/5e1zT7miep8?autoplay=1&loop=1&playlist=5e1zT7miep8";  
  
  setInterval(crearCorazon, 400);  
  
  // MOSTRAR CIERRE DESPUÉS  
  setTimeout(() => {  
    const cierre = document.getElementById("cierre");  
    cierre.style.opacity = "1";  
    cierre.classList.add("brillo");  
  }, 4000);  
}  
  
function crearCorazon() {  
  const corazon = document.createElement("div");  
  corazon.classList.add("corazon");  
  corazon.innerHTML = "💖";  
  corazon.style.left = Math.random() * 100 + "vw";  
  corazon.style.fontSize = (Math.random() * 20 + 10) + "px";  
  
  document.body.appendChild(corazon);  
  
  setTimeout(() => {  
    corazon.remove();  
  }, 6000);  
}  
</script>  
  
</body>  
</html>  
