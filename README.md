<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Как понять, что сайт теряет клиентов — Валерия Нестерова</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Manrope:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --black: #0f0f0f;
    --white: #fafaf8;
    --accent: #e8412a;
    --muted: #888880;
    --border: #e2e2de;
    --highlight-bg: #f5f4f0;
    --tool-bg: #f9f8f5;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--white);
    color: var(--black);
    font-family: 'Manrope', sans-serif;
    font-weight: 400;
    font-size: 17px;
    line-height: 1.75;
    -webkit-font-smoothing: antialiased;
  }

  /* HEADER */
  .header {
    max-width: 680px;
    margin: 0 auto;
    padding: 64px 24px 0;
  }

  .author-line {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 40px;
    font-size: 13px;
    font-weight: 500;
    color: var(--muted);
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  .author-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent);
    flex-shrink: 0;
  }

  .headline {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 5vw, 42px);
    font-weight: 700;
    line-height: 1.2;
    letter-spacing: -0.02em;
    color: var(--black);
    margin-bottom: 20px;
  }

  .subheadline {
    font-size: 15px;
    color: var(--muted);
    font-weight: 400;
    line-height: 1.6;
    border-left: 2px solid var(--accent);
    padding-left: 16px;
    margin-bottom: 48px;
  }

  .divider {
    height: 1px;
    background: var(--border);
    margin-bottom: 48px;
  }

  /* INTRO */
  .intro {
    max-width: 680px;
    margin: 0 auto;
    padding: 0 24px;
  }

  .intro p {
    margin-bottom: 18px;
    color: #2a2a28;
  }

  .intro-note {
    background: var(--highlight-bg);
    border-radius: 8px;
    padding: 20px 24px;
    margin: 32px 0;
    font-size: 15px;
    color: #444;
    line-height: 1.7;
  }

  .intro-note strong { color: var(--black); }

  /* SECTIONS */
  .content {
    max-width: 680px;
    margin: 0 auto;
    padding: 0 24px;
  }

  .section {
    margin: 56px 0;
  }

  .section-number {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 8px;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(20px, 3.5vw, 26px);
    font-weight: 700;
    line-height: 1.25;
    margin-bottom: 20px;
    color: var(--black);
  }

  .section p {
    margin-bottom: 16px;
    color: #2a2a28;
  }

  /* TOOL CARDS */
  .tool-card {
    background: var(--tool-bg);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px 22px;
    margin: 20px 0;
  }

  .tool-name {
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 0.04em;
    color: var(--black);
    margin-bottom: 6px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .tool-name a {
    color: var(--accent);
    text-decoration: none;
    font-family: 'Manrope', sans-serif;
    font-size: 13px;
    font-weight: 500;
  }

  .tool-name a:hover { text-decoration: underline; }

  .tool-desc {
    font-size: 15px;
    color: #555;
    line-height: 1.65;
    margin: 0;
  }

  /* EXAMPLE BLOCK */
  .example-block {
    border-left: 3px solid var(--accent);
    padding: 16px 20px;
    margin: 24px 0;
    background: #fff9f8;
    border-radius: 0 8px 8px 0;
  }

  .example-label {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 8px;
  }

  .example-block p {
    font-size: 15px;
    color: #333;
    line-height: 1.65;
    margin: 0;
    font-style: italic;
  }

  /* TIP */
  .tip {
    background: #f0f4ff;
    border-radius: 8px;
    padding: 18px 22px;
    margin: 20px 0;
    font-size: 15px;
    color: #2a2a4a;
    line-height: 1.65;
  }

  .tip strong { color: #1a1a3a; }

  /* SUMMARY */
  .summary-section {
    background: var(--black);
    border-radius: 16px;
    padding: 40px 36px;
    margin: 56px 0;
    color: var(--white);
  }

  .summary-section h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(20px, 3.5vw, 26px);
    font-weight: 700;
    margin-bottom: 20px;
    color: var(--white);
  }

  .summary-section p {
    color: #c8c8c4;
    margin-bottom: 14px;
    font-size: 15px;
    line-height: 1.7;
  }

  .summary-section .example-block {
    background: rgba(255,255,255,0.06);
    border-left-color: var(--accent);
    border-radius: 0 8px 8px 0;
  }

  .summary-section .example-block p {
    color: #ddd;
  }

  /* CTA */
  .cta-section {
    background: var(--highlight-bg);
    border-radius: 16px;
    padding: 40px 36px;
    margin: 40px 0 64px;
    text-align: center;
  }

  .cta-section h3 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 12px;
    color: var(--black);
  }

  .cta-section p {
    font-size: 15px;
    color: var(--muted);
    margin-bottom: 24px;
    line-height: 1.65;
  }

  .cta-btn {
    display: inline-block;
    background: var(--accent);
    color: #fff;
    text-decoration: none;
    padding: 14px 32px;
    border-radius: 50px;
    font-size: 15px;
    font-weight: 600;
    letter-spacing: 0.02em;
    transition: opacity 0.2s;
  }

  .cta-btn:hover { opacity: 0.88; }

  /* TOOLS OVERVIEW TABLE */
  .tools-table {
    width: 100%;
    border-collapse: collapse;
    margin: 24px 0;
    font-size: 14px;
  }

  .tools-table th {
    text-align: left;
    padding: 10px 14px;
    background: var(--black);
    color: var(--white);
    font-weight: 600;
    font-size: 12px;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .tools-table th:first-child { border-radius: 8px 0 0 0; }
  .tools-table th:last-child { border-radius: 0 8px 0 0; }

  .tools-table td {
    padding: 10px 14px;
    border-bottom: 1px solid var(--border);
    color: #333;
    vertical-align: top;
  }

  .tools-table tr:last-child td { border-bottom: none; }
  .tools-table tr:nth-child(even) td { background: var(--tool-bg); }

  .tools-table a {
    color: var(--accent);
    text-decoration: none;
    font-weight: 500;
  }

  .tools-table a:hover { text-decoration: underline; }

  /* FOOTER */
  .footer {
    max-width: 680px;
    margin: 0 auto;
    padding: 0 24px 64px;
    font-size: 13px;
    color: var(--muted);
    text-align: center;
  }

  /* MEME BLOCKS */
  .meme-block {
    margin: 32px 0;
    border-radius: 12px;
    overflow: hidden;
    background: var(--highlight-bg);
    border: 1px solid var(--border);
  }
  .meme-inner { padding: 28px 24px; text-align: center; }
  .meme-emoji { font-size: 48px; display: block; margin-bottom: 12px; line-height: 1; }
  .meme-text { font-family: 'Playfair Display', serif; font-size: clamp(16px, 3vw, 20px); font-weight: 700; color: var(--black); line-height: 1.35; margin-bottom: 8px; }
  .meme-caption { font-size: 13px; color: var(--muted); font-style: italic; }
  .meme-block.dark-meme { background: var(--black); border-color: #222; }
  .meme-block.dark-meme .meme-text { color: var(--white); }
  .meme-block.dark-meme .meme-caption { color: #888; }
  .meme-dialogue { padding: 24px; display: flex; flex-direction: column; gap: 12px; }
  .meme-bubble { max-width: 75%; padding: 12px 16px; border-radius: 16px; font-size: 15px; line-height: 1.5; }
  .meme-bubble.left { background: #fff; border: 1px solid var(--border); border-bottom-left-radius: 4px; align-self: flex-start; color: var(--black); }
  .meme-bubble.right { background: var(--accent); color: #fff; border-bottom-right-radius: 4px; align-self: flex-end; }
  .meme-bubble-label { font-size: 11px; font-weight: 700; letter-spacing: 0.08em; text-transform: uppercase; color: var(--muted); margin-bottom: 6px; }

  /* SOCIAL PROOF */
  .social-proof-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin: 20px 0 24px; }
  .sp-card { background: var(--black); border-radius: 10px; padding: 16px 12px; text-align: center; }
  .sp-number { font-family: 'Playfair Display', serif; font-size: 32px; font-weight: 700; color: var(--accent); line-height: 1; margin-bottom: 6px; }
  .sp-label { font-size: 12px; color: #aaa; line-height: 1.4; }
  .reviews-row { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin: 0 0 24px; }
  .review-card { background: var(--white); border: 1px solid var(--border); border-radius: 10px; padding: 16px; text-align: left; }
  .review-stars { color: #f59e0b; font-size: 13px; margin-bottom: 8px; }
  .review-text { font-size: 13px; color: #444; line-height: 1.6; font-style: italic; margin-bottom: 10px; }
  .review-author { font-size: 12px; color: var(--muted); font-weight: 500; }
  .cta-desc { font-size: 15px; color: var(--muted); margin-bottom: 24px; line-height: 1.65; }
  .cta-buttons { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }
  .cta-btn-outline { background: transparent !important; border: 2px solid var(--accent); color: var(--accent) !important; }
  .cta-btn-outline:hover { background: var(--accent) !important; color: #fff !important; }

  /* INSTAGRAM CARD */
  .ig-card { max-width: 632px; margin: 0 24px 48px; display: flex; align-items: center; justify-content: space-between; background: var(--white); border: 1px solid var(--border); border-radius: 16px; padding: 20px 24px; gap: 16px; }
  .ig-card-left { display: flex; align-items: center; gap: 14px; }
  .ig-avatar { width: 52px; height: 52px; border-radius: 50%; background: linear-gradient(135deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888); display: flex; align-items: center; justify-content: center; font-family: 'Playfair Display', serif; font-size: 22px; font-weight: 700; color: #fff; flex-shrink: 0; }
  .ig-handle { font-weight: 700; font-size: 15px; color: var(--black); margin-bottom: 2px; }
  .ig-name { font-size: 13px; color: var(--muted); margin-bottom: 2px; }
  .ig-bio { font-size: 12px; color: #aaa; }
  .ig-follow-btn { display: flex; align-items: center; gap: 7px; background: linear-gradient(135deg, #f09433, #e6683c, #dc2743, #cc2366); color: #fff; text-decoration: none; padding: 10px 18px; border-radius: 50px; font-size: 14px; font-weight: 600; white-space: nowrap; transition: opacity 0.2s; flex-shrink: 0; }
  .ig-follow-btn:hover { opacity: 0.88; }

  @media (max-width: 600px) {
    .summary-section, .cta-section { padding: 28px 24px; }
    .tools-table { font-size: 13px; }
    .tools-table th, .tools-table td { padding: 8px 10px; }
    .reviews-row { grid-template-columns: 1fr; }
    .ig-card { flex-direction: column; align-items: flex-start; }
    .cta-buttons { flex-direction: column; align-items: center; }
    .meme-bubble { max-width: 90%; }
  }
</style>
</head>
<body>

<div class="header">
  <div class="author-line">
    <span class="author-dot"></span>
    Валерия Нестерова · velary_design · 2025
  </div>

  <h1 class="headline">Как понять, что сайт теряет клиентов — даже если он «нормально работает»</h1>

  <p class="subheadline">Бесплатный экспресс-аудит за 40 минут. Без доступа к аналитике, без технических знаний. Все инструменты открываются в РФ.</p>

  <div class="divider"></div>
</div>

<div class="intro">
  <p>Большинство владельцев бизнеса считают, что у них нормальный сайт. Он загружается, выглядит аккуратно, контакты есть. Но «нормально работает» и «приносит клиентов» — это, к сожалению, разные вещи.</p>

  <p>Эта методичка для двух ситуаций: вы хотите проверить свой сайт самостоятельно — или вы дизайнер и хотите прийти к потенциальному клиенту с конкретными цифрами, а не с общими словами про «улучшить».</p>

  <div class="intro-note">
    <strong>Как пользоваться:</strong> Пройдитесь по каждому разделу, проверьте свой сайт по каждому инструменту и записывайте что нашли. В конце у вас будет готовый список проблем с объяснением, что они значат для бизнеса. Всё бесплатно.
  </div>

  <div class="meme-block">
    <div class="meme-dialogue">
      <div>
        <div class="meme-bubble-label">Владелец бизнеса</div>
        <div class="meme-bubble left">У нас нормальный сайт. Мы его делали в 2018 году, всё работает</div>
      </div>
      <div>
        <div class="meme-bubble-label" style="text-align:right;">PageSpeed Insights</div>
        <div class="meme-bubble right">Производительность: 11/100 🙂</div>
      </div>
    </div>
  </div>

</div>

<div class="content">

  <!-- SECTION 1 -->
  <div class="section">
    <div class="section-number">01 / скорость</div>
    <h2 class="section-title">Первое, что убивает конверсию</h2>

    <p>Если сайт грузится дольше 3 секунд, больше трети посетителей уходят, не увидев ни строчки текста. Не потому что им неинтересно — просто не дождались.</p>

    <div class="tool-card">
      <div class="tool-name">Google PageSpeed Insights <a href="https://pagespeed.web.dev" target="_blank">↗ pagespeed.web.dev</a></div>
      <p class="tool-desc">Вбейте адрес сайта и смотрите на оценку для мобильных. Ниже 50 — плохо. Ниже 30 — серьёзная проблема. PageSpeed покажет конкретные причины: тяжёлые изображения, лишние скрипты, слабый хостинг.</p>
    </div>

    <div class="tool-card">
      <div class="tool-name">GTmetrix <a href="https://gtmetrix.com" target="_blank">↗ gtmetrix.com</a></div>
      <p class="tool-desc">Более детальный отчёт. Главное здесь — waterfall-диаграмма: наглядно видно, какой именно элемент тормозит всё остальное. Удобно показывать клиенту — это не абстрактные «проблемы», а конкретная картинка.</p>
    </div>

    <div class="example-block">
      <div class="example-label">Как говорить с клиентом</div>
      <p>«Ваш сайт грузится 6,5 секунд на телефоне. Это выше нормы вдвое. При среднем трафике это примерно 40% посетителей, которые уходят до того, как увидели ваш оффер».</p>
    </div>
  </div>

  <!-- SECTION 2 -->
  <div class="section">
    <div class="section-number">02 / SEO</div>
    <h2 class="section-title">Виден ли сайт в поиске вообще</h2>

    <p>Самая быстрая проверка — зайдите в Google и введите: <strong>site:вашсайт.ru</strong></p>

    <p>Результаты покажут, сколько страниц проиндексировано. Если их значительно меньше, чем страниц на сайте — часть контента в поиске просто не существует.</p>

    <div class="tool-card">
      <div class="tool-name">Ahrefs Webmaster Tools <a href="https://ahrefs.com/webmaster-tools" target="_blank">↗ ahrefs.com/webmaster-tools</a></div>
      <p class="tool-desc">Бесплатно после регистрации. Покажет битые страницы, ошибки noindex, каноникал, и главное — по каким запросам сайт вообще появляется в поиске и на каких позициях. Это отличный аргумент: «Ваши конкуренты видны по 40 запросам, ваш сайт — по трём».</p>
    </div>

    <div class="tool-card">
      <div class="tool-name">Яндекс.Вебмастер <a href="https://webmaster.yandex.ru" target="_blank">↗ webmaster.yandex.ru</a></div>
      <p class="tool-desc">Если сайт работает на РФ-аудиторию — проверяйте обязательно. Google и Яндекс индексируют по-разному, и бывает, что в одном поисковике всё хорошо, а в другом — полный провал.</p>
    </div>

    <div class="tool-card">
      <div class="tool-name">PR-CY <a href="https://pr-cy.ru" target="_blank">↗ pr-cy.ru</a></div>
      <p class="tool-desc">Российский сервис, комплексный экспресс-аудит на русском языке: доступность для поисковиков, заголовки H1, метатеги, структура страниц, скорость. Удобен тем, что всё сразу в одном месте.</p>
    </div>

    <div class="meme-block dark-meme">
      <div class="meme-inner">
        <span class="meme-emoji">🔍</span>
        <div class="meme-text">«Наш сайт точно в Google есть»</div>
        <div class="meme-caption">site:вашсайт.ru — найдено: 0 результатов</div>
      </div>
    </div>
  </div>

  <!-- SECTION 3 -->
  <div class="section">
    <div class="section-number">03 / конкуренты</div>
    <h2 class="section-title">Откуда у них трафик — и как это использовать</h2>

    <p>Это то, о чём редко говорят в обычных аудитах — а зря. Анализ конкурентов превращает разговор о редизайне из «хорошо бы обновить» в «вот почему вы теряете клиентов прямо сейчас».</p>

    <div class="tool-card">
      <div class="tool-name">SimilarWeb <a href="https://similarweb.com" target="_blank">↗ similarweb.com</a></div>
      <p class="tool-desc">Введите домен конкурента. Бесплатная версия покажет примерный трафик, откуда он приходит (поиск, соцсети, реклама, прямые заходы) и топ ключевых слов. Если у конкурента 60% трафика из органики, а у вашего клиента — 5% — это конкретный разговор про SEO.</p>
    </div>

    <div class="example-block">
      <div class="example-label">Как использовать дизайнеру</div>
      <p>Показывать не просто «ваш сайт медленный», а «вот что делают конкуренты и почему они обгоняют вас в поиске». Это другой уровень доверия к специалисту.</p>
    </div>
  </div>

  <!-- SECTION 4 -->
  <div class="section">
    <div class="section-number">04 / технические ошибки</div>
    <h2 class="section-title">Что видно снаружи без доступа к коду</h2>

    <div class="tool-card">
      <div class="tool-name">W3C Validator <a href="https://validator.w3.org" target="_blank">↗ validator.w3.org</a></div>
      <p class="tool-desc">Проверяет корректность кода. Критические ошибки означают, что в каких-то браузерах или на каких-то устройствах сайт может отображаться неправильно.</p>
    </div>

    <div class="tool-card">
      <div class="tool-name">SSL Labs Test <a href="https://ssllabs.com/ssltest" target="_blank">↗ ssllabs.com/ssltest</a></div>
      <p class="tool-desc">Проверяет SSL-сертификат. Если оценка ниже B или сертификат просрочен — браузер показывает посетителям предупреждение «этот сайт небезопасен». Значительная часть людей закрывает страницу сразу, не читая дальше.</p>
    </div>

    <div class="tool-card">
      <div class="tool-name">Screaming Frog SEO Spider <a href="https://screamingfrog.co.uk/seo-spider" target="_blank">↗ screamingfrog.co.uk</a></div>
      <p class="tool-desc">Бесплатно до 500 страниц. Находит битые ссылки, редиректы, дубли title и description, проверяет структуру H1–H2. Даже бесплатной версии хватает для малого бизнеса.</p>
    </div>
  </div>

  <!-- SECTION 5 -->
  <div class="section">
    <div class="section-number">05 / мобильная версия</div>
    <h2 class="section-title">Проверка, которую автоматика не заменит</h2>

    <div class="tool-card">
      <div class="tool-name">Mobile-Friendly Test <a href="https://search.google.com/test/mobile-friendly" target="_blank">↗ search.google.com</a></div>
      <p class="tool-desc">10 секунд — и вы знаете ответ. Если сайт не пригоден для мобильных, Google официально понижает его в мобильной выдаче.</p>
    </div>

    <div class="tip">
      <strong>Но этого недостаточно.</strong> Откройте сайт на своём телефоне и пройдите путь клиента вручную: найдите нужную услугу, дочитайте до кнопки заявки, попробуйте нажать. Иногда кнопка есть — но она такая маленькая, что попасть в неё пальцем невозможно. Иногда форма обратной связи просто не работает на мобильном. Это прямые потери заявок, и автотест этого не покажет.
    </div>

    <div class="meme-block">
      <div class="meme-inner">
        <span class="meme-emoji">📱</span>
        <div class="meme-text">Кнопка «Оставить заявку» на мобильном</div>
        <div class="meme-caption">размер: 8×8 пикселей · цвет: серый на сером · положение: за краем экрана</div>
      </div>
    </div>
  </div>

  <!-- SECTION 6 -->
  <div class="section">
    <div class="section-number">06 / поведение пользователей</div>
    <h2 class="section-title">Как люди ведут себя на сайте на самом деле</h2>

    <p>Если у вас есть доступ к сайту или клиент готов дать его на время — подключите один из этих инструментов. Вы буквально смотрите, как реальный человек заходит на сайт, куда кликает и где уходит.</p>

    <div class="tool-card">
      <div class="tool-name">Microsoft Clarity <a href="https://clarity.microsoft.com" target="_blank">↗ clarity.microsoft.com</a></div>
      <p class="tool-desc">Полностью бесплатный инструмент от Microsoft. Записывает видеосессии пользователей и строит тепловые карты кликов. Чаще всего именно здесь обнаруживается самое неожиданное: люди не доходят до кнопки заявки, кликают на некликаемые элементы или путаются в навигации.</p>
    </div>

    <div class="tool-card">
      <div class="tool-name">Яндекс.Метрика — Вебвизор <a href="https://metrika.yandex.ru" target="_blank">↗ metrika.yandex.ru</a></div>
      <p class="tool-desc">Аналог для РФ-аудитории, привычный и бесплатный. Вебвизор пишет записи сессий, Метрика показывает карты кликов и воронки. В 2025 году интерфейс обновился — появились «Воронки» с настраиваемыми шагами.</p>
    </div>
  </div>

  <!-- SECTION 7 -->
  <div class="section">
    <div class="section-number">07 / технологии</div>
    <h2 class="section-title">На чём сделан сайт и почему это важно</h2>

    <div class="tool-card">
      <div class="tool-name">Wappalyzer <a href="https://wappalyzer.com" target="_blank">↗ wappalyzer.com</a></div>
      <p class="tool-desc">Установите расширение для Chrome или Firefox. Зайдите на любой сайт — и сразу увидите технологии: CMS, плагины, скрипты, фреймворки.</p>
    </div>

    <div class="example-block">
      <div class="example-label">Как говорить с клиентом</div>
      <p>«Ваш сайт работает на WordPress 5.2 и не обновлялся с 2019 года. Устаревшие плагины взламывают. Поддерживать такой сайт со временем дороже, чем сделать новый».</p>
    </div>

    <div class="meme-block">
      <div class="meme-dialogue">
        <div>
          <div class="meme-bubble-label">Wappalyzer показал</div>
          <div class="meme-bubble left">WordPress 4.9 · jQuery 1.8 · PHP 5.6 · последнее обновление: 7 лет назад</div>
        </div>
        <div>
          <div class="meme-bubble-label" style="text-align:right;">Хакеры в 3:00 ночи</div>
          <div class="meme-bubble right">Спасибо, удобно 🎁</div>
        </div>
      </div>
    </div>
  </div>

  <!-- SECTION 8 -->
  <div class="section">
    <div class="section-number">08 / репутация</div>
    <h2 class="section-title">Карты и отзывы — трафик, который уже ищет вас</h2>

    <p>Найдите компанию в Google Картах, Яндекс.Картах и 2ГИС. Есть ли карточка? Заполнена ли? Есть ли фотографии, описание, ответы на отзывы?</p>

    <p>Для малого бизнеса с локальной аудиторией карточка в Картах часто приносит больше клиентов, чем сам сайт. Это люди, которые уже ищут то, что вы предлагаете — прямо сейчас, рядом с вами.</p>

    <div class="tip">
      <strong>Отдельный момент — отзывы.</strong> Посмотрите на Zoon, Флампе, отраслевых агрегаторах. Что пишут? Отвечает ли компания? Часто оказывается, что негативный отзыв двухлетней давности без ответа — первое, что видит человек перед тем как принять решение.
    </div>
  </div>

  <!-- TOOLS TABLE -->
  <div class="section">
    <div class="section-number">итого</div>
    <h2 class="section-title">Все инструменты в одном месте</h2>

    <table class="tools-table">
      <thead>
        <tr>
          <th>Что проверяем</th>
          <th>Инструмент</th>
          <th>Бесплатно</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Скорость</td>
          <td><a href="https://pagespeed.web.dev">PageSpeed</a>, <a href="https://gtmetrix.com">GTmetrix</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>SEO и индексация</td>
          <td><a href="https://ahrefs.com/webmaster-tools">Ahrefs WMT</a>, <a href="https://webmaster.yandex.ru">Я.Вебмастер</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>Комплексный аудит (РФ)</td>
          <td><a href="https://pr-cy.ru">PR-CY</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>Конкуренты</td>
          <td><a href="https://similarweb.com">SimilarWeb</a></td>
          <td>базово ✓</td>
        </tr>
        <tr>
          <td>Технические ошибки</td>
          <td><a href="https://validator.w3.org">W3C</a>, <a href="https://ssllabs.com/ssltest">SSL Labs</a>, <a href="https://screamingfrog.co.uk">Screaming Frog</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>Мобильная версия</td>
          <td><a href="https://search.google.com/test/mobile-friendly">Mobile-Friendly Test</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>Поведение пользователей</td>
          <td><a href="https://clarity.microsoft.com">Microsoft Clarity</a>, <a href="https://metrika.yandex.ru">Яндекс.Метрика</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>Технологии сайта</td>
          <td><a href="https://wappalyzer.com">Wappalyzer</a></td>
          <td>✓</td>
        </tr>
        <tr>
          <td>Репутация и карты</td>
          <td>Google Карты, Яндекс.Карты, 2ГИС</td>
          <td>✓</td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- SUMMARY -->
  <div class="summary-section">
    <h2>Что делать с тем, что нашли</h2>
    <p>Соберите всё в один документ. Для каждой проблемы напишите не только что не так, но и что это значит для бизнеса конкретно.</p>

    <div class="example-block">
      <div class="example-label">❌ Плохо</div>
      <p>«Низкий PageSpeed», «нет карточки в Картах», «устаревший WordPress».</p>
    </div>

    <div class="example-block" style="margin-top:14px; border-left-color: #4ade80;">
      <div class="example-label" style="color:#4ade80;">✓ Хорошо</div>
      <p>«Сайт грузится 6 секунд на телефоне — это потеря ~40% посетителей до первого экрана». «Ваших конкурентов находят в Картах, вас — нет, это потерянные лиды прямо сейчас».</p>
    </div>

    <p style="margin-top:20px;">Бизнес понимает деньги, клиентов и конкурентов. Говорите на этом языке — и вас услышат.</p>
  </div>

  <!-- CTA -->
  <div class="cta-section">
    <h3>Хотите, чтобы такой аудит сделала я?</h3>

    <div class="social-proof-grid">
      <div class="sp-card">
        <div class="sp-number">5+</div>
        <div class="sp-label">лет в дизайне</div>
      </div>
      <div class="sp-card">
        <div class="sp-number">30+</div>
        <div class="sp-label">сданных проектов</div>
      </div>
      <div class="sp-card">
        <div class="sp-number">3</div>
        <div class="sp-label">направления: логотип, сайт, фирстиль</div>
      </div>
    </div>

    <div class="reviews-row">
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">«Лера сделала сайт для нашей логистической компании с нуля — сдала в срок, по техзаданию, без правок по 10 раз. Редкость»</p>
        <div class="review-author">— клиент, Атлас Карго Про</div>
      </div>
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">«Логотип и фирменный стиль — получили то, чего хотели с первого раза. Понимает задачу бизнеса, не просто рисует красиво»</p>
        <div class="review-author">— клиент, малый бизнес</div>
      </div>
    </div>

    <p class="cta-desc">Приду с конкретными данными по вашему сайту, покажу точки роста и предложу решение. Без воды и абстрактных рекомендаций.</p>

    <div class="cta-buttons">
      <a class="cta-btn" href="https://t.me/lera_n23" target="_blank">✈ Написать в Telegram</a>
      <a class="cta-btn cta-btn-outline" href="https://www.instagram.com/velary_design/" target="_blank">Смотреть работы →</a>
    </div>
  </div>

  <!-- INSTAGRAM PROFILE CARD -->
  <div class="ig-card">
    <div class="ig-card-left">
      <div class="ig-avatar">В</div>
      <div class="ig-info">
        <div class="ig-handle">@velary_design</div>
        <div class="ig-name">Валерия Нестерова</div>
        <div class="ig-bio">логотип · сайт · фирменный стиль</div>
      </div>
    </div>
    <a class="ig-follow-btn" href="https://www.instagram.com/velary_design/" target="_blank">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1.2" fill="currentColor" stroke="none"/></svg>
      Подписаться
    </a>
  </div>

</div>

<div class="footer">
  <p>© 2026 · Методичка Валерии Нестеровой · <a href="https://www.instagram.com/velary_design/" style="color:var(--accent); text-decoration:none;">@velary_design</a></p>
  <p style="margin-top:6px;">Веб-дизайн · Логотипы · Фирменный стиль</p>
</div>

</body>
</html>
