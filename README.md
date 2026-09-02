<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>V-CAKE | Confeitaria Artesanal</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --rosa: #d98f9d;
      --rosa-claro: #f7dfe3;
      --rosa-muito-claro: #fff4f5;
      --creme: #fffaf6;
      --marrom: #654438;
      --marrom-escuro: #493027;
      --dourado: #b88a50;
      --branco: #ffffff;
      --sombra: 0 8px 30px rgba(101, 68, 56, 0.08);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "DM Sans", sans-serif;
      background: var(--creme);
      color: var(--marrom);
      line-height: 1.6;
    }

    /* =========================
       TOPO
    ========================== */

    header {
      width: 100%;
      background:
        radial-gradient(circle at top center, #fff 0%, #fff8f5 45%, #fcebed 100%);
      text-align: center;
      padding: 35px 20px 30px;
      border-bottom: 1px solid #f0d8d8;
    }

    .header-content {
      width: 100%;
      max-width: 1100px;
      margin: 0 auto;
    }

    .logo-img {
      width: 180px;
      height: 180px;
      object-fit: contain;
      display: block;
      margin: 0 auto 12px;
      filter: drop-shadow(0 8px 15px rgba(101, 68, 56, 0.12));
    }

    .brand-name {
      font-family: "Playfair Display", serif;
      font-size: clamp(2.2rem, 8vw, 4rem);
      color: var(--marrom-escuro);
      letter-spacing: 3px;
      line-height: 1;
      margin-bottom: 8px;
    }

    .brand-subtitle {
      font-size: 0.95rem;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--rosa);
      font-weight: 600;
    }

    .instagram {
      display: inline-block;
      margin-top: 15px;
      color: var(--marrom);
      text-decoration: none;
      font-weight: 600;
    }

    .instagram:hover {
      color: var(--rosa);
    }

    /* =========================
       DESTAQUE
    ========================== */

    .hero {
      width: 100%;
      background: var(--marrom-escuro);
      color: white;
      padding: 25px 20px;
    }

    .hero-content {
      max-width: 1100px;
      margin: auto;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .hero-text h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(1.5rem, 5vw, 2.2rem);
      margin-bottom: 5px;
    }

    .hero-text p {
      opacity: 0.9;
    }

    .hero-button {
      display: inline-block;
      background: var(--rosa);
      color: white;
      text-decoration: none;
      padding: 13px 22px;
      border-radius: 30px;
      font-weight: 700;
      transition: 0.3s;
      white-space: nowrap;
    }

    .hero-button:hover {
      transform: translateY(-2px);
      background: #c97f8d;
    }

    /* =========================
       NAVEGAÇÃO
    ========================== */

    nav {
      width: 100%;
      background: rgba(255, 255, 255, 0.96);
      border-bottom: 1px solid #eadbd7;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 3px 15px rgba(0, 0, 0, 0.04);
    }

    .nav-content {
      max-width: 1200px;
      margin: auto;
      padding: 10px 15px;
      display: flex;
      gap: 8px;
      overflow-x: auto;
      scrollbar-width: none;
    }

    .nav-content::-webkit-scrollbar {
      display: none;
    }

    nav a {
      flex: 0 0 auto;
      text-decoration: none;
      color: var(--marrom);
      background: var(--rosa-muito-claro);
      border: 1px solid #efd4d8;
      padding: 8px 14px;
      border-radius: 25px;
      font-size: 0.85rem;
      font-weight: 600;
      transition: 0.25s;
    }

    nav a:hover {
      background: var(--rosa);
      color: white;
    }

    /* =========================
       CONTEÚDO
    ========================== */

    main {
      width: 100%;
      padding: 30px 15px 50px;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
    }

    .section {
      background: white;
      border-radius: 22px;
      padding: 28px;
      margin-bottom: 25px;
      box-shadow: var(--sombra);
      border: 1px solid #f1e5e0;
      scroll-margin-top: 75px;
    }

    .section-title {
      display: flex;
      align-items: center;
      gap: 12px;
      font-family: "Playfair Display", serif;
      color: var(--marrom-escuro);
      font-size: clamp(1.6rem, 4vw, 2.2rem);
      margin-bottom: 22px;
    }

    .section-title::after {
      content: "";
      height: 1px;
      background: #ead3d0;
      flex: 1;
    }

    /* =========================
       MASSAS
    ========================== */

    .massas-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .info-card {
      background: var(--rosa-muito-claro);
      border-radius: 16px;
      padding: 22px;
      border: 1px solid #f1d8dc;
    }

    .info-card h3 {
      color: var(--marrom-escuro);
      margin-bottom: 7px;
      font-family: "Playfair Display", serif;
      font-size: 1.25rem;
    }

    .info-card p {
      font-size: 0.92rem;
      color: #755d53;
    }

    /* =========================
       RECHEIOS
    ========================== */

    .recheios-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }

    .recheio {
      position: relative;
      background: #fffaf9;
      border: 1px solid #eaded9;
      border-radius: 13px;
      padding: 15px;
      font-weight: 600;
    }

    .tag {
      display: inline-block;
      margin-left: 6px;
      padding: 3px 7px;
      border-radius: 10px;
      background: var(--rosa);
      color: white;
      font-size: 0.68rem;
      text-transform: uppercase;
      font-weight: 700;
    }

    .tag.gold {
      background: var(--dourado);
    }

    /* =========================
       DOCINHOS
    ========================== */

    .docinhos-precos {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
      margin-bottom: 22px;
    }

    .preco-card {
      text-align: center;
      background: var(--rosa-muito-claro);
      border: 1px solid #efd8dc;
      border-radius: 16px;
      padding: 20px 12px;
    }

    .preco-card strong {
      display: block;
      font-family: "Playfair Display", serif;
      font-size: 1.45rem;
      color: var(--marrom-escuro);
    }

    .preco {
      display: block;
      color: var(--rosa);
      font-size: 1.35rem;
      font-weight: 800;
      margin-top: 5px;
    }

    .sabores {
      background: #fffaf8;
      border-radius: 15px;
      padding: 20px;
    }

    .sabores strong {
      display: block;
      margin-bottom: 12px;
    }

    .sabores-lista {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .sabor {
      padding: 7px 12px;
      border-radius: 20px;
      background: white;
      border: 1px solid #ead8d4;
      font-size: 0.88rem;
    }

    /* =========================
       PRODUTOS
    ========================== */

    .produtos-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 16px;
    }

    .produto {
      background: #fffaf8;
      border: 1px solid #eaded9;
      border-radius: 17px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      min-height: 160px;
    }

    .produto h3 {
      font-family: "Playfair Display", serif;
      color: var(--marrom-escuro);
      font-size: 1.2rem;
      margin-bottom: 5px;
    }

    .produto p {
      color: #79635a;
      font-size: 0.88rem;
      flex: 1;
    }

    .produto-preco {
      color: var(--rosa);
      font-weight: 800;
      font-size: 1.25rem;
      margin-top: 12px;
    }

    /* =========================
       KITS
    ========================== */

    .kits-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .kit {
      background: linear-gradient(145deg, #fff8f7, #fff);
      border: 1px solid #ecd8d5;
      border-radius: 18px;
      padding: 20px;
      position: relative;
    }

    .kit-number {
      color: var(--rosa);
      font-weight: 800;
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .kit h3 {
      font-family: "Playfair Display", serif;
      font-size: 1.35rem;
      margin: 5px 0 12px;
      color: var(--marrom-escuro);
    }

    .kit p {
      font-size: 0.9rem;
      color: #735e55;
    }

    .kit-price {
      display: block;
      margin-top: 15px;
      font-size: 1.4rem;
      font-weight: 800;
      color: var(--rosa);
    }

    /* =========================
       RODAPÉ
    ========================== */

    footer {
      width: 100%;
      background: var(--marrom-escuro);
      color: white;
      padding: 35px 20px;
      text-align: center;
    }

    .footer-content {
      max-width: 900px;
      margin: auto;
    }

    footer h2 {
      font-family: "Playfair Display", serif;
      font-size: 1.8rem;
      margin-bottom: 8px;
    }

    footer p {
      opacity: 0.85;
      margin: 4px 0;
    }

    .footer-instagram {
      display: inline-block;
      color: #f7dfe3;
      text-decoration: none;
      margin-top: 12px;
      font-weight: 700;
    }

    /* =========================
       WHATSAPP
    ========================== */

    .whatsapp {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 200;
      background: #25d366;
      color: white;
      width: 58px;
      height: 58px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      font-size: 25px;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
      transition: 0.3s;
    }

    .whatsapp:hover {
      transform: scale(1.08);
    }

    /* =========================
       RESPONSIVO
    ========================== */

    @media (max-width: 900px) {

      .produtos-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .kits-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .recheios-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 600px) {

      header {
        padding: 28px 15px 25px;
      }

      .logo-img {
        width: 170px;
        height: 170px;
      }

      .hero-content {
        flex-direction: column;
        text-align: center;
      }

      .hero-button {
        width: 100%;
        max-width: 300px;
      }

      main {
        padding: 18px 10px 35px;
      }

      .section {
        padding: 20px 15px;
        border-radius: 18px;
      }

      .massas-grid,
      .recheios-grid,
      .docinhos-precos,
      .produtos-grid,
      .kits-grid {
        grid-template-columns: 1fr;
      }

      .section-title {
        font-size: 1.65rem;
      }

      .produto {
        min-height: auto;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       CABEÇALHO
  ========================== -->

  <header>
    <div class="header-content">

      <img
        src="logo.png.JPG"
        alt="Logo V-CAKE Confeitaria Artesanal"
        class="logo-img"
      >

      <h1 class="brand-name">V-CAKE</h1>

      <p class="brand-subtitle">
        Confeitaria Artesanal
      </p>

      <a
        href="https://instagram.com/Vitoria_Cake24"
        target="_blank"
        rel="noopener noreferrer"
        class="instagram"
      >
        @Vitoria_Cake24
      </a>

    </div>
  </header>


  <!-- =========================
       DESTAQUE
  ========================== -->

  <section class="hero">

    <div class="hero-content">

      <div class="hero-text">
        <h2>Feito com carinho para adoçar seus momentos ♥</h2>
        <p>Encomendas com no mínimo 48h de antecedência.</p>
      </div>

      <a
        href="https://wa.me/5564992147719?text=Ol%C3%A1!%20Gostaria%20de%20fazer%20um%20pedido%20na%20V-CAKE."
        class="hero-button"
      >
        Fazer pedido
      </a>

    </div>

  </section>


  <!-- =========================
       MENU
  ========================== -->

  <nav>
    <div class="nav-content">

      <a href="#massas">Massas</a>
      <a href="#recheios">Recheios</a>
      <a href="#docinhos">Docinhos</a>
      <a href="#bolos">Bolos</a>
      <a href="#kits">Kits</a>
      <a href="#tortas">Tortas</a>
      <a href="#travessas">Travessas</a>
      <a href="#pudins">Pudins</a>

    </div>
  </nav>


  <!-- =========================
       CONTEÚDO
  ========================== -->

  <main>

    <div class="container">


      <!-- MASSAS -->

      <section class="section" id="massas">

        <h2 class="section-title">Massas</h2>

        <div class="massas-grid">

          <div class="info-card">
            <h3>Massa Branca de Baunilha</h3>
            <p>
              Fofinha, leve e perfeita para combinar com diversos recheios.
            </p>
          </div>

          <div class="info-card">
            <h3>Massa de Chocolate</h3>
            <p>
              Feita com 50% cacau, úmida e com sabor intenso de chocolate.
            </p>
          </div>

        </div>

      </section>


      <!-- RECHEIOS -->

      <section class="section" id="recheios">

        <h2 class="section-title">Recheios</h2>

        <div class="recheios-grid">

          <div class="recheio">
            Leite Ninho com Morango
            <span class="tag">Mais pedido</span>
          </div>

          <div class="recheio">Brigadeiro Cremoso</div>

          <div class="recheio">Coco Cremoso</div>

          <div class="recheio">
            Ninho com Nutella
            <span class="tag gold">Premium</span>
          </div>

          <div class="recheio">Creme de Abacaxi</div>

          <div class="recheio">Creme de Paçoca</div>

          <div class="recheio">Doce de Leite com Ameixa</div>

          <div class="recheio">Brigadeiro de Maracujá</div>

          <div class="recheio">Ouro Branco</div>

        </div>

      </section>


      <!-- DOCINHOS -->

      <section class="section" id="docinhos">

        <h2 class="section-title">Docinhos</h2>

        <div class="docinhos-precos">

          <div class="preco-card">
            <strong>25 unidades</strong>
            <small>1 sabor</small>
            <span class="preco">R$ 45,00</span>
          </div>

          <div class="preco-card">
            <strong>50 unidades</strong>
            <small>Até 2 sabores</small>
            <span class="preco">R$ 90,00</span>
          </div>

          <div class="preco-card">
            <strong>100 unidades</strong>
            <small>Até 4 sabores</small>
            <span class="preco">R$ 170,00</span>
          </div>

        </div>

        <div class="sabores">

          <strong>Sabores disponíveis:</strong>

          <div class="sabores-lista">

            <span class="sabor">Brigadeiro</span>
            <span class="sabor">Coco</span>
            <span class="sabor">Leite Ninho</span>
            <span class="sabor">Ninho com Nutella</span>
            <span class="sabor">Bicho de Pé</span>
            <span class="sabor">Paçoca</span>
            <span class="sabor">Maracujá</span>
            <span class="sabor">Churros com Amendoim</span>

          </div>

        </div>

      </section>


      <!-- BOLOS -->

      <section class="section" id="bolos">

        <h2 class="section-title">Bolos & Sobremesas</h2>

        <div class="produtos-grid">

          <div class="produto">
            <h3>Bolo por quilo</h3>
            <p>Bolos personalizados conforme sua escolha.</p>
            <span class="produto-preco">R$ 75,00 / kg</span>
          </div>

          <div class="produto">
            <h3>Bento Cake 5cm</h3>
            <p>Uma opção pequena e delicada para presentear.</p>
            <span class="produto-preco">R$ 38,00</span>
          </div>

          <div class="produto">
            <h3>Bento Cake 10cm</h3>
            <p>Aproximadamente 800g.</p>
            <span class="produto-preco">R$ 55,00</span>
          </div>

          <div class="produto">
            <h3>Bolo no Pote</h3>
            <p>Ninho com Morango, Brigadeiro ou Coco.</p>
            <span class="produto-preco">R$ 12,00</span>
          </div>

        </div>

      </section>


      <!-- KITS -->

      <section class="section" id="kits">

        <h2 class="section-title">Kits</h2>

        <div class="kits-grid">

          <div class="kit">
            <span class="kit-number">Kit 01</span>
            <h3>Kit Festa</h3>
            <p>
              800g de bolo<br>
              10 docinhos<br>
              6 cupcakes
            </p>
            <span class="kit-price">R$ 98,00</span>
          </div>

          <div class="kit">
            <span class="kit-number">Kit 02</span>
            <h3>Kit Festa</h3>
            <p>
              1,5kg de bolo<br>
              25 docinhos<br>
              12 cupcakes
            </p>
            <span class="kit-price">R$ 185,00</span>
          </div>

          <div class="kit">
            <span class="kit-number">Kit 03</span>
            <h3>Kit Festa</h3>
            <p>
              2kg de bolo<br>
              50 docinhos<br>
              20 cupcakes
            </p>
            <span class="kit-price">R$ 225,00</span>
          </div>

          <div class="kit">
            <span class="kit-number">Kit 04</span>
            <h3>Kit Festa</h3>
            <p>
              3kg de bolo<br>
              100 docinhos<br>
              24 cupcakes
            </p>
            <span class="kit-price">R$ 410,00</span>
          </div>

        </div>

      </section>


      <!-- TORTAS -->

      <section class="section" id="tortas">

        <h2 class="section-title">Tortas</h2>

        <div class="produtos-grid">

          <div class="produto">
            <h3>Torta de Limão</h3>
            <span class="produto-preco">R$ 75,00</span>
          </div>

          <div class="produto">
            <h3>Torta de Abacaxi</h3>
            <span class="produto-preco">R$ 75,00</span>
          </div>

          <div class="produto">
            <h3>Banoffee</h3>
            <span class="produto-preco">R$ 75,00</span>
          </div>

        </div>

      </section>


      <!-- TRAVESSAS -->

      <section class="section" id="travessas">

        <h2 class="section-title">Sobremesas na Travessa</h2>

        <div class="produtos-grid">

          <div class="produto">
            <h3>Travessa Pequena</h3>
            <p>Bombom de morango, bombom de uva ou mousse trufado.</p>
            <span class="produto-preco">R$ 70,00</span>
          </div>

          <div class="produto">
            <h3>Travessa Grande</h3>
            <p>Bombom de morango, bombom de uva ou mousse trufado.</p>
            <span class="produto-preco">R$ 130,00</span>
          </div>

        </div>

      </section>


      <!-- PUDINS -->

      <section class="section" id="pudins">

        <h2 class="section-title">Pudins & Individuais</h2>

        <div class="produtos-grid">

          <div class="produto">
            <h3>Pudim Grande</h3>
            <p>Tradicional, maracujá ou ameixa.</p>
            <span class="produto-preco">R$ 65,00</span>
          </div>

          <div class="produto">
            <h3>Mini Pudim</h3>
            <p>Perfeito para uma sobremesa individual.</p>
            <span class="produto-preco">R$ 8,00</span>
          </div>

          <div class="produto">
            <h3>Mini Mousse</h3>
            <p>Delicioso e cremoso.</p>
            <span class="produto-preco">R$ 8,00</span>
          </div>

        </div>

      </section>

    </div>

  </main>


  <!-- =========================
       RODAPÉ
  ========================== -->

  <footer>

    <div class="footer-content">

      <h2>V-CAKE</h2>

      <p>Confeitaria Artesanal</p>

      <p>📍 Mansões das Águas Quentes – Caldas Novas</p>

      <p>🕐 Atendimento: 07h às 19h</p>

      <p>📦 Encomendas com 48h de antecedência</p>

      <a
        href="https://instagram.com/Vitoria_Cake24"
        target="_blank"
        rel="noopener noreferrer"
        class="footer-instagram"
      >
        @Vitoria_Cake24
      </a>

    </div>

  </footer>


  <!-- WHATSAPP -->

  <a
    class="whatsapp"
    href="https://wa.me/5564992147719?text=Ol%C3%A1!%20Gostaria%20de%20fazer%20um%20pedido%20na%20V-CAKE."
    aria-label="Fazer pedido pelo WhatsApp"
    title="Fazer pedido pelo WhatsApp"
  >
    ☎
  </a>

</body>
</html>
