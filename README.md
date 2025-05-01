<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Formulário de Preferência</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      padding: 20px;
    }

    .form-container {
      background-color: white;
      padding: 20px;
      max-width: 400px;
      margin: 0 auto;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    h2 {
      text-align: center;
      color: #333;
    }

    label {
      display: block;
      margin: 15px 0 5px;
      font-weight: bold;
    }

    input[type="text"],
    input[type="number"] {
      width: 100%;
      padding: 8px;
      box-sizing: border-box;
    }

    .radio-group {
      margin-top: 5px;
    }

    .radio-group label {
      font-weight: normal;
      margin-right: 10px;
    }

    button {
      margin-top: 20px;
      width: 100%;
      padding: 10px;
      background-color: #3498db;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background-color: #2980b9;
    }
  </style>
</head>
<body>

  <div class="form-container">
    <h2>🍽️ Suas Preferências</h2>
    <form id="form-preferencias" onsubmit="mostrarResposta(event)">
      <label for="comida">Qual é sua comida favorita?</label>
      <input type="text" id="comida" name="comida" required>

      <label for="idade">Qual é sua idade?</label>
      <input type="number" id="idade" name="idade" required>

      <label>Qual é seu sexo?</label>
      <div class="radio-group">
        <label><input type="radio" name="sexo" value="Masculino" required> Masculino</label>
        <label><input type="radio" name="sexo" value="Feminino"> Feminino</label>
      </div>

      <button type="submit">Enviar</button>
    </form>
  </div>

  <script>
    function mostrarResposta(event) {
      event.preventDefault();
      const comida = document.getElementById('comida').value;
      const idade = document.getElementById('idade').value;
      const sexo = document.querySelector('input[name="sexo"]:checked').value;

      alert(`🍴 Comida favorita: ${comida}\n📅 Idade: ${idade}\n🧍 Sexo: ${sexo}`);
    }
  </script>

</body>
</html>
