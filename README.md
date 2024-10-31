<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loja de Plantas</title>
    
    <!-- CSS incorporado diretamente no HTML -->
    <style>
        /* Reset básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
        }

        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1em;
        }

        #cart {
            position: absolute;
            top: 1em;
            right: 1em;
            background: white;
            color: #333;
            padding: 0.5em 1em;
            border-radius: 5px;
            font-weight: bold;
        }

        main {
            padding: 2em;
        }

        #product-list {
            display: flex;
            gap: 1em;
            flex-wrap: wrap;
            justify-content: center;
        }

        .product {
            background: white;
            padding: 1em;
            border: 1px solid #ddd;
            border-radius: 5px;
            width: 200px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .product img {
            width: 100%; /* Ocupa a largura total do contêiner */
            height: auto;
            border-radius: 5px;
            margin-bottom: 10px;
        }

        .product h2 {
            font-size: 1.5em;
            color: #333;
        }

        .product p {
            font-size: 1.2em;
            color: #666;
        }

        .product button {
            margin-top: 10px;
            padding: 0.5em 1em;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .product button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <header>
        <h1>Loja de Plantas</h1>
        <div id="cart">
            <p>Carrinho: <span id="cart-total">0</span>R$</p>
        </div>
    </header>
    <main>
        <section id="product-list">
            <div class="product">
                <img src="imagens/monstera.jpg" alt="Monstera Deliciosa">
                <h2>Monstera Deliciosa</h2>
                <p>Preço: 15R$</p>
                <button onclick="addToCart(15)">Adicionar ao Carrinho</button>
            </div>
            <div class="product">
                <img src="imagens/ficus.jpg" alt="Ficus Lyrata">
                <h2>Ficus Lyrata</h2>
                <p>Preço: 20R$</p>
                <button onclick="addToCart(20)">Adicionar ao Carrinho</button>
            </div>
            <div class="product">
                <img src="imagens/sao-jorge.jpg" alt="Espada de São Jorge">
                <h2>Espada de São Jorge</h2>
                <p>Preço: 10R$</p>
                <button onclick="addToCart(10)">Adicionar ao Carrinho</button>
            </div>
            <div class="product">
                <img src="imagens/cacto.jpg" alt="Cacto">
                <h2>Cacto</h2>
                <p>Preço: 8R$</p>
                <button onclick="addToCart(8)">Adicionar ao Carrinho</button>
            </div>
        </section>
    </main>
    
    <!-- JavaScript incorporado diretamente no HTML -->
    <script>
        // Inicializa o total do carrinho
        let cartTotal = 0;

        // Função para adicionar ao carrinho
        function addToCart(price) {
            cartTotal += price;
            document.getElementById("cart-total").innerText = cartTotal;
        }
    </script>
</body>
</html>
