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
            background-color: #FAF4F0;
            color: #5C4033;
            padding-bottom: 120px;
        }

        /* CABEÇALHO LADO A LADO DA TELA (100% LARGURA) */
        header {
            width: 100%;
            background-color: #FFFDF9;
            text-align: center;
            padding: 40px 20px 30px;
            border-bottom: 1px solid #EAD8D0;
        }

        .logo-img {
            width: 140px;
            height: 140px;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #F2C4CE;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            margin-bottom: 12px;
        }

        header h1 {
            font-size: 2.5rem;
            color: #8B5E3C;
            letter-spacing: 2px;
        }

        header p {
            font-size: 1rem;
            color: #C08A93;
            margin-top: 5px;
            letter-spacing: 1px;
            font-weight: 600;
        }

        .insta-link {
            display: inline-block;
            margin-top: 15px;
            color: #8B5E3C;
            text-decoration: none;
            font-weight: bold;
            background: #FFF;
            padding: 8px 20px;
            border-radius: 20px;
            border: 1px solid #EAD8D0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.03);
            font-size: 0.9rem;
        }

        /* NAVEGAÇÃO COMPLETA DE CANTO A CANTO */
        .categories-nav {
            width: 100%;
            display: flex;
            overflow-x: auto;
            white-space: nowrap;
            background: #FFF;
            padding: 12px 15px;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
            border-bottom: 1px solid #EAD8D0;
        }

        .categories-nav a {
            color: #8B5E3C;
            text-decoration: none;
            padding: 8px 16px;
            margin-right: 8px;
            border-radius: 18px;
            background-color: #F8EBEA;
            font-size: 0.9rem;
            font-weight: 600;
        }

        /* CONTEÚDO PRINCIPAL DO CARDÁPIO */
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 0 15px;
        }

        .category-section {
            background: #FFF;
            border-radius: 16px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.03);
            border: 1px solid #EAD8D0;
        }

        .category-title {
            font-size: 1.1rem;
            color: #FFF;
            background-color: #D896A1;
            padding: 10px 15px;
            border-radius: 10px;
            margin-bottom: 15px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .info-card {
            background: #FAF4F0;
            border-radius: 10px;
            padding: 12px 15px;
            margin-bottom: 10px;
        }

        .info-card-title {
            font-weight: bold;
            color: #5C4033;
            font-size: 0.95rem;
        }

        .info-card-desc {
            font-size: 0.85rem;
            color: #7D6B5D;
            margin-top: 3px;
        }

        .rule-badge {
            background-color: #FCEEF0;
            color: #C08A93;
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-bottom: 12px;
            text-align: center;
            border: 1px solid #F5D6DC;
        }

        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px dashed #EAD8D0;
            gap: 10px;
        }

        .menu-item:last-child {
            border-bottom: none;
        }

        .item-info {
            flex: 1;
        }

        .item-name {
            font-weight: 600;
            font-size: 0.95rem;
            color: #5C4033;
        }

        .item-desc {
            font-size: 0.8rem;
            color: #8C7A6B;
            margin-top: 2px;
        }

        .item-price {
            font-weight: bold;
            font-size: 0.95rem;
            color: #8B5E3C;
            white-space: nowrap;
        }

        footer {
            background-color: #8B5E3C;
            color: #FFF;
            text-align: center;
            padding: 20px 15px;
            font-size: 0.85rem;
            line-height: 1.6;
            margin-top: 30px;
            border-radius: 16px;
        }

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
            font-size: 1rem;
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
        <a href="#travessas">🍓 Travessas</a>
        <a href="#pudins">🍮 Pudins</a>
    </div>

    <div class="container">

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

        <section id="recheios" class="category-section">
            <div class="category-title">🎂 RECHEIOS DE BOLO</div>
            <div class="menu-item"><div class="item-name">Leite Ninho com Morango <span style="font-size:0.8rem; color:#C08A93;">(mais pedido)</span></div></div>
            <div class="menu-item"><div class="item-name">Brigadeiro Cremoso</div></div>
            <div class="menu-item"><div class="item-name">Coco Cremoso</div></div>
            <div class="menu-item"><div class="item-name">Ninho com Nutella <span style="font-size:0.8rem; color:#C08A93;">(premium)</span></div></div>
            <div class="menu-item"><div class="item-name">Creme de Abacaxi</div></div>
            <div class="menu-item"><div class="item-name">Creme de Paçoca</div></div>
            <div class="menu-item"><div class="item-name">Doce de Leite com Ameixa</div></div>
            <div class="menu-item"><div class="item-name">Brigadeiro de Maracujá</div></div>
            <div class="menu-item"><div class="item-name">Ouro Branco</div></div>
        </section>

        <section id="docinhos" class="category-section">
            <div class="category-title">🍬 DOCINHOS</div>
            <div class="rule-badge">REGRA: 25un = 1 sabor | 50un = 2 sabores | 100un = até 4 sabores</div>
            
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

            <div class="info-card" style="margin-top: 12px;">
                <div class="info-card-title" style="font-size:0.85rem; color:#C08A93;">Sabores disponíveis:</div>
                <div class="info-card-desc">Brigadeiro, Coco, Leite Ninho, Ninho com Nutella, Bicho de Pé, Paçoca, Maracujá, Churros com amendoim.</div>
            </div>
        </section>

        <section id="bolos-kits" class="category-section">
            <div class="category-title">🎁 BOLOS / KITS / SOBREMESAS</div>
            
            <div class="menu-item">
                <div class="item-info"><div class="item-name">Bolo por quilo</div></div>
                <div class="item-price">R$ 75,00 / kg</div>
            </div>

            <div class="menu-item">
                <div class="item-info"><div class="item-name">Bento Cake 5cm</div></div>
                <div class="item-price">R$ 38,00</div>
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bento Cake 10cm</div>
                    <div class="item-desc">Aproximadamente 800g</div>
                </div>
                <div class="item-price">R$ 55,00</div>
            </div>

            <div class="menu-item">
                <div class="item-info">
                    <div class="item-name">Bolo no pote</div>
                    <div class="item-desc">Ninho/Morango, Brigadeiro, Coco</div>
                </div>
                <div class="item-price">R$ 12,00</div>
            </div>

            <div style="margin-top: 15px;">
                <div class="menu-item">
                    <div class="item-info"><div class="item-name">KIT 1 — 800g + 10 doces + 6 cupcakes</div></div>
                    <div class="item-price">R$ 98,00</div>
                </div>
                <div class="menu-item">
                    <div class="item-info"><div class="item-name">KIT 2 — 1,5kg + 25 doces + 12 cupcakes</div></div>
                    <div class="item-price">R$ 185,00</div>
                </div>
                <div class="menu-item">
                    <div class="item-info"><div class="item-name">KIT 3 — 2kg + 50 doces + 20 cupcakes</div></div>
                    <div class="item-price">R$ 225,00</div>
                </div>
                <div class="menu-item">
                    <div class="item-info"><div class="item-name">KIT 4 — 3kg + 100 doces + 24 cupcakes</div></div>
                    <div class="item-price">R$ 410,00</div>
                </div>
            </div>
        </section>

        <section id="tortas" class="category-section">
            <div class="category-title">🥧 TORTAS</div>
            <div class="menu-item">
                <div class="item-info"><div class="item-name">Torta (Limão / Abacaxi / Banoffee)</div></div>
                <div class="item-price">R$ 75,00</div>
            </div>
        </section>

        <section id="travessas" class="category-section">
            <div class="category-title">🍓 SOBREMESAS NA TRAVESSA</div>
            
            <div class="menu-item">
                <div class="item-info"><div class="item-name">Travessa Pequena</div></div>
                <div class="item-price">R$ 70,00</div>
            </div>

            <div class="menu-item">
                <div class="item-info"><div class="item-name">Travessa Grande</div></div>
                <div class="item-price">R$ 130,00</div>
            </div>

            <div class="info-card" style="margin-top: 10px;">
                <div class="info-card-title" style="font-size:0.85rem; color:#C08A93;">Sabores disponíveis:</div>
                <div class="info-card-desc">Bombom de morango, Bombom de uva, Mousse trufado.</div>
            </div>
        </section>

        <section id="pudins" class="category-section">
            <div class="category-title">🍮 PUDINS & SOBREMESAS INDIVIDUAIS</div>
            
            <div class="menu-item">
                <div class="item-info"><div class="item-name">Pudim Grande (Tradicional / Maracujá / Ameixa)</div></div>
                <div class="item-price">R$ 65,00</div>
            </div>

            <div class="menu-item">
                <div class="item-info"><div class="item-name">Mini Pudim</div></div>
                <div class="item-price">R$ 8,00</div>
            </div>

            <div class="menu-item">
                <div class="item-info"><div class="item-name">Mini Mousse</div></div>
                <div class="item-price">R$ 8,00</div>
            </div>
        </section>

        <footer>
            <p>🕒 <strong>7h às 19h</strong> | 📦 <strong>48h antecedência</strong></p>
            <p>📍 <strong>Retirada:</strong> Mansões das Águas Quentes - Caldas Novas</p>
        </footer>

    </div>

    <a href="https://wa.me/5564992147719?text=Olá!%20Gostaria%20de%20fazer%20um%20pedido%20na%20V-CAKE" target="_blank" class="btn-whatsapp">
        💬 Faça seu pedido no WhatsApp
    </a>

</body>
</html>
