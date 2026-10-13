
<template>
  <section id="home" class="section home front-page">
    <!-- Newspaper edition -->
    <div class="edition-bar">
      <span>VOL. I · NO. 01</span>
      <span>CHENNAI, INDIA</span>
      <span>PORTFOLIO EDITION · 2026</span>
    </div>

    <!-- Masthead -->
    <header class="newspaper-masthead">
      <p class="masthead-overline">An Independent Record of Digital Craft</p>
      <h1 class="newspaper-name">The Daily Chronicle</h1>
      <p class="masthead-subtitle">
        ENGINEERING · TECHNOLOGY · DIGITAL INNOVATION
      </p>
    </header>

    <div class="ornamental-rule">
      <span>✦</span>
    </div>

    <!-- Lead story -->
    <div class="front-kicker">
      <span>THE DEVELOPER'S EDITION</span>
      <span>FEATURE STORY</span>
    </div>

    <h2 class="front-headline">
      Turning Business Problems
      <span>Into Digital Solutions</span>
    </h2>

    <p class="front-byline">
      By Harshavardhini
      <span>·</span>
      Full-Stack Developer
    </p>

    <div class="rule thin"></div>

    <!-- Newspaper columns -->
    <div class="front-grid">
      <article class="front-column lead-story">
        <p class="column-label">THE LEAD STORY</p>

        <h3>
          Building Systems That Work
          Beyond the Screen
        </h3>

        <p class="lead-description">
          In an age where businesses depend on dependable digital
          infrastructure, one developer sets out to transform everyday
          operational challenges into practical, production-ready software.
        </p>

        <div class="lead-image-placeholder">
          <span class="engraving-symbol">✥</span>
          <span>IDEAS INTO INFRASTRUCTURE</span>
          <span class="engraving-symbol">✥</span>
        </div>

        <p class="column-copy">
          From enterprise resource planning platforms to interactive
          dashboards and workflow automation, the work centres on building
          systems that people can rely on in their daily operations.
        </p>
      </article>

      <article class="front-column">
        <p class="column-label">THE ENGINEERING DESK</p>

        <h3>From Concept to Production</h3>

        <p class="column-copy">
          Working across Vue.js, Laravel, APIs, and databases, the focus
          remains on connecting thoughtful interfaces with dependable
          backend systems.
        </p>

        <div class="rule thin"></div>

        <h3>Technology With Purpose</h3>

        <p class="column-copy">
          Payroll, attendance, Kanban workflows, performance metrics,
          and scheduled background tasks all contribute to software
          designed around real operational needs.
        </p>
      </article>

      <aside class="front-column side-story">
        <div class="classified-box">
          <p class="column-label">CAREER CLASSIFIEDS</p>
          <h3>Developer Available</h3>
          <div class="rule thin"></div>
          <p class="column-copy">
            Open to meaningful engineering challenges, collaborative teams,
            and opportunities to build useful digital products.
          </p>
        </div>

        <div class="side-note">
          <p class="column-label">ON THE RECORD</p>
          <p class="side-quote">
            “Good software does more than function.
            It makes work better.”
          </p>
        </div>

        <a href="#projects" class="front-link">
          READ THE PROJECT CHRONICLE →
        </a>
      </aside>
    </div>

    <div class="bottom-edition">
      <span>INDEPENDENTLY BUILT</span>
      <span>DESIGNED WITH PURPOSE</span>
      <span>END OF FRONT PAGE</span>
    </div>
  </section>
</template>

<style scoped>
.front-page {
  max-width: 1240px;
  padding: 32px 48px 60px;
  margin: 0 auto;
}

.edition-bar {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  padding: 8px 0;
  border-top: 2px solid var(--ink);
  border-bottom: 1px solid var(--ink);
  font-size: 9px;
  letter-spacing: 1.5px;
}

.newspaper-masthead {
  text-align: center;
  padding: 20px 0 10px;
}

.masthead-overline {
  font-size: 10px;
  text-align: center;
  font-style: italic;
  color: var(--muted-ink);
}

.newspaper-name {
  font-family: var(--font-masthead);
  font-size: clamp(42px, 7.5vw, 86px);
  line-height: 1.15;
  letter-spacing: 1px;
}

.masthead-subtitle {
  font-size: 9px;
  letter-spacing: 3px;
  margin-top: 6px;
}

.ornamental-rule {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10px 0 20px;
  border-top: 3px double var(--ink);
}

.ornamental-rule span {
  background: var(--paper);
  padding: 0 12px;
  margin-top: -13px;
  font-size: 19px;
}

.front-kicker {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  color: var(--accent);
  font-size: 10px;
  font-weight: bold;
  letter-spacing: 2px;
}

.front-headline {
  max-width: 1000px;
  margin: 14px auto;
  text-align: center;
  font-family: var(--font-heading);
  font-size: clamp(38px, 6vw, 68px);
  font-weight: 900;
  line-height: 1.02;
  letter-spacing: -1.5px;
  text-transform: uppercase;
}

.front-headline span {
  display: block;
  color: var(--accent);
  font-style: italic;
}

.front-byline {
  text-align: center;
  font-size: 11px;
  font-style: italic;
  color: var(--muted-ink);
  margin-bottom: 18px;
}

.front-byline span {
  margin: 0 6px;
}

.front-grid {
  display: grid;
  grid-template-columns: 1.35fr 1fr 0.8fr;
  gap: 24px;
  margin-top: 24px;
  align-items: start;
}

.front-column {
  min-width: 0;
}

.front-column + .front-column {
  border-left: 1px solid var(--line);
  padding-left: 20px;
}

.column-label {
  color: var(--accent);
  font-size: 9px;
  font-weight: bold;
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.front-column h3 {
  font-family: var(--font-heading);
  font-size: 23px;
  line-height: 1.18;
  margin-bottom: 12px;
}

.lead-story h3 {
  font-size: 31px;
}

.lead-description {
  font-family: var(--font-heading);
  font-size: 15px;
  line-height: 1.65;
  font-style: italic;
  text-align: justify;
  margin-bottom: 16px;
}

.column-copy {
  font-size: 12px;
  line-height: 1.85;
  text-align: justify;
  color: var(--muted-ink);
}

.lead-image-placeholder {
  min-height: 115px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  flex-wrap: wrap;
  gap: 10px;
  padding: 20px 8px;
  margin-bottom: 16px;
  border: 3px double var(--line);
  background:
    repeating-linear-gradient(
      0deg,
      transparent,
      transparent 4px,
      rgba(38, 33, 28, 0.035) 5px
    );
  text-align: center;
  font-family: var(--font-heading);
  font-size: 10px;
  letter-spacing: 2px;
}

.engraving-symbol {
  font-size: 28px;
}

.classified-box {
  padding: 14px;
  border: 2px solid var(--ink);
  outline: 1px solid var(--ink);
  outline-offset: 3px;
  margin: 4px 3px 28px;
}

.classified-box h3 {
  font-size: 23px;
  text-align: center;
}

.side-note {
  border-top: 3px double var(--ink);
  border-bottom: 3px double var(--ink);
  padding: 16px 0;
  margin-bottom: 20px;
}

.side-quote {
  font-family: var(--font-heading);
  font-size: 19px;
  font-style: italic;
  line-height: 1.5;
}

.front-link {
  font-size: 9px;
  font-weight: bold;
  letter-spacing: 1px;
  color: var(--accent);
  text-decoration: underline;
}

.bottom-edition {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  margin-top: 32px;
  padding-top: 10px;
  border-top: 3px double var(--ink);
  font-size: 8px;
  letter-spacing: 1.2px;
}

@media (max-width: 850px) {
  .front-grid {
    grid-template-columns: 1fr 1fr;
  }

  .side-story {
    grid-column: 1 / -1;
  }

  .front-column.side-story {
    border-left: 0;
    border-top: 1px solid var(--line);
    padding: 22px 0 0;
  }

  .classified-box {
    max-width: 420px;
    margin-left: auto;
    margin-right: auto;
  }
}

@media (max-width: 560px) {
  .front-page {
    padding: 24px 18px 42px;
  }

  .edition-bar {
    font-size: 7px;
    letter-spacing: 0.5px;
  }

  .front-kicker {
    font-size: 8px;
    letter-spacing: 1px;
  }

  .front-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .front-column + .front-column {
    border-left: 0;
    border-top: 1px solid var(--line);
    padding: 20px 0 0;
  }

  .lead-story h3 {
    font-size: 27px;
  }

  .bottom-edition {
    flex-wrap: wrap;
    font-size: 7px;
  }
}
</style>
