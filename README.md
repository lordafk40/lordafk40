<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <title>REİZ — Mustafa Çoban | REİZMEDYA</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="REİZ — Mustafa Çoban | Full-Stack Developer, AI & Cyber Security Enthusiast, Founder of REİZMEDYA." />

  <!-- Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />

  <style>
    :root {
      --bg: #05070b;
      --bg-soft: #0b1018;
      --card: #101725;
      --accent: #00e7ff;
      --accent-soft: rgba(0, 231, 255, 0.12);
      --accent-2: #5b8dff;
      --text: #e7edf7;
      --muted: #9aa4c3;
      --danger: #ff3b6b;
      --success: #00d985;
      --radius-lg: 18px;
      --radius-md: 12px;
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.65);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #13213a 0, #05070b 55%);
      color: var(--text);
      line-height: 1.6;
      min-height: 100vh;
    }

    a {
      color: var(--accent);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    /* Layout */
    .page {
      max-width: 1080px;
      margin: 32px auto 64px;
      padding: 0 16px;
    }

    header {
      display: flex;
      gap: 24px;
      align-items: center;
      margin-bottom: 28px;
    }

    header .avatar-wrap {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 20%, #2af6ff, #0042ff);
      padding: 5px;
      box-shadow: 0 0 35px rgba(0, 231, 255, 0.55);
      flex-shrink: 0;
    }

    header .avatar-inner {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: #05070b url("https://i.ibb.co/2t9CfqN/reizmedya-logo.png") center/cover no-repeat;
      border: 2px solid rgba(255, 255, 255, 0.1);
    }

    header .info h1 {
      font-size: 28px;
      letter-spacing: 0.06em;
    }

    header .info h2 {
      font-size: 16px;
      font-weight: 500;
      color: var(--muted);
      margin: 6px 0 10px;
    }

    .tagline {
      font-style: italic;
      color: var(--accent);
      font-size: 14px;
    }

    .chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 12px;
    }

    .chip {
      border-radius: 999px;
      padding: 6px 12px;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      border: 1px solid rgba(255, 255, 255, 0.07);
      background: rgba(255, 255, 255, 0.02);
      color: var(--muted);
    }

    .chip.primary {
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      color: #02040a;
      border: none;
    }

    nav {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
      margin: 10px 0 26px;
    }

    nav a {
      font-size: 13px;
      padding: 6px 12px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.08);
      background: rgba(5, 9, 20, 0.75);
      color: var(--muted);
    }

    nav a:hover {
      background: var(--accent-soft);
      color: var(--accent);
    }

    section {
      margin-bottom: 26px;
    }

    .section-card {
      background: linear-gradient(135deg, rgba(255, 255, 255, 0.02), rgba(0, 0, 0, 0.7));
      border-radius: var(--radius-lg);
      border: 1px solid rgba(255, 255, 255, 0.07);
      padding: 18px 18px 20px;
      box-shadow: var(--shadow-soft);
      backdrop-filter: blur(18px);
    }

    .section-title {
      font-size: 17px;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .section-title span {
      width: 24px;
      height: 24px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 20%, var(--accent), var(--accent-2));
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 13px;
      color: #02040a;
    }

    .section-title small {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: .16em;
      color: var(--muted);
      margin-left: auto;
    }

    /* Hakkımda */
    .about p {
      font-size: 14px;
      color: var(--muted);
      margin-bottom: 6px;
    }

    .bullet-inline {
      display: inline-flex;
      gap: 6px;
      flex-wrap: wrap;
      margin-top: 6px;
    }

    .pill {
      font-size: 11px;
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.06);
      color: var(--text);
    }

    /* Timeline */
    .timeline {
      border-left: 2px solid rgba(255, 255, 255, 0.08);
      margin-left: 6px;
      padding-left: 18px;
      margin-top: 6px;
    }

    .timeline-block {
      margin-bottom: 12px;
      position: relative;
    }

    .timeline-block::before {
      content: '';
      position: absolute;
      left: -20px;
      top: 4px;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 8px var(--accent);
    }

    .timeline-block h4 {
      font-size: 14px;
      margin-bottom: 2px;
      color: var(--text);
    }

    .timeline-block ul {
      list-style: none;
      font-size: 13px;
      color: var(--muted);
    }

    .timeline-block li::before {
      content: "• ";
      color: var(--accent);
    }

    /* Tech tables */
    .tech-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 14px;
      margin-top: 10px;
    }

    .tech-column {
      background: rgba(5, 9, 20, 0.9);
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.06);
      padding: 10px 12px 9px;
    }

    .tech-column h4 {
      font-size: 13px;
      margin-bottom: 6px;
      color: var(--accent);
    }

    .tech-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 12px;
      color: var(--muted);
      padding: 2px 0;
      border-bottom: 1px dashed rgba(255, 255, 255, 0.06);
    }

    .tech-item:last-child {
      border-bottom: none;
    }

    .tech-item a {
      font-size: 11px;
      color: var(--accent-2);
      word-break: break-all;
    }

    /* Awards & Projects */
    .badge-list {
      display: flex;
      flex-direction: column;
      gap: 4px;
      font-size: 13px;
      color: var(--muted);
    }

    .badge-list span {
      color: var(--accent);
      margin-right: 6px;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 12px;
      margin-top: 8px;
    }

    .project-card {
      background: rgba(5, 9, 20, 0.9);
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.06);
      padding: 10px 12px;
      font-size: 13px;
      color: var(--muted);
    }

    .project-card h4 {
      font-size: 14px;
      color: var(--text);
      margin-bottom: 4px;
    }

    /* Contact */
    .contact-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 8px;
      margin-top: 6px;
      font-size: 13px;
    }

    .contact-item i {
      color: var(--accent);
      margin-right: 8px;
      width: 14px;
      text-align: center;
    }

    /* Stats */
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 14px;
      margin-top: 10px;
    }

    .stats-grid img {
      width: 100%;
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.06);
      background: #0b1018;
    }

    /* Motto */
    .motto {
      margin-top: 8px;
      border-radius: var(--radius-lg);
      padding: 14px 16px;
      background: radial-gradient(circle at top left, rgba(0, 231, 255, 0.2), transparent),
                  radial-gradient(circle at bottom right, rgba(255, 59, 107, 0.18), transparent),
                  #05070b;
      border: 1px solid rgba(255, 255, 255, 0.08);
      text-align: center;
      font-size: 14px;
      color: var(--accent);
    }

    /* Smooth scroll */
    html {
      scroll-behavior: smooth;
    }

    @media (max-width: 640px) {
      header {
        flex-direction: column;
        align-items: flex-start;
      }
      header .avatar-wrap {
        margin: 0 auto;
      }
    }
  </style>

  <script>
    // Basit highlight: menüde tıklanan bölüm sarı border verir
    document.addEventListener("DOMContentLoaded", () => {
      const links = document.querySelectorAll("nav a[href^='#']");
      links.forEach((link) => {
        link.addEventListener("click", (e) => {
          links.forEach(l => l.classList.remove("active"));
          e.currentTarget.classList.add("active");
        });
      });
    });
  </script>
</head>
<body>
  <div class="page">

    <!-- Header -->
    <header>
      <div class="avatar-wrap">
        <div class="avatar-inner"></div>
      </div>
      <div class="info">
        <h1>REİZ — Mustafa Çoban</h1>
        <h2>Full-Stack Developer • AI &amp; Cyber Security Enthusiast • Founder of REİZMEDYA</h2>
        <div class="tagline">“Kod benim için meslek değil, kaderimdi.”</div>

        <div class="chip-row">
          <span class="chip primary">Full-Stack</span>
          <span class="chip">AI Developer</span>
          <span class="chip">Cyber Security</span>
          <span class="chip">Founder @ REİZMEDYA</span>
          <span class="chip">Kırşehir • TR</span>
        </div>
      </div>
    </header>

    <!-- Nav -->
    <nav>
      <a href="#about">Hakkımda</a>
      <a href="#timeline">Eğitim &amp; Kariyer</a>
      <a href="#skills">Teknolojiler</a>
      <a href="#awards">Ödüller</a>
      <a href="#projects">Projeler</a>
      <a href="#contact">İletişim</a>
      <a href="#stats">İstatistikler</a>
    </nav>

    <!-- About -->
    <section id="about">
      <div class="section-card about">
        <h3 class="section-title">
          <span>🧬</span> 1) HAKKIMDA – GEÇMİŞTEN BUGÜNE REİZ HİKAYESİ
        </h3>
        <p>Ben Mustafa Çoban (REİZ). 22 Ekim 2004’te Kırşehir’de doğdum. Çocukluğumdan beri asker-polis olmak istedim, fakat göz rahatsızlığım nedeniyle bu hayal kapandı. Ama vazgeçmek genlerimde yoktu.</p>
        <p>Bilgisayara ilk sarıldığım gün kaderim değişti. Çünkü bugün:</p>
        <div class="bullet-inline">
          <span class="pill">Web geliştirme</span>
          <span class="pill">Yapay zekâ</span>
          <span class="pill">Siber güvenlik</span>
          <span class="pill">Full-Stack mühendislik</span>
          <span class="pill">Tasarım &amp; markalaşma</span>
          <span class="pill">Mobil uygulama geliştirme</span>
        </div>
        <p style="margin-top:8px;">gibi alanlarda Türkiye’nin en genç, en çok proje üreten geliştiricilerinden biri oldum.</p>
      </div>
    </section>

    <!-- Timeline -->
    <section id="timeline">
      <div class="section-card">
        <h3 class="section-title">
          <span>🚀</span> 2) EĞİTİM &amp; KARİYER ZAMAN ÇİZELGESİ
        </h3>

        <div class="timeline">
          <div class="timeline-block">
            <h4>📌 İlk Yıllar</h4>
            <ul>
              <li>Vali Mithat Saylam İlköğretim / Yunusemre Ortaokulu</li>
              <li>Küçük yaşlardan itibaren bilgisayar merakı</li>
              <li>Unity ile oyun geliştirme denemeleri</li>
              <li>HTML/CSS ile ilk statik siteler</li>
            </ul>
          </div>

          <div class="timeline-block">
            <h4>📌 Lise Dönemi</h4>
            <ul>
              <li>Mehmet Akif Ersoy Anadolu Lisesi (haksız şekilde sınıf tekrarı)</li>
              <li>Endüstri Meslek Lisesi – Web Tasarım temeli</li>
              <li>İlk freelance işler: logo, afiş, küçük web siteleri</li>
            </ul>
          </div>

          <div class="timeline-block">
            <h4>📌 Üniversite: Ahi Evran Üniversitesi</h4>
            <ul>
              <li>Web Tasarımı ve Kodlama Bölümü – bu dönem, REİZ karakterinin net oturduğu dönem oldu.</li>
              <li>APDAS projesinin temelleri burada atıldı</li>
              <li>İlk kurumsal müşteri projeleri</li>
              <li>Tasarım &amp; yazılım yeteneğinin birleştiği dönem</li>
              <li>Üniversitede tanınan, teknik destek veren öğrenci oldum</li>
            </ul>
          </div>

          <div class="timeline-block">
            <h4>📌 2024–2025: PATLAMA DÖNEMİ</h4>
            <ul>
              <li>Next.js, React, MongoDB, FastAPI… Hepsinin profesyonel kullanımına geçiş</li>
              <li>İlk büyük projeler, e-ticaret siteleri</li>
              <li>Üniversite sitesi (APDAS), turizm siteleri, firmalarla çalışmaya başlama</li>
            </ul>
          </div>

          <div class="timeline-block">
            <h4>📌 REİZMEDYA – DOĞUŞ</h4>
            <ul>
              <li>Kırşehir’de yerel bir marka değil; gelecekte ulusal ve global yazılım ajansı olacak bir ekibin ilk adımı.</li>
              <li>REİZMEDYA bugün:</li>
              <li>Web geliştirme • Mobil uygulama • AI sistemleri • Siber güvenlik • SEO &amp; analiz • Sosyal medya yönetimi • Tasarım &amp; branding</li>
              <li>gibi tüm alanları kapsayan full-stack bir dijital medya &amp; teknoloji markasıdır.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills">
      <div class="section-card">
        <h3 class="section-title">
          <span>🧠</span> 3) TEKNOLOJİ YETKİNLİKLERİ (LOGOLU)
        </h3>

        <div class="tech-grid">
          <div class="tech-column">
            <h4>🔵 Frontend</h4>
            <div class="tech-item">
              <span>HTML5</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>CSS3</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>JavaScript</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>React</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>Next.js</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>Tailwind</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg">logo</a>
            </div>
          </div>

          <div class="tech-column">
            <h4>🟢 Backend</h4>
            <div class="tech-item">
              <span>Node.js</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-plain.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>FastAPI</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>Python</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>Express.js</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg">logo</a>
            </div>
          </div>

          <div class="tech-column">
            <h4>🟣 Veritabanı</h4>
            <div class="tech-item">
              <span>MongoDB</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>MySQL</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg">logo</a>
            </div>
          </div>

          <div class="tech-column">
            <h4>🎨 Tasarım &amp; Araçlar</h4>
            <div class="tech-item">
              <span>Figma</span>
              <a href="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg">logo</a>
            </div>
            <div class="tech-item">
              <span>Adobe Illustrator</span>
              <a href="https://cdn-icons-png.flaticon.com/512/5968/5968525.png">logo</a>
            </div>
            <div class="tech-item">
              <span>Canva</span>
              <a href="https://cdn-icons-png.flaticon.com/512/5968/5968520.png">logo</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Awards -->
    <section id="awards">
      <div class="section-card">
        <h3 class="section-title">
          <span>🏆</span> 4) ÖDÜLLER, BAŞARILAR, RESMİ KAYITLAR
        </h3>
        <div class="badge-list">
          <div><span>🎖</span> TÜBİTAK 2209-A Araştırma Projesi Başarılı Onay</div>
          <div><span>🎖</span> APDAS – Üniversite çapında akademik analiz sistemi projesi</div>
          <div><span>🎖</span> Turizm &amp; e-ticaret siteleri geliştirme başarıları</div>
          <div><span>🎖</span> Yerel işletmelerle kurumsal yazılım işbirlikleri</div>
          <div><span>🎖</span> AEÜ öğrencileri arasında teknik destek ve yazılım danışmanlığı</div>
          <div><span>🎖</span> REİZMEDYA’nın resmi olarak kurulması – startup temeli</div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <div class="section-card">
        <h3 class="section-title">
          <span>💻</span> 5) BÜYÜK PROJELERİM
        </h3>

        <div class="projects-grid">
          <div class="project-card">
            <h4>🟦 APDAS – Akademik Performans ve Ders Analiz Sistemi</h4>
            <p>Üniversitenin tüm akademik yapısını dijitale taşıyan dev proje. 100+ sayfalık dokümantasyon, grafikler, analizler, kullanıcı panelleri, dashboard…</p>
          </div>
          <div class="project-card">
            <h4>🟩 Reiz AI</h4>
            <p>Çok dilli, sohbet geçmişli, premium tasarımlı AI platformu.</p>
          </div>
          <div class="project-card">
            <h4>🟧 Reiz Form (Next.js + MongoDB)</h4>
            <p>Dinamik form oluşturma paneli. Kullanıcılar form üretiyor, veriler MongoDB’ye kaydediliyor.</p>
          </div>
          <div class="project-card">
            <h4>🟪 Ayıntap Gross App (React Native / Expo)</h4>
            <p>Mobil market uygulaması.</p>
          </div>
          <div class="project-card">
            <h4>🟨 Seyahat &amp; Turizm Siteleri</h4>
            <p>Aslantur.com başta olmak üzere çeşitli turizm ve rezervasyon siteleri.</p>
          </div>
          <div class="project-card">
            <h4>🟥 GlowBeauty</h4>
            <p>Perfume &amp; beauty temalı e-ticaret + müşteri deneyimi sitesi.</p>
          </div>
          <div class="project-card">
            <h4>REİZWEB &amp; REİZMOBİL • Sohbet Uygulaması Projesi</h4>
            <p>Web ve mobil tarafta kurumsal projeler; gerçek zamanlı sohbet altyapısı.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <div class="section-card">
        <h3 class="section-title">
          <span>📬</span> 6) İLETİŞİM BİLGİLERİ
        </h3>
        <div class="contact-list">
          <div class="contact-item">
            <i class="fa-solid fa-envelope"></i> 📧 Mail: <a href="mailto:reizmedya@gmail.com">reizmedya@gmail.com</a>
          </div>
          <div class="contact-item">
            <i class="fa-solid fa-globe"></i> 🌍 Website: <a href="https://reizmedya.com" target="_blank">reizmedya.com</a>
          </div>
          <div class="contact-item">
            <i class="fa-brands fa-github"></i> 🐙 GitHub: <a href="https://github.com/lordafk40" target="_blank">github.com/lordafk40</a>
          </div>
          <div class="contact-item">
            <i class="fa-brands fa-linkedin"></i> 💼 LinkedIn:
            <a href="https://www.linkedin.com/in/reiz-medya-8a4231380" target="_blank">linkedin.com/in/reiz-medya-8a4231380</a>
          </div>
          <div class="contact-item">
            <i class="fa-brands fa-instagram"></i> 📱 Instagram:
            <a href="https://instagram.com/reizmedya" target="_blank">@reizmedya</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats -->
    <section id="stats">
      <div class="section-card">
        <h3 class="section-title">
          <span>📊</span> 7–9) İSTATİSTİKLER (GitHub &amp; LeetCode)
        </h3>
        <div class="stats-grid">
          <img src="https://github-profile-trophy.vercel.app/?username=REIZ00&theme=onedark&no-frame=true&margin-w=10" alt="GitHub Trophy" />
          <img src="https://github-readme-stats.vercel.app/api?username=REIZ00&show_icons=true&theme=radical" alt="GitHub Stats" />
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=REIZ00&layout=compact&theme=radical" alt="Top Langs" />
          <img src="https://leetcode.card.workers.dev/?username=reiz00&theme=dark&font=baloo&extension=null" alt="LeetCode Stats" />
        </div>

        <div class="motto">
          ⭐ Biz kod yazmıyoruz; sistem kuruyoruz. <br />
          Vizyonumuz Türkiye’den başlar, dünyada tamamlanır. <br />
          Dijital çağın yeni imzası: <strong>REİZMEDYA</strong>.
        </div>
      </div>
    </section>

  </div>
</body>
</html>
