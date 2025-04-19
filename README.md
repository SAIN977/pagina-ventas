#<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Curso Productividad Total</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f2f2f2;
      color: #333;
    }
    header {
      background: #4CAF50;
      color: white;
      padding: 40px 20px;
      text-align: center;
    }
    .container {
      max-width: 800px;
      margin: auto;
      padding: 20px;
      background: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 8px;
      margin-top: 30px;
    }
    h1, h2 {
      margin-top: 0;
    }
    .benefits {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .benefits div {
      background: #e8f5e9;
      padding: 10px;
      border-radius: 5px;
    }
    .price {
      text-align: center;
      margin: 30px 0;
    }
    .price span {
      font-size: 2em;
      color: #4CAF50;
    }
    .btn {
      display: inline-block;
      padding: 15px 30px;
      background: #4CAF50;
      color: white;
      text-decoration: none;
      font-weight: bold;
      border-radius: 5px;
    }
    .cta {
      text-align: center;
      margin-top: 40px;
    }
    .timer {
      text-align: center;
      font-size: 1.2em;
      margin-top: 20px;
      color: #d32f2f;
    }
    .testimonials {
      margin-top: 50px;
    }
    .testimonials h2 {
      text-align: center;
    }
    .testimonial {
      background: #f9f9f9;
      padding: 15px;
      margin: 10px 0;
      border-left: 4px solid #4CAF50;
      font-style: italic;
    }
  </style>
</head>
<body>

  <header>
    <h1>Curso Online: Productividad Total</h1>
    <p>Domina tu tiempo, cumple tus metas y mejora tu vida en 4 semanas</p>
  </header>

  <div class="container">
    <h2>¿Qué obtendrás?</h2>
    <div class="benefits">
      <div>✅ Técnicas comprobadas de gestión del tiempo</div>
      <div>✅ Plantillas listas para organizar tu día</div>
      <div>✅ Acceso de por vida al curso</div>
      <div>✅ Garantía de devolución de 7 días</div>
    </div>

    <div class="price">
      <p>Precio especial solo por hoy:</p>
      <span>$10.99</span>
      <br><br>
      <a href="https://www.paypal.com/buy?hosted_button_id=EXAMPLE" class="btn" target="_blank">Comprar ahora</a>
    </div>

    <div class="timer">
      ¡Oferta válida por tiempo limitado!<br>
      <span id="countdown"></span>
    </div>

    <div class="cta">
      <p>¡No esperes más para transformar tu rutina!</p>
    </div>

    <div class="testimonials">
      <h2>Lo que dicen nuestros alumnos</h2>
      <div class="testimonial">"Gracias a este curso, ahora soy mucho más eficiente y logro mis metas diarias sin estrés." – Ana R.</div>
      <div class="testimonial">"¡Increíble contenido! Me ayudó a estructurar mis días y a tener más tiempo libre." – Luis M.</div>
      <div class="testimonial">"Recomiendo este curso a todo el que quiera mejorar su productividad." – Carla D.</div>
    </div>
  </div>

  <script>
    // Cuenta regresiva 24h
    const countdownEl = document.getElementById('countdown');
    const targetDate = new Date();
    targetDate.setHours(targetDate.getHours() + 24);

    function updateCountdown() {
      const now = new Date();
      const diff = targetDate - now;
      const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((diff % (1000 * 60)) / 1000);

      if (diff > 0) {
        countdownEl.textContent = `${hours}h ${minutes}m ${seconds}s restantes`;
      } else {
        countdownEl.textContent = '¡La oferta ha terminado!';
      }
    }

    setInterval(updateCountdown, 1000);
  </script>

</body>
</html>

