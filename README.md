<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Barber Studio 25</title>
<style>
body{margin:0;font-family:Arial,Helvetica,sans-serif;background:#0b0b0f;color:white}
header{background:#111827;padding:40px;text-align:center}
.logo{font-size:36px;font-weight:bold;letter-spacing:3px}
.container{max-width:900px;margin:auto;padding:20px}
.card{background:#111827;padding:20px;border-radius:10px;margin-bottom:20px}
h2{margin-top:0}
.services{display:grid;grid-template-columns:1fr 1fr 1fr;gap:15px}
.service{background:#0f172a;padding:15px;border-radius:8px;text-align:center}
button{background:#1d4ed8;color:white;border:none;padding:10px 15px;border-radius:6px;cursor:pointer}
input,select{width:100%;padding:10px;margin-top:8px;margin-bottom:12px;border-radius:6px;border:none}
footer{text-align:center;padding:20px;background:#020617;margin-top:40px}
.whatsapp{display:inline-block;margin-top:10px}
</style>
</head>
<body>

<header>
<div class="logo">BARBER STUDIO 25</div>
<p>Estilo clásico y moderno</p>
</header>

<div class="container">

<div class="card">
<h2>Información</h2>
<p><b>Dirección:</b> Sanabria 1894, Monte Castro, CABA</p>
<p><b>Teléfono:</b> 1164091400</p>
<p><b>Barbero:</b> Nicolás Villalba</p>
<p><b>Horario:</b></p>
<p>Martes a Viernes: 9:00–13:00 / 15:00–20:00</p>
<p>Sábados: 10:00–18:00</p>
<p>Domingos y Lunes: Cerrado</p>
</div>

<div class="card">
<h2>Servicios</h2>
<div class="services">
<div class="service">
<h3>Corte</h3>
<p>$14.000</p>
<p>30 min</p>
</div>
<div class="service">
<h3>Corte + Barba</h3>
<p>$16.000</p>
<p>45 min</p>
</div>
<div class="service">
<h3>Barba</h3>
<p>$10.000</p>
<p>15 min</p>
</div>
</div>
</div>

<div class="card">
<h2>Reservar turno</h2>
<form id="reservaForm">
<label>Nombre</label>
<input type="text" required>

<label>Teléfono</label>
<input type="tel" required>

<label>Servicio</label>
<select id="servicio">
<option value="Corte de cabello">Corte de cabello</option>
<option value="Corte y barba">Corte y barba</option>
<option value="Barba">Barba</option>
</select>

<label>Fecha</label>
<input type="date" id="fecha" required>

<label>Hora</label>
<select id="hora">
<option>09:00</option>
<option>09:30</option>
<option>10:00</option>
<option>10:30</option>
<option>11:00</option>
<option>11:30</option>
<option>12:00</option>
<option>12:30</option>
<option>15:00</option>
<option>15:30</option>
<option>16:00</option>
<option>16:30</option>
<option>17:00</option>
<option>17:30</option>
<option>18:00</option>
<option>18:30</option>
<option>19:00</option>
<option>19:30</option>
</select>

<button type="submit">Reservar por WhatsApp</button>
</form>
</div>

</div>

<footer>
<p>Barber Studio 25</p>
<a class="whatsapp" href="https://wa.me/5491164091400" target="_blank">
<button>Escribir por WhatsApp</button>
</a>
</footer>

<script>
document.getElementById("reservaForm").addEventListener("submit",function(e){
e.preventDefault()

let nombre=this.querySelector("input[type=text]").value
let telefono=this.querySelector("input[type=tel]").value
let servicio=document.getElementById("servicio").value
let fecha=document.getElementById("fecha").value
let hora=document.getElementById("hora").value

let mensaje=`Hola! Quiero reservar turno:%0A
Nombre: ${nombre}%0A
Teléfono: ${telefono}%0A
Servicio: ${servicio}%0A
Fecha: ${fecha}%0A
Hora: ${hora}`

window.open(`https://wa.me/5491164091400?text=${mensaje}`,'_blank')
})
</script>

</body>
</html>
