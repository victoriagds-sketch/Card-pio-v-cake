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
            padding-bottom: 80px;
        }

        /* CABEÇALHO */
        header {
            background: linear-gradient(135deg, #FFF0F5 0%, #F5E6E8 100%);
            text-align: center;
            padding: 40px 20px 30px;
            border-bottom: 2px solid #E8D8CE;
        }

        header h1 {
            font-size: 2.8rem;
            color: #8B5E3C;
            letter-spacing: 3px;
        }

        header p {
            font-size: 1.1rem;
            color: #B5838D;
            margin-top: 5px;
            letter-spacing: 1px;
            font-weight: 500;
        }

        .insta-link {
            display: inline-block;
            margin-top: 15px;
            color: #8B5E3C;
            text-decoration: none;
            font-weight: bold;
            background: #FFF;
            padding: 6px 15px;
            border-radius: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
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
            transition: all 0.2s;
        }

        .categories-nav a:hover {
            background-color: #B5838D;
            color: #FFF;
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
            font-size: 1.3rem;
            color: #8B5E3C;
            background-color: #F7EDE2;
            padding: 10px 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 5px solid #D4A373;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* CARDS DOS PRODUTOS */
        .menu-item {
            background: #FFF;
            border: 1px solid #E8D8CE;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
        }

        .item-info {
            flex-grow: 1;
            padding-right: 15px;
        }

        .item-name {
            font-weight: bold;
            font-size: 1.05rem;
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
            font-size: 1.1rem;
            color: #B5838D;
            white-space: nowrap;
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
            border-radius: 10px;
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

        .kit-ul li {
            margin-bottom: 5px;
        }

        /* BOTÃO FLUTUANTE PEDIDO */
        .btn-whatsapp {
            position: fixed;
            bottom: 20px;
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
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
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
        <h1>V-CAKE</h1>
        <p>Confeitaria Artesanal</p>
        <a href="https://instagram.com/Vitoria_Cake24" target="_blank" class="insta-link">📸 @Vitoria_Cake24</a>
    </header>

    <div class="categories-nav">
        <a href="#bolos">🍰 Bolos</a>
        <a href="#cupcakes">🧁 Cupcakes</a>
        <a href="#docinhos">🍬 Docinhos</a>
        <a href="#kits">🎁 Kits</a>
        <a href="#tortas">🍰 Tortas</a>
        <a href="#travessa">🍓 Travessas</a>
        <a href="#pudins">🍮 Pudins</a>
        <a href="#individuais">🍫 Individuais</a>
    </div>

    <div class="container">

        <!-- BOLOS -->
        <section id="bolos" class="category-section">
            <div class="category-title">🍰 Bolos</div>
            
            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bolo por quilo</div>
                </div>
                <div class="item-price">R$ 75,00 / kg</div>
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bento Cake de 5 cm (na hamburgueira)</div>
                </div>
                <div class="item-price">R$ 38,00</div>
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bento Cake de 10 cm</div>
                    <div class="item-desc">Aproximadamente 800 g</div>
                </div>
                <div class="item-price">R$ 55,00</div>
            </div>
        </section>

        <!-- CUPCAKES -->
        <section id="cupcakes" class="category-section">
            <div class="category-title">🧁 Cupcakes</div>
            <div class="menu-item">
                <div class="item-info"><div class="item-name">6 unidades</div></div>
                <div class="item-price">R$ 45,00</div>
            </div>
            <div class="menu-item">
                <div class="item-info"><div class="item-name">12 unidades</div></div>
                <div class="item-price">R$ 90,00</div>
            </div>
        </section>

        <!-- DOCINHOS -->
        <section id="docinhos" class="category-section">
            <div class="category-title">🍬 Docinhos</div>
            <div class="menu-item">
                <div class="item-info"><div class="item-name">25 unidades</div></div>
                <div class="item-price">R$ 45,00</div>
            </div>
            <div class="menu-item">
                <div class="item-info"><div class="item-name">50 unidades</div></div>
                <div class="item-price">R$ 90,00</div>
            </div>
            <div class="menu-item">
                <div class="item-info"><div class="item-name">100 unidades</div></div>
                <div class="item-price">R$ 170,00</div>
            </div>
        </section>

        <!-- KITS -->
        <section id="kits" class="category-section">
            <div class="category-title">🎁 Kits Festa</div>
            <div class="kits-grid">
                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">Kit 1</span><span class="kit-price">R$ 98,00</span></div>
                    <ul class="kit-ul">
                        <li>Bolo de 10 cm (aprox. 800 g)</li>
                        <li>10 docinhos</li>
                        <li>6 cupcakes</li>
                    </ul>
                </div>
                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">Kit 2</span><span class="kit-price">R$ 185,00</span></div>
                    <ul class="kit-ul">
                        <li>Bolo de 1,5 kg</li>
                        <li>25 docinhos</li>
                        <li>12 cupcakes</li>
                    </ul>
                </div>
                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">Kit 3</span><span class="kit-price">R$ 225,00</span></div>
                    <ul class="kit-ul">
                        <li>Bolo de 2 kg</li>
                        <li>50 docinhos</li>
                        <li>20 cupcakes</li>
                    </ul>
                </div>
                <div class="kit-card">
                    <div class="kit-header"><span class="kit-title">Kit 4</span><span class="kit-price">R$ 410,00</span></div>
                    <ul class="kit-ul">
                        <li>Bolo de 3 kg</li>
                        <li>100 docinhos</li>
                        <li>24 cupcakes</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- TORTAS -->
        <section id="tortas" class="category-section">
            <div class="category-title">🍰 Tortas — R$ 75,00</div>
            <div class="menu-item"><div class="item-name">Torta de limão</div></div>
            <div class="menu-item"><div class="item-name">Torta de abacaxi</div></div>
            <div class="menu-item"><div class="item-name">Banoffee</div></div>
        </section>

        <!-- SOBREMESAS NA TRAVESSA -->
        <section id="travessa" class="category-section">
            <div class="category-title">🍓 Sobremesas na Travessa</div>
            <div class="kit-card" style="margin-bottom: 12px;">
                <div class="kit-header"><span class="kit-title">Travessa Pequena</span><span class="kit-price">R$ 70,00</span></div>
                <div class="item-desc" style="color: #5C4033;">Sabores disponíveis: Bombom de morango, Bombom de uva, Mousse trufado.</div>
            </div>
            <div class="kit-card">
                <div class="kit-header"><span class="kit-title">Travessa Grande</span><span class="kit-price">R$ 130,00</span></div>
                <div class="item-desc" style="color: #5C4033;">Sabores disponíveis: Bombom de morango, Bombom de uva, Mousse trufado.</div>
            </div>
        </section>

        <!-- PUDINS -->
        <section id="pudins" class="category-section">
            <div class="category-title">🍮 Pudins — R$ 65,00</div>
            <div class="menu-item"><div class="item-name">Pudim tradicional</div></div>
            <div class="menu-item"><div class="item-name">Pudim de maracujá</div></div>
            <div class="menu-item"><div class="item-name">Pudim com calda de ameixa</div></div>
        </section>

        <!-- INDIVIDUAIS -->
        <section id="individuais" class="category-section">
            <div class="category-title">🍫 Sobremesas Individuais</div>
            <div class="menu-item">
                <div class="item-name">Bolo no pote</div>
                <div class="item-price">R$ 12,00</div>
            </div>
            <div class="menu-item">
                <div class="item-name">Mini pudim</div>
                <div class="item-price">R$ 8,00</div>
            </div>
            <div class="menu-item">
                <div class="item-name">Mini mousse</div>
                <div class="item-price">R$ 8,00</div>
            </div>
        </section>

    </div>

    <!-- BOTÃO DE WHATSAPP -->
    <a href="https://wa.me/5564992147719?text=Olá!%20Gostaria%20de%20fazer%20um%20pedido%20na%20V-CAKE" target="_blank" class="btn-whatsapp">
        💬 Faça seu pedido no WhatsApp
    </a>

</body>
</html>
