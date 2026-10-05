# marat
Тема раст, вам понравится! 
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rasta Vibes</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Segoe UI', sans-serif;
    background: #0d0d0d;
    color: #f0f0f0;
    line-height: 1.7;
  }

  header {
    background: linear-gradient(135deg, #e63946, #f4c430, #2a9d3f, #0d0d0d);
    background-size: 400% 400%;
    animation: flow 12s ease infinite;
    border-bottom: 4px solid #eec474;
  }

  @keyframes flow {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  .header-inner {
    background: rgba(13, 13, 13, 0.88);
    backdrop-filter: blur(12px);
    padding: 24px 32px;
    display: flex;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .logo {
    font-size: 28px;
    font-weight: 800;
    background: linear-gradient(90deg, #e63946, #f4c430, #2a9d3f);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .logo span {
    display: block;
    font-size: 11px;
    font-weight: 400;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #a0a0a0;
    -webkit-text-fill-color: #a0a0a0;
    margin-top: 2px;
  }

  nav {
    margin-left: auto;
    display: flex;
    gap: 28px;
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: 1.5px;
  }

  nav a {
    color: #a0a0a0;
    text-decoration: none;
    position: relative;
    padding-bottom: 4px;
    transition: color 0.3s;
  }

  nav a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background: linear-gradient(90deg, #e63946, #f4c430, #2a9d3f);
    transition: width 0.3s;
  }

  nav a:hover { color: #f4c430; }
  nav a:hover::after { width: 100%; }

  .hero {
    padding: 100px 32px 80px;
    text-align: center;
    background:
      radial-gradient(ellipse at 20% 50%, rgba(230, 57, 70, 0.15) 0%, transparent 50%),
      radial-gradient(ellipse at 80% 50%, rgba(42, 157, 63, 0.15) 0%, transparent 50%),
      radial-gradient(ellipse at 50% 80%, rgba(244, 196, 48, 0.1) 0%, transparent 50%);
  }

  .hero h1 {
    font-size: clamp(2.8rem, 8vw, 5.5rem);
    font-weight: 900;
    line-height: 1.05;
    letter-spacing: -2px;
    margin-bottom: 20px;
    background: linear-gradient(135deg, #e63946 0%, #f4c430 50%, #2a9d3f 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero p {
    font-size: 1.1rem;
    color: #a0a0a0;
    max-width: 600px;
    margin: 0 auto 36px;
  }

  .hero a {
    display: inline-block;
    padding: 16px 40px;
    background: linear-gradient(135deg, #e63946, #f4c430, #2a9d3f);
    background-size: 200% 200%;
    animation: flow 6s ease infinite;
    color: #0d0d0d;
    font-weight: 700;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: 13px;
    border-radius: 50px;
    transition: transform 0.3s, box-shadow 0.3s;
  }

  .hero a:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 30px rgba(244, 196, 48, 0.35);
  }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 24px 80px;
  }

  section { margin-bottom: 64px; }

  section h2 {
    font-size: 1.8rem;
    font-weight: 700;
    margin-bottom: 28px;
    position: relative;
    padding-left: 20px;
  }

  section h2::before {
    content: '';
    position: absolute;
    left: 0;
    top: 6px;
    bottom: 6px;
    width: 5px;
    border-radius: 3px;
    background: linear-gradient(180deg, #e63946, #f4c430, #2a9d3f);
  }

  .cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 24px;
  }

  .card {
    background: #1e1e1e;
    border-radius: 18px;
    padding: 32px 28px;
    border: 1px solid rgba(255, 255, 255, 0.06);
    transition: transform 0.35s, border-color 0.35s, box-shadow 0.35s;
    position: relative;
    overflow: hidden;
  }

  .card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, #e63946, #f4c430, #2a9d3f);
    opacity: 0;
    transition: opacity 0.35s;
  }

  .card:hover {
    transform: translateY(-6px);
    border-color: rgba(244, 196, 48, 0.3);
    box-shadow: 0 16px 40px rgba(0, 0, 0, 0.5);
  }

  .card:hover::before { opacity: 1; }

  .card-icon {
    font-size: 2.2rem;
    margin-bottom: 16px;
    display: block;
  }

  .card h3 {
    font-size: 1.15rem;
    font-weight: 700;
    margin-bottom: 10px;
    color: #eec474;
  }

  .card p {
    font-size: 0.92rem;
    color: #a0a0a0;
  }

  .facts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
  }

  .fact {
    text-align: center;
    padding: 28px 16px;
    background: rgba(255, 255, 255, 0.03);
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.05);
  }

  .fact-number {
    font-size: 2.4rem;
    font-weight: 800;
    background: linear-gradient(135deg, #f4c430, #eec474);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .fact-label {
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: #a0a0a0;
    margin-top: 6px;
  }

  footer {
    border-top: 1px solid rgba(255, 255, 255, 0.06);
    padding: 40px 32px;
    text-align: center;
    font-size: 0.82rem;
    color: #a0a0a0;
    background: rgba(0, 0, 0, 0.3);
  }

  .footer-colors {
    display: flex;
    justify-content: center;
    gap: 8px;
    margin-bottom: 20px;
  }

  .footer-colors span {
    width: 32px;
    height: 6px;
    border-radius: 3px;
  }

  .footer-colors span:nth-child(1) { background: #e63946; }
  .footer-colors span:nth-child(2) { background: #f4c430; }
  .footer-colors span:nth-child(3) { background: #2a9d3f; }
  .footer-colors span:nth-child(4) { background: #0d0d0d; border: 1px solid rgba(255,255,255,0.15); }

  footer a { color: #eec474; text-decoration: none; }
  footer a:hover { text-decoration: underline; }

  @media (max-width: 720px) {
    .header-inner { padding: 18px 20px; }
    nav { margin-left: 0; width: 100%; gap: 20px; font-size: 12px; }
    .hero { padding: 70px 20px 60px; }
    .container { padding: 0 16px 60px; }
    section h2 { font-size: 1.5rem; }
  }
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <div class="logo">
      Rasta Vibes
      <span>Культура · Музыка · Свобода</span>
    </div>
    <nav>
      <a href="#culture">Культура</a>
      <a href="#music">Музыка</a>
      <a href="#style">Стиль</a>
      <a href="#facts">Факты</a>
    </nav>
  </div>
</header>

<section class="hero">
  <h1>Ощути ритм Расты</h1>
  <p>Красный, жёлтый, зелёный — цвета силы, мудрости и надежды.</p>
  <a href="#culture">Узнать больше</a>
</section>

<div class="container">

  <section id="culture">
    <h2>Культура Растафари</h2>
    <div class="cards">
      <div class="card">
        <span class="card-icon">🦁</span>
        <h3>Лев Иудейский</h3>
        <p>Символ силы, сопротивления и божественного присутствия.</p>
      </div>
      <div class="card">
        <span class="card-icon">🎶</span>
        <h3>Регги как голос</h3>
        <p>Музыка единства, мира и справедливости для всего мира.</p>
      </div>
      <div class="card">
        <span class="card-icon">🌿</span>
        <h3>Символы и смыслы</h3>
        <p>Дреды, цвета флага и образ жизни — идентичность свободы.</p>
      </div>
    </div>
  </section>

  <section id="music">
    <h2>Музыка и ритм</h2>
    <div class="cards">
      <div class="card">
        <span class="card-icon">🎤</span>
        <h3>Классика регги</h3>
        <p>Тяжёлый бас, размеренный ритм и тексты о свободе.</p>
      </div>
      <div class="card">
        <span class="card-icon">🌍</span>
        <h3>Глобальное влияние</h3>
        <p>Фестивали по всему миру собирают тысячи людей.</p>
      </div>
      <div class="card">
        <span class="card-icon">💚</span>
        <h3>Послание единства</h3>
        <p>Музыка объединяет людей независимо от происхождения.</p>
      </div>
    </div>
  </section>

  <section id="style">
    <h2>Стиль и эстетика</h2>
    <div class="cards">
      <div class="card">
        <span class="card-icon">🔴🟡🟢</span>
        <h3>Цветовая палитра</h3>
        <p>Красный, жёлтый, зелёный и чёрный — основа стиля.</p>
      </div>
      <div class="card">
        <span class="card-icon">🎨</span>
        <h3>Визуальный язык</h3>
        <p>Смелые цвета, фактуры и узнаваемые символы.</p>
      </div>
      <div class="card">
        <span class="card-icon">✨</span>
        <h3>Современный взгляд</h3>
        <p>Градиенты, стекло и яркие акценты в дизайне.</p>
      </div>
    </div>
  </section>

  <section id="facts">
    <h2>Раста в цифрах</h2>
    <div class="facts">
      <div class="fact">
        <div class="fact-number">4</div>
        <div class="fact-label">Ключевых цвета</div>
      </div>
      <div class="fact">
        <div class="fact-number">1930</div>
        <div class="fact-label">Год основания</div>
      </div>
      <div class="fact">
        <div class="fact-number">∞</div>
        <div class="fact-label">Влияние на музыку</div>
      </div>
    </div>
  </section>

</div>

<footer>
  <div class="footer-colors">
    <span></span><span></span><span></span><span></span>
  </div>
  <p>Rasta Vibes — культура, музыка, стиль.</p>
  <p style="margin-top: 8px;">
    <a href="#">О проекте</a> · <a href="#">Контакты</a>
  </p>
</footer>

</body>
</html>
