<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gerador de Sensi FF</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #1e1e1e;
        color: #fff;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 20px;
    }
    h1 {
        color: #ffcc00;
    }
    select, button {
        margin: 10px;
        padding: 10px;
        font-size: 16px;
    }
    .resultado {
        margin-top: 20px;
        background: #333;
        padding: 15px;
        border-radius: 10px;
        width: 300px;
        text-align: left;
    }
</style>
</head>
<body>
<h1>Gerador de Sensi FF</h1>

<label>Escolha o celular:</label>
<select id="celular">
    <option>iPhone</option>
    <option>Samsung</option>
    <option>Xiaomi</option>
    <option>Motorola</option>
    <option>LG</option>
    <option>Outro</option>
</select>

<label>Tipo de Free Fire:</label>
<select id="tipoFF">
    <option>Normal</option>
    <option>Max</option>
</select>

<button onclick="gerarSensi()">Gerar Sensibilidade</button>

<div class="resultado" id="resultado">
    <p><strong>Geral:</strong> -</p>
    <p><strong>Ponto Vermelho:</strong> -</p>
    <p><strong>2x:</strong> -</p>
    <p><strong>4x:</strong> -</p>
    <p><strong>AWM:</strong> -</p>
    <p><strong>Olhadinha:</strong> -</p>
</div>

<script>
function gerarSensi() {
    const celular = document.getElementById('celular').value;
    const tipoFF = document.getElementById('tipoFF').value;

    // Gerando valores aleatórios ou baseados em celular/FF
    const sensiGeral = (Math.random() * (100 - 50) + 50).toFixed(1);
    const pontoVermelho = (Math.random() * (100 - 50) + 50).toFixed(1);
    const doisX = (Math.random() * (100 - 50) + 50).toFixed(1);
    const quatroX = (Math.random() * (100 - 50) + 50).toFixed(1);
    const awm = (Math.random() * (100 - 50) + 50).toFixed(1);
    const olhadinha = (Math.random() * (100 - 50) + 50).toFixed(1);

    document.getElementById('resultado').innerHTML = `
        <p><strong>Geral:</strong> ${sensiGeral}</p>
        <p><strong>Ponto Vermelho:</strong> ${pontoVermelho}</p>
        <p><strong>2x:</strong> ${doisX}</p>
        <p><strong>4x:</strong> ${quatroX}</p>
        <p><strong>AWM:</strong> ${awm}</p>
        <p><strong>Olhadinha:</strong> ${olhadinha}</p>
    `;
}
</script>
</body>
</html>
