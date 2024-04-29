<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bem Vindo à Loja do Geração Eleita</title>
<style>
  body {
    font-family: 'Arial', sans-serif;
    background: url('caminho-para-sua-imagem-de-fundo.jpg') no-repeat center center fixed;
    background-size: cover;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: #FFF;
  }
  .container {
    background: rgba(0, 0, 0, 0.8);
    padding: 20px;
    border-radius: 8px;
    width: 340px;
  }
  .form-group {
    margin-bottom: 15px;
  }
  label {
    display: block;
    text-align: left;
  }
  select, input, button {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
  }
  h1 {
    text-align: center;
    color: #FFF;
  }
  button {
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
    margin-top: 20px;
  }
  button:hover {
    opacity: 0.8;
  }
  .checkbox-group {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .checkbox-group label {
    margin: 5px;
  }
</style>
</head>
<body>

<div class="container">
  <h1>Bem Vindo à Loja do Geração Eleita</h1>
  <form id="pedidoForm">
    <div class="form-group">
      <label for="nome">Seu Nome:</label>
      <input type="text" id="nome" name="nome" placeholder="Digite seu nome" required>
    </div>

    <div class="form-group">
      <label for="acai">Escolha o seu Açaí:</label>
      <img src="caminho-para-imagem-acai.jpg" alt="Açaí" class="item-image">
      <select id="acai" name="acai">
        <option value="Açaí 300ml - R$6,00">300ml - R$6,00</option>
        <option value="Açaí 500ml - R$10,00">500ml - R$10,00</option>
      </select>
    </div>

    <div class="form-group">
      <label>Adicionais:</label>
      <div class="checkbox-group">
        <label><input type="checkbox" name="adicionais" value="Leite em Pó"> Leite em Pó</label>
        <label><input type="checkbox" name="adicionais" value="Leite Condensado"> Leite Condensado</label>
        <label><input type="checkbox" name="adicionais" value="Paçoca"> Paçoca</label>
        <label><input type="checkbox" name="adicionais" value="Granola"> Granola</label>
        <label><input type="checkbox" name="adicionais" value="Amendoim"> Amendoim</label>
      </div>
    </div>

    <!-- Repetir a estrutura acima para coberturas e frutas -->

    <button type="button" onclick="enviarPedido()">Faça seu pedido</button>
  </form>
</div>

<script>
function enviarPedido() {
  var nome = document.getElementById('nome').value;
  var acai = document.getElementById('acai').value;
  var adicionaisElements = document.querySelectorAll('input[name="adicionais"]:checked');
  var adicionaisValues = Array.from(adicionaisElements).map(el => el.value);
  
  var mensagem = `Olá Geração Eleita, aqui está o meu pedido:
  Nome: ${nome}
  Açaí: ${acai}
  Adicionais: ${adicionaisValues.join(', ')}
  `;
  
  // Inclua aqui as variáveis e a lógica para as coberturas e frutas

  var numeroWhatsApp = "27997904763";
  window.open(`https://wa.me/55${numeroWhatsApp}?text=${encodeURIComponent(mensagem)}`, '_blank');
}
</script>

</body>
</html>

