---
layout: page
title: Contacto
permalink: /contacto/
---

# Acercate a nosotros (ﾉ◕ヮ◕)ﾉ*:･ﾟ✧

¡Estamos para ayudarte! Si tienes algún comentario, sugerencia o duda estaremos encantados de escucharte :)

<br>

<style>
  form {
    max-width: 600px;
    margin: auto;
  }

  input, textarea {
    width: 100%;
    padding: 10px;
    box-sizing: border-box;
  }

  button {
    padding: 10px 20px;
    background-color: #007acc;
    color: white;
    border: none;
    cursor: pointer;
  }

  button:hover {
    background-color: #005fa3;
  }
</style>

<form action="https://formspree.io/f/mqapwyoj" method="POST">
  <label for="name">Nombre:</label><br>
  <input type="text" id="name" name="name" required><br><br>

  <label for="email">Correo electrónico:</label><br>
  <input type="email" id="email" name="_replyto" required><br><br>

  <label for="subject">Asunto:</label><br>
  <input type="text" id="subject" name="subject" required><br><br>

  <label for="message">Mensaje:</label><br>
  <textarea id="message" name="message" rows="5" required></textarea><br><br>

  <button type="submit">Enviar</button>
</form>

