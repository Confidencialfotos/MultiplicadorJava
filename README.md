<!DOCTYPE html>
<html>
<head>
    <title>Multiplicador JavaScript</title>
</head>
<body>

    <h1>Multiplicador de Dois Números</h1>

    <label for="numero1">Primeiro Número:</label>
    <input type="number" id="numero1"><br><br>

    <label for="numero2">Segundo Número:</label>
    <input type="number" id="numero2"><br><br>

    <button onclick="multiplicar()">Multiplicar</button>

    <h3>Resultado: <span id="resultado"></span></h3>

    <script>
        function multiplicar() {
            // 1. Obter os valores dos campos de entrada
            // Usamos parseFloat para garantir que os valores sejam tratados como números (podendo incluir decimais)
            var num1 = parseFloat(document.getElementById('numero1').value);
            var num2 = parseFloat(document.getElementById('numero2').value);

            // 2. Verificar se os valores são números válidos
            if (isNaN(num1) || isNaN(num2)) {
                document.getElementById('resultado').textContent = 'Por favor, insira números válidos.';
                return; // Sai da função se não for um número
            }

            // 3. Realizar a multiplicação
            var resultadoMultiplicacao = num1 * num2;

            // 4. Exibir o resultado na página
            document.getElementById('resultado').textContent = resultadoMultiplicacao;
        }
    </script>

</body>
</html>
