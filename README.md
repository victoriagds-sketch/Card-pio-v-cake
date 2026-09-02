<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>V-CAKE | Cardápio Confeitaria Artesanal</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #FFFDF9;
            color: #4A3B32;
            padding-bottom: 120px;
        }

        /* CABEÇALHO COM LOGO */
        header {
            background: linear-gradient(135deg, #FFF0F5 0%, #F5E6E8 100%);
            text-align: center;
            padding: 30px 20px 25px;
            border-bottom: 2px solid #E8D8CE;
        }

        .logo-img {
            width: 110px;
            height: 110px;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #FFF;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            margin-bottom: 10px;
        }

        header h1 {
            font-size: 2.4rem;
            color: #8B5E3C;
            letter-spacing: 2px;
        }

        header p {
            font-size: 1rem;
            color: #B5838D;
            margin-top: 3px;
            letter-spacing: 1px;
            font-weight: 500;
        }

        .insta-link {
            display: inline-block;
            margin-top: 12px;
            color: #8B5E3C;
            text-decoration: none;
            font-weight: bold;
            background: #FFF;
            padding: 6px 15px;
            border-radius: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            font-size: 0.9rem;
        }

        /* NAVEGAÇÃO / CATEGORIAS */
        .categories-nav {
            display: flex;
            overflow-x: auto;
            white-space: nowrap;
            background: #FFF;
            padding: 12px 15px;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            border-bottom: 1px solid #E8D8CE;
        }

        .categories-nav a {
            color: #8B5E3C;
            text-decoration: none;
            padding: 8px 16px;
            margin-right: 8px;
            border-radius: 20px;
            background-color: #F7EDE2;
            font-size: 0.9rem;
            font-weight: 600;
        }

        /* CONTEÚDO PRINCIPAL */
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 0 15px;
        }

        .category-section {
            margin-bottom: 35px;
        }

        .category-title {
            font-size: 1.2rem;
            color: #8B5E3C;
            background-color: #F7EDE2;
            padding: 10px 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 5px solid #D4A373;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* CARDS / LISTAS */
        .info-card {
            background: #FFF;
            border: 1px solid #E8D8CE;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 12px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
        }

        .info-card-title {
            font-weight: bold;
            color: #5C4033;
            font-size: 1rem;
            margin-bottom: 5px;
        }

        .info-card-desc {
            font-size: 0.9rem;
            color: #7D6B5D;
        }

        .rule-badge {
            background-color: #FFF0F5;
            color: #B5838D;
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 15px;
            border: 1px solid #F5E6E8;
            text-align: center;
        }

        /* ITEMS COM FOTOS */
        .menu-item {
            background: #FFF;
            border: 1px solid #E8D8CE;
            border-radius: 12px;
            padding: 12px 15px;
            margin-bottom: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 12px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
        }

        .item-info {
            flex: 1;
        }

        .item-name {
            font-weight: bold;
            font-size: 1rem;
            color: #5C4033;
        }

        .item-desc {
            font-size: 0.85rem;
            color: #7D6B5D;
            margin-top: 4px;
            font-style: italic;
        }

        .item-price {
            font-weight: bold;
            font-size: 1.05rem;
            color: #B5838D;
            white-space: nowrap;
            margin-top: 4px;
        }

        .item-img {
            width: 75px;
            height: 75px;
            object-fit: cover;
            border-radius: 10px;
            border: 1px solid #E8D8CE;
            flex-shrink: 0;
        }

        /* GRIDS DOS KITS */
        .kits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
        }

        .kit-card {
            background-color: #FFF8F0;
            border: 1px solid #E8D8CE;
            border-radius: 12px;
            padding: 15px;
        }

        .kit-header {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px solid #E8D8CE;
            padding-bottom: 8px;
            margin-bottom: 10px;
        }

        .kit-title {
            font-weight: bold;
            color: #8B5E3C;
            font-size: 1.1rem;
        }

        .kit-price {
            font-weight: bold;
            color: #B5838D;
            font-size: 1.1rem;
        }

        .kit-ul {
            padding-left: 20px;
            font-size: 0.9rem;
            color: #6B4E31;
        }

        /* RODAPÉ INFORMATIVO */
        footer {
            background-color: #7A4B4B;
            color: #FFF;
            text-align: center;
            padding: 20px 15px;
            font-size: 0.85rem;
            line-height: 1.6;
            margin-top: 30px;
            border-top-left-radius: 15px;
            border-top-right-radius: 15px;
        }

        /* BOTÃO FLUTUANTE PEDIDO */
        .btn-whatsapp {
            position: fixed;
            bottom: 15px;
            right: 20px;
            left: 20px;
            max-width: 400px;
            margin: 0 auto;
            background-color: #25D366;
            color: white;
            text-align: center;
            padding: 14px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.05rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            z-index: 1000;
        }
    </style>
</head>
<body>

    <header>
        <!-- FOTO DA LOGO DA V-CAKE -->
        <img src="logo.png" alt="V-CAKE Confeitaria" class="logo-img">
        <h1>V-CAKE</h1>
        <p>CONFEITARIA ARTESANAL</p>
        <a href="https://instagram.com/Vitoria_Cake24" target="_blank" class="insta-link">📸 @Vitoria_Cake24</a>
    </header>

    <div class="categories-nav">
        <a href="#massas">🍰 Massas</a>
        <a href="#recheios">🎂 Recheios</a>
        <a href="#docinhos">🍬 Docinhos</a>
        <a href="#bolos-kits">🎁 Bolos & Kits</a>
        <a href="#tortas">🥧 Tortas</a>
        <a href="#travessa">🍓 Travessas</a>
        <a href="#pudins">🍮 Pudins</a>
    </div>

    <div class="container">

        <!-- NOSSAS MASSAS -->
        <section id="massas" class="category-section">
            <div class="category-title">🍰 NOSSAS MASSAS</div>
            <div class="info-card">
                <div class="info-card-title">Massa Branca de Baunilha</div>
                <div class="info-card-desc">Fofinha e combina com tudo</div>
            </div>
            <div class="info-card">
                <div class="info-card-title">Massa de Chocolate 50% Cacau</div>
                <div class="info-card-desc">Úmida e intensa</div>
            </div>
        </section>

        <!-- RECHEIOS DE BOLO -->
        <section id="recheios" class="category-section">
            <div class="category-title">🎂 RECHEIOS DE BOLO</div>
            <div class="info-card"><div class="info-card-title">Leite Ninho com Morango <span style="font-size:0.8rem; color:#B5838D;">(mais pedido)</span></div></div>
            <div class="info-card"><div class="info-card-title">Brigadeiro Cremoso</div></div>
            <div class="info-card"><div class="info-card-title">Coco Cremoso</div></div>
            <div class="info-card"><div class="info-card-title">Ninho com Nutella <span style="font-size:0.8rem; color:#B5838D;">(premium)</span></div></div>
            <div class="info-card"><div class="info-card-title">Creme de Abacaxi</div></div>
            <div class="info-card"><div class="info-card-title">Creme de Paçoca</div></div>
            <div class="info-card"><div class="info-card-title">Doce de Leite com Ameixa</div></div>
            <div class="info-card"><div class="info-card-title">Brigadeiro de Maracujá</div></div>
            <div class="info-card"><div class="info-card-title">Ouro Branco</div></div>
        </section>

        <!-- DOCINHOS -->
        <section id="docinhos" class="category-section">
            <div class="category-title">🍬 DOCINHOS</div>
            <div class="rule-badge">REGRA: 25un = 1 sabor | 50un = 2 sabores | 100un = até 4 sabores</div>
            
            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">25 unidades</div>
                    <div class="item-price">R$ 45,00</div>
                </div>
                <img src="docinhos.jpg" alt="Docinhos" class="item-img">
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">50 unidades</div>
                    <div class="item-price">R$ 90,00</div>
                </div>
                <img src="docinhos.jpg" alt="Docinhos" class="item-img">
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">100 unidades</div>
                    <div class="item-price">R$ 170,00</div>
                </div>
                <img src="docinhos.jpg" alt="Docinhos" class="item-img">
            </div>

            <div class="info-card" style="margin-top: 10px;">
                <div class="info-card-title" style="font-size:0.9rem;">Sabores disponíveis:</div>
                <div class="info-card-desc">Brigadeiro, Coco, Leite Ninho, Ninho com Nutella, Bicho de Pé, Paçoca, Maracujá, Churros com amendoim.</div>
            </div>
        </section>

        <!-- BOLOS / KITS / SOBREMESAS -->
        <section id="bolos-kits" class="category-section">
            <div class="category-title">🎁 BOLOS / KITS / SOBREMESAS</div>
            
            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bolo por quilo</div>
                    <div class="item-price">R$ 75,00 / kg</div>
                </div>
                <img src="bolo-kilo.jpg" alt="Bolo por quilo" class="item-img">
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bento Cake 5cm</div>
                    <div class="item-desc">Na hamburgueira</div>
                    <div class="item-price">R$ 38,00</div>
                </div>
                <img src="bento-5cm.jpg" alt="Bento Cake 5cm" class="item-img">
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bolo no pote</div>
                    <div class="item-desc">Ninho/Morango, Brigadeiro, Coco</div>
                    <div class="item-price">R$ 12,00</div>
                </div>
                <img src="bolo-pote.jpg" alt="Bolo no Pote" class="item-img">
            </div>

            <div class="kits-grid" style="margin-top: 15px;">
                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">KIT 1</span><span class="kit-price">R$ 98,00</span></div>
                    <ul class="kit-ul">
                        <li>800g + 10 doces + 6 cupcakes</li>
                    </ul>
                </div>

                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">KIT 2</span><span class="kit-price">R$ 185,00</span></div>
                    <ul class="kit-ul">
                        <li>1,5kg + 25 doces + 12 cupcakes</li>
                    </ul>
                </div>

                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">KIT 3</span><span class="kit-price">R$ 225,00</span></div>
                    <ul class="kit-ul">
                        <li>2kg + 50 doces + 20 cupcakes</li>
                    </ul>
                </div>

                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">KIT 4</span><span class="kit-price">R$ 410,00</span></div>
                    <ul class="kit-ul">
                        <li>3kg + 100 doces + 24 cupcakes</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- TORTAS -->
        <section id="tortas" class="category-section">
            <div class="category-title">🥧 TORTAS</div>
            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Torta (Limão / Abacaxi / Banoffee)</div>
                    <div class="item-price">R$ 75,00</div>
                </div>
                <img src="torta.jpg" alt="Torta" class="item-img">
            </div>
        </section>

    </div>

    <!-- RODAPÉ DE INFORMAÇÕES -->
    <footer>
        <p>🕒 <strong>Atendimento:</strong> 7h às 19h | 📦 <strong>48h antecedência</strong></p>
        <p>📍 <strong>Retirada:</strong> Mansões das Águas Quentes - Caldas Novas</p>
    </footer>

    <!-- BOTÃO DE WHATSAPP -->
    <a href="https://wa.me/5564992147719?text=Olá!%20Gostaria%20de%20fazer%20um%20pedido%20na%20V-CAKE" target="_blank" class="btn-whatsapp">
        💬 Faça seu pedido no WhatsApp
    </a>

</body>
</html>
