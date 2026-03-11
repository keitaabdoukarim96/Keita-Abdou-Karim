<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GitHub README — Keita</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #1c2128;
    --border: #30363d;
    --accent: #00d4aa;
    --accent2: #7c3aed;
    --accent3: #f59e0b;
    --text: #e6edf3;
    --muted: #8b949e;
    --mono: 'Space Mono', monospace;
    --sans: 'Syne', sans-serif;
    --body: 'Inter', sans-serif;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--body);
    min-height: 100vh;
    padding: 40px 20px;
  }

  .readme-wrapper {
    max-width: 860px;
    margin: 0 auto;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  /* GitHub top bar */
  .github-bar {
    background: var(--bg2);
    border-bottom: 1px solid var(--border);
    padding: 12px 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .github-bar .dot {
    width: 12px; height: 12px;
    border-radius: 50%;
  }
  .dot.red { background: #ff5f57; }
  .dot.yellow { background: #febc2e; }
  .dot.green { background: #28c840; }
  .github-bar span {
    margin-left: 12px;
    color: var(--muted);
    font-family: var(--mono);
    font-size: 12px;
  }

  /* README content */
  .readme-content {
    padding: 48px 48px;
  }

  /* HERO */
  .hero {
    margin-bottom: 40px;
    position: relative;
  }

  .hero-tag {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .hero-tag::before {
    content: '';
    width: 24px;
    height: 1px;
    background: var(--accent);
    display: inline-block;
  }

  .hero h1 {
    font-family: var(--sans);
    font-size: 48px;
    font-weight: 800;
    line-height: 1.1;
    margin-bottom: 8px;
    background: linear-gradient(135deg, #ffffff 0%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-subtitle {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 24px;
    line-height: 1.8;
  }

  .hero-subtitle span {
    color: var(--accent);
  }

  /* Typing animation */
  .typing-line {
    font-family: var(--mono);
    font-size: 14px;
    color: var(--accent);
    background: var(--bg2);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    padding: 12px 16px;
    border-radius: 4px;
    margin-bottom: 32px;
    position: relative;
    overflow: hidden;
  }
  .typing-line::before {
    content: '> ';
    color: var(--muted);
  }
  .cursor {
    display: inline-block;
    width: 2px;
    height: 14px;
    background: var(--accent);
    margin-left: 2px;
    vertical-align: middle;
    animation: blink 1s infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* Badges row */
  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 40px;
  }
  .badge {
    font-family: var(--mono);
    font-size: 11px;
    padding: 5px 12px;
    border-radius: 4px;
    font-weight: 700;
    letter-spacing: 0.5px;
    border: 1px solid;
  }
  .badge.green { background: rgba(0,212,170,0.1); border-color: var(--accent); color: var(--accent); }
  .badge.purple { background: rgba(124,58,237,0.1); border-color: var(--accent2); color: #a78bfa; }
  .badge.yellow { background: rgba(245,158,11,0.1); border-color: var(--accent3); color: var(--accent3); }
  .badge.blue { background: rgba(56,139,253,0.1); border-color: #388bfd; color: #79c0ff; }

  /* SECTION */
  .section {
    margin-bottom: 40px;
  }
  .section-title {
    font-family: var(--sans);
    font-size: 18px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-title .icon {
    font-size: 18px;
  }
  .section-line {
    height: 1px;
    background: linear-gradient(90deg, var(--accent) 0%, transparent 100%);
    margin-bottom: 20px;
    opacity: 0.4;
  }

  /* About */
  .about-text {
    color: var(--muted);
    line-height: 1.8;
    font-size: 14px;
  }
  .about-text strong {
    color: var(--text);
  }
  .about-text .highlight {
    color: var(--accent);
    font-weight: 600;
  }

  /* Skills grid */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
  }
  .skill-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    transition: border-color 0.2s;
    position: relative;
    overflow: hidden;
  }
  .skill-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 100%;
    background: var(--accent);
  }
  .skill-card.purple::before { background: var(--accent2); }
  .skill-card.yellow::before { background: var(--accent3); }
  .skill-card.blue::before { background: #388bfd; }

  .skill-card-title {
    font-family: var(--sans);
    font-size: 13px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .skill-card-items {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    line-height: 1.8;
  }

  /* Stats row */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    margin-bottom: 16px;
  }
  .stat-box {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    text-align: center;
  }
  .stat-number {
    font-family: var(--sans);
    font-size: 28px;
    font-weight: 800;
    color: var(--accent);
    display: block;
  }
  .stat-label {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-top: 4px;
  }

  /* Currently learning */
  .learning-block {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
  }
  .learning-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 8px 0;
    border-bottom: 1px solid var(--border);
    font-family: var(--mono);
    font-size: 12px;
    color: var(--muted);
  }
  .learning-item:last-child { border-bottom: none; }
  .learning-item .status {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--accent);
    flex-shrink: 0;
    box-shadow: 0 0 6px var(--accent);
    animation: pulse 2s infinite;
  }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.4} }
  .learning-item span { color: var(--text); }

  /* Projects */
  .project-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 12px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
  .project-name {
    font-family: var(--sans);
    font-size: 14px;
    font-weight: 700;
    color: var(--accent);
    margin-bottom: 6px;
  }
  .project-desc {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.6;
    max-width: 500px;
  }
  .project-tech {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--muted);
    background: var(--bg3);
    border: 1px solid var(--border);
    padding: 3px 8px;
    border-radius: 4px;
    white-space: nowrap;
  }

  /* Contact */
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
  }
  .contact-item {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    display: flex;
    align-items: center;
    gap: 12px;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--muted);
  }
  .contact-item .icon { font-size: 20px; }
  .contact-item span { color: var(--text); font-size: 11px; }

  /* Footer quote */
  .footer-quote {
    margin-top: 40px;
    padding: 24px;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    text-align: center;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--muted);
    font-style: italic;
    border-top: 2px solid var(--accent);
  }
  .footer-quote strong {
    color: var(--accent);
    display: block;
    font-size: 14px;
    margin-bottom: 8px;
    font-style: normal;
  }

  /* COPY BOX */
  .copy-section {
    margin-top: 48px;
    border-top: 1px solid var(--border);
    padding-top: 48px;
  }
  .copy-label {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 16px;
    text-align: center;
  }
  .copy-box {
    background: #0a0f16;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 24px;
    font-family: var(--mono);
    font-size: 11px;
    color: #79c0ff;
    line-height: 1.7;
    white-space: pre-wrap;
    overflow-x: auto;
    position: relative;
  }
  .copy-btn {
    position: absolute;
    top: 12px; right: 12px;
    background: var(--accent);
    color: #000;
    border: none;
    padding: 6px 14px;
    border-radius: 4px;
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 700;
    cursor: pointer;
    letter-spacing: 0.5px;
  }
  .copy-btn:hover { opacity: 0.85; }
</style>
</head>
<body>

<div class="readme-wrapper">
  <div class="github-bar">
    <div class="dot red"></div>
    <div class="dot yellow"></div>
    <div class="dot green"></div>
    <span>keita / README.md</span>
  </div>

  <div class="readme-content">

    <!-- HERO -->
    <div class="hero">
      <div class="hero-tag">Bienvenue sur mon GitHub</div>
      <h1>Keita</h1>
      <div class="hero-subtitle">
        <span>Expert SEO/SEA</span> · Intégrateur Web · Développeur No-Code IA<br>
        Prompt Engineering · Automatisation · France 🇫🇷
      </div>

      <div class="typing-line">
        En formation intensive · De zéro à expert · Chaque semaine je publie ce que j'apprends<span class="cursor"></span>
      </div>

      <div class="badges">
        <span class="badge green">🔍 SEO / SEA</span>
        <span class="badge blue">🌐 Intégration Web</span>
        <span class="badge purple">🤖 No-Code IA</span>
        <span class="badge yellow">⚡ Automatisation</span>
        <span class="badge green">💬 Prompt Engineering</span>
        <span class="badge blue">📊 Google Analytics 4</span>
      </div>
    </div>

    <!-- ABOUT -->
    <div class="section">
      <div class="section-title"><span class="icon">👤</span> Qui suis-je ?</div>
      <div class="section-line"></div>
      <p class="about-text">
        Je suis <strong>Keita</strong>, basé en <strong>France</strong>. Je me forme de manière intensive pour devenir un expert reconnu en <span class="highlight">SEO/SEA</span>, <span class="highlight">intégration web multi-CMS</span> et <span class="highlight">développement d'applications avec l'IA</span>.<br><br>
        Ma philosophie : <strong>apprendre → appliquer → publier</strong>. Chaque chose que j'apprends devient du contenu concret. Pas de théorie sans pratique. Ce GitHub est le reflet direct de ma progression réelle — avec ses erreurs, ses découvertes et ses victoires.
      </p>
    </div>

    <!-- COMPÉTENCES -->
    <div class="section">
      <div class="section-title"><span class="icon">🛠️</span> Mes Compétences</div>
      <div class="section-line"></div>
      <div class="skills-grid">
        <div class="skill-card">
          <div class="skill-card-title">🔍 SEO / SEA</div>
          <div class="skill-card-items">
            → Audit technique & On-Page<br>
            → Keyword Research<br>
            → Google Ads (Search, Display)<br>
            → Netlinking & Autorité
          </div>
        </div>
        <div class="skill-card blue">
          <div class="skill-card-title">🌐 Intégration Web</div>
          <div class="skill-card-items">
            → WordPress (sans template)<br>
            → HTML / CSS / JS<br>
            → Multi-CMS : Wix, Shopify<br>
            → Intégration de maquettes Figma
          </div>
        </div>
        <div class="skill-card purple">
          <div class="skill-card-title">🤖 Développeur No-Code IA</div>
          <div class="skill-card-items">
            → Apps web & mobile avec Claude<br>
            → Sécurité & déploiement<br>
            → Prompt Engineering avancé<br>
            → Bibliothèque de prompts
          </div>
        </div>
        <div class="skill-card yellow">
          <div class="skill-card-title">⚡ Automatisation</div>
          <div class="skill-card-items">
            → Make (Integromat)<br>
            → n8n self-hosted<br>
            → API Claude + workflows<br>
            → Rapports SEO automatisés
          </div>
        </div>
      </div>
    </div>

    <!-- STATS -->
    <div class="section">
      <div class="section-title"><span class="icon">📊</span> Analyse & Data</div>
      <div class="section-line"></div>
      <div class="stats-row">
        <div class="stat-box">
          <span class="stat-number">GA4</span>
          <div class="stat-label">Google Analytics 4</div>
        </div>
        <div class="stat-box">
          <span class="stat-number">GSC</span>
          <div class="stat-label">Search Console</div>
        </div>
        <div class="stat-box">
          <span class="stat-number">GTM</span>
          <div class="stat-label">Tag Manager</div>
        </div>
      </div>
    </div>

    <!-- EN COURS -->
    <div class="section">
      <div class="section-title"><span class="icon">🚀</span> En ce moment — Formation Active</div>
      <div class="section-line"></div>
      <div class="learning-block">
        <div class="learning-item">
          <div class="status"></div>
          <div><span>Phase 0</span> — Fondation blog/portfolio WordPress + LinkedIn</div>
        </div>
        <div class="learning-item">
          <div class="status"></div>
          <div><span>Phase 1</span> — Bases SEO · Intégration multi-CMS · Google Analytics 4</div>
        </div>
        <div class="learning-item" style="opacity:0.4;">
          <div class="status" style="background:#30363d;box-shadow:none;animation:none;"></div>
          <div><span>Phase 2</span> — Contenu SEO · LinkedIn · Écriture humaine (pas IA)</div>
        </div>
        <div class="learning-item" style="opacity:0.4;">
          <div class="status" style="background:#30363d;box-shadow:none;animation:none;"></div>
          <div><span>Phase 3+</span> — Google Ads · Prompt Engineering · Automatisation</div>
        </div>
      </div>
    </div>

    <!-- PROJETS -->
    <div class="section">
      <div class="section-title"><span class="icon">📁</span> Projets en cours</div>
      <div class="section-line"></div>
      <div class="project-card">
        <div>
          <div class="project-name">🌐 Blog & Portfolio SEO/SEA</div>
          <div class="project-desc">Site WordPress custom (sans template) — intégration de maquette, optimisation SEO complète, GA4 + Search Console configurés.</div>
        </div>
        <span class="project-tech">WordPress · SEO</span>
      </div>
      <div class="project-card">
        <div>
          <div class="project-name">⚡ Workflows d'automatisation IA</div>
          <div class="project-desc">Automatisation de rapports SEO, publication LinkedIn et veille concurrentielle avec Make + Claude API.</div>
        </div>
        <span class="project-tech">Make · Claude API</span>
      </div>
      <div class="project-card">
        <div>
          <div class="project-name">🤖 Apps No-Code avec IA</div>
          <div class="project-desc">Développement d'applications web et mobile complexes via Prompt Engineering avec Claude — sécurité, déploiement inclus.</div>
        </div>
        <span class="project-tech">Claude · No-Code</span>
      </div>
    </div>

    <!-- CONTACT -->
    <div class="section">
      <div class="section-title"><span class="icon">📬</span> Me contacter</div>
      <div class="section-line"></div>
      <div class="contact-grid">
        <div class="contact-item">
          <span class="icon">💼</span>
          <div>LinkedIn<br><span>→ /in/keita (en optimisation)</span></div>
        </div>
        <div class="contact-item">
          <span class="icon">📍</span>
          <div>Localisation<br><span>→ France 🇫🇷</span></div>
        </div>
        <div class="contact-item">
          <span class="icon">✍️</span>
          <div>Blog / Portfolio<br><span>→ En construction</span></div>
        </div>
        <div class="contact-item">
          <span class="icon">📧</span>
          <div>Email<br><span>→ À venir</span></div>
        </div>
      </div>
    </div>

    <!-- QUOTE -->
    <div class="footer-quote">
      <strong>"On apprend → On applique → On publie"</strong>
      Ce GitHub grandit avec moi. Chaque commit est une leçon. Chaque projet est une preuve.
    </div>

    <!-- COPY SECTION -->
    <div class="copy-section">
      <div class="copy-label">📋 Code README.md — Copie dans GitHub</div>
      <div style="position:relative;">
        <pre class="copy-box" id="readme-code"><!-- KEITA — README.md GitHub Profil -->

&lt;div align="center"&gt;

## 👋 Bonjour, je suis **Keita**
### Expert SEO/SEA · Intégrateur Web · Développeur No-Code IA · Automatisation

&lt;br&gt;

![Badge](https://img.shields.io/badge/SEO%2FSEA-Expert%20en%20formation-00d4aa?style=for-the-badge)
![Badge](https://img.shields.io/badge/No--Code%20IA-Claude%20%7C%20Automatisation-7c3aed?style=for-the-badge)
![Badge](https://img.shields.io/badge/France-Based-f59e0b?style=for-the-badge)

&lt;/div&gt;

---

### 👤 Qui suis-je ?

Je suis **Keita**, basé en **France**. Je me forme de manière intensive pour devenir un expert reconnu en **SEO/SEA**, **intégration web multi-CMS** et **développement d'applications avec l'IA**.

> 💡 **Ma philosophie :** `apprendre → appliquer → publier`
> Chaque chose que j'apprends devient du contenu concret.
> Ce GitHub est le reflet direct de ma progression réelle.

---

### 🛠️ Mes Compétences

| 🔍 SEO / SEA | 🌐 Intégration Web | 🤖 No-Code IA | ⚡ Automatisation |
|---|---|---|---|
| Audit technique | WordPress sans template | Apps Claude | Make (Integromat) |
| Keyword Research | HTML / CSS / JS | Prompt Engineering | n8n self-hosted |
| Google Ads Search | Multi-CMS | Sécurité + déploiement | API Claude |
| Netlinking | Intégration Figma | Bibliothèque prompts | Rapports SEO auto |

---

### 📊 Outils Maîtrisés

![GA4](https://img.shields.io/badge/Google%20Analytics%204-Analyse-orange?style=flat-square&logo=google-analytics)
![GSC](https://img.shields.io/badge/Search%20Console-SEO-blue?style=flat-square&logo=google)
![GTM](https://img.shields.io/badge/Google%20Tag%20Manager-Tracking-4285F4?style=flat-square&logo=google-tag-manager)
![WordPress](https://img.shields.io/badge/WordPress-Intégration-21759B?style=flat-square&logo=wordpress)
![Claude](https://img.shields.io/badge/Claude%20AI-Développement-7C3AED?style=flat-square)

---

### 🚀 Formation Active — Ma Progression

- ✅ **Phase 0** — Fondation blog/portfolio WordPress + LinkedIn
- 🔜 **Phase 1** — Bases SEO · Intégration multi-CMS · GA4
- ⏳ **Phase 2** — Contenu SEO · LinkedIn · Écriture humaine
- ⏳ **Phase 3** — Google Ads · SEA de A à Z
- ⏳ **Phase 4** — Analyse données · Looker Studio · KPIs
- ⏳ **Phase 5** — Autorité · Netlinking · Personal Branding
- ⏳ **Phase 6** — Prompt Engineering avancé avec Claude
- ⏳ **Phase 7** — Automatisation IA (Make · n8n · API)

---

### 📁 Projets en cours

🌐 **Blog & Portfolio SEO/SEA** — WordPress custom, GA4, Search Console
⚡ **Workflows d'automatisation IA** — Make + Claude API + LinkedIn auto
🤖 **Apps No-Code** — Applications web/mobile via Prompt Engineering Claude

---

### 📬 Me contacter

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Keita-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/)
[![Blog](https://img.shields.io/badge/Blog%20Portfolio-En%20construction-00d4aa?style=for-the-badge)](https://github.com/)

---

&lt;div align="center"&gt;

*"On apprend → On applique → On publie.*
*Chaque commit est une leçon. Chaque projet est une preuve."*

&lt;/div&gt;</pre>
        <button class="copy-btn" onclick="copyReadme()">📋 Copier</button>
      </div>
    </div>

  </div>
</div>

<script>
function copyReadme() {
  const code = document.getElementById('readme-code').innerText;
  navigator.clipboard.writeText(code).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✅ Copié !';
    setTimeout(() => btn.textContent = '📋 Copier', 2000);
  });
}
</script>

</body>
</html>
