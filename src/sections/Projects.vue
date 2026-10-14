<template>
  <section class="section projects-page">
    <!-- Standardized Section Banner -->
    <h2 class="heading">Project Chronicle</h2>

    <!-- Main broadsheet grid -->
    <div class="broadsheet-grid">
      <!-- ===================== LEAD FEATURE (2/3 width) ===================== -->
      <div class="lead-column">
        <!-- Lead article: Sneaker Design Studio -->
        <article class="lead-article">
          <!-- Overline label -->
          <p class="article-kicker">★ Featured Project • Live on the Web</p>

          <!-- Headline -->
          <h3 class="lead-headline">
            The Sneaker Design Studio:<br />
            A Canvas That Moves
          </h3>

          <div class="lead-rule"></div>

          <!-- Lead article body — two-column newspaper layout -->
          <div class="lead-body">
            <p>
              <span class="drop-cap">I</span>n a marketplace saturated with static product pages,
              the
              <span class="text-emphasis">Sneaker Design Studio</span>
              arrives as something altogether different — a browser-based creative tool that places
              the power of customisation directly in the hands of the customer.
            </p>
            <p>
              Built entirely on the open web with Vue and Three.js, the studio renders a
              <span class="text-emphasis">real-time 3D sneaker</span>
              that responds instantly to colour pickers, material selectors, and part-by-part
              editing controls. Each stroke of interaction is met with immediate visual feedback —
              no page reloads, no waiting.
            </p>
            <p>
              The architecture behind the experience is deliberately lean. A reactive state layer
              propagates changes across the scene graph, keeping the renderer in perfect sync with
              user intent at all times. The result is a workflow that feels less like configuring a
              product and more like sketching on a live canvas.
            </p>

            <!-- Pull quote -->
            <blockquote class="newspaper-pull-quote">
              "What began as a technical exercise in WebGL became something customers actually want
              to spend time inside."
            </blockquote>

            <p>
              The application is deployed on Vercel and performs at production speed without
              compromise. It stands as evidence that immersive, interactive commerce experiences are
              no longer the exclusive territory of native apps — the browser is ready.
            </p>
          </div>

          <!-- Live demo link — styled as a newspaper classified notice -->
          <div class="demo-notice">
            <span class="demo-label">▸ LIVE EDITION</span>
            <a
              href="https://sneaker-design-studio.vercel.app/"
              target="_blank"
              rel="noopener"
              class="demo-link"
            >
              sneaker-design-studio.vercel.app
            </a>
            <span class="demo-tag">Interactive Demo Available</span>
          </div>
        </article>

        <!-- Secondary article: HR Management System -->
        <article class="secondary-article">
          <div class="rule thin-rule"></div>
          <p class="article-kicker">Enterprise Systems</p>
          <h3 class="secondary-headline">HR Management System</h3>
          <p class="article-byline">Laravel &bull; Vue.js &bull; Internal ERP Platform</p>
          <p class="article-body">
            A full-scale internal ERP platform covering payroll, attendance, employee performance
            dashboards, and operational reporting — built with Laravel and Vue, deployed and
            actively used in daily organisational workflows. Modules include story-point
            calculation, time tracking, and live performance metrics.
          </p>
        </article>
      </div>

      <!-- ===================== SIDE DISPATCHES (1/3 width) ===================== -->
      <aside class="dispatch-column">
        <!-- Vertical rule -->
        <div class="column-rule"></div>

        <!-- Dispatch: College Management System -->
        <div class="dispatch-card">
          <p class="dispatch-overline">Academic Systems</p>
          <h4 class="dispatch-headline">College Management System</h4>
          <div class="dispatch-rule"></div>
          <p class="dispatch-body">
            An academic management system handling student records, course administration,
            attendance tracking, and institutional workflows. Built with Laravel; serves as the
            operational backbone for multi-department academic oversight.
          </p>
          <p class="dispatch-stack">Stack: Laravel &bull; MySQL &bull; Blade</p>
        </div>

        <div class="dispatch-divider"></div>

        <!-- Dispatch: Kanban & Workflow Tracker -->
        <div class="dispatch-card">
          <p class="dispatch-overline">Productivity Tools</p>
          <h4 class="dispatch-headline">Kanban &amp; Workflow Tracker</h4>
          <div class="dispatch-rule"></div>
          <p class="dispatch-body">
            A story-point–driven Kanban board created to measure productivity, timelines, and team
            performance. Supports real-world project tracking with role-based views and automated
            reporting — revealing more than spreadsheets ever could.
          </p>
          <p class="dispatch-stack">Stack: Vue.js &bull; Laravel &bull; WebSockets</p>
        </div>

        <div class="dispatch-divider"></div>

        <!-- Brief notice box -->
        <div class="notice-box">
          <p class="notice-title">Developer on Record</p>
          <p class="notice-body">
            All systems listed above were shipped to production and remain in active use inside real
            organisations. Available for new commissions.
          </p>
        </div>
      </aside>
    </div>
  </section>
</template>

<style scoped>
/* =========================
   SECTION WRAPPER
========================= */
.projects-page {
  padding: 60px 60px 30px;
  max-width: 1200px;
  margin: auto;
}

/* =========================
   HEADLINE
========================= */
.heading {
  font-family: var(--font-heading);
  font-size: 40px;
  font-weight: 700;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 4px;
  line-height: 1.1;
  color: var(--ink);
  border-top: 2px solid var(--ink);
  border-bottom: 2px solid var(--ink);
  padding: 14px 0 12px;
  margin-bottom: 14px;
  width: 100%;
  box-sizing: border-box;
}

.thin-rule {
  border-top: 1px solid var(--line);
  margin: 18px 0;
}

/* =========================
   BROADSHEET GRID
========================= */
.broadsheet-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 0 48px;
  margin-top: 36px;
  align-items: start;
}

/* =========================
   LEAD COLUMN
========================= */
.lead-column {
  border-right: 1px solid var(--line);
  padding-right: 48px;
}

/* =========================
   LEAD ARTICLE
========================= */
.lead-article {
  margin-bottom: 0;
}

.article-kicker {
  font-family: var(--font-body);
  font-size: 10px;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 8px;
  text-align: left;
}

.lead-headline {
  font-family: var(--font-heading);
  font-size: 38px;
  line-height: 1.1;
  letter-spacing: 0.5px;
  margin-bottom: 6px;
  font-weight: 700;
  color: var(--ink);
}

.article-byline {
  font-family: var(--font-body);
  font-size: 11px;
  font-style: italic;
  color: var(--muted-ink);
  text-align: left;
  margin-bottom: 0;
}

.lead-rule {
  border-top: 1px solid var(--line);
  margin: 12px 0;
}

/* Lead body: 2-column newspaper text */
.lead-body {
  column-count: 2;
  column-gap: 30px;
}

.lead-body p {
  font-family: var(--font-body);
  font-size: 14px;
  line-height: 1.85;
  text-align: justify;
  color: var(--ink);
  margin-bottom: 14px;
  break-inside: avoid;
}

/* Drop cap */
.drop-cap {
  float: left;
  font-family: var(--font-heading);
  font-size: 58px;
  line-height: 0.82;
  margin: 4px 8px 0 0;
  color: var(--ink);
}

.text-emphasis {
  font-style: italic;
  font-weight: 600;
}

/* Pull quote — spans both columns */
.newspaper-pull-quote {
  column-span: all;
  font-family: var(--font-heading);
  font-size: 18px;
  line-height: 1.5;
  border-top: 2px solid var(--ink);
  border-bottom: 2px solid var(--ink);
  padding: 12px 4px;
  margin: 16px 0;
  text-align: center;
  font-style: italic;
  color: var(--ink);
}

/* =========================
   LIVE DEMO NOTICE
========================= */
.demo-notice {
  column-span: all;
  display: flex;
  align-items: center;
  gap: 10px;
  flex-wrap: wrap;
  background: var(--ink);
  color: var(--paper);
  padding: 10px 16px;
  margin-top: 18px;
  font-family: var(--font-body);
}

.demo-label {
  font-size: 9px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--paper);
  opacity: 0.75;
  white-space: nowrap;
}

.demo-link {
  font-family: var(--font-heading);
  font-size: 15px;
  font-style: italic;
  color: #f5e6c0;
  text-decoration: underline;
  letter-spacing: 0.3px;
  transition: opacity 0.2s;
}

.demo-link:hover {
  opacity: 0.75;
}

.demo-tag {
  font-size: 9px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--paper);
  opacity: 0.6;
  margin-left: auto;
}

/* =========================
   SECONDARY ARTICLE
========================= */
.secondary-article {
  margin-top: 30px;
}

.secondary-headline {
  font-family: var(--font-heading);
  font-size: 22px;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin: 4px 0 6px;
  color: var(--ink);
}

.article-body {
  font-family: var(--font-body);
  font-size: 13.5px;
  line-height: 1.8;
  text-align: justify;
  color: var(--muted-ink);
}

/* =========================
   DISPATCH COLUMN (SIDEBAR)
========================= */
.dispatch-column {
  position: relative;
  padding-left: 0;
}

.column-rule {
  display: none; /* visual rule is achieved via border-right on lead-column */
}

.dispatch-card {
  margin-bottom: 0;
}

.dispatch-overline {
  font-family: var(--font-body);
  font-size: 9.5px;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 4px;
}

.dispatch-headline {
  font-family: var(--font-heading);
  font-size: 20px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  line-height: 1.15;
  color: var(--ink);
  margin-bottom: 0;
}

.dispatch-rule {
  border-top: 1px solid var(--line);
  margin: 8px 0;
}

.dispatch-body {
  font-family: var(--font-body);
  font-size: 13px;
  line-height: 1.8;
  text-align: justify;
  color: var(--muted-ink);
  margin-bottom: 6px;
}

.dispatch-stack {
  font-family: var(--font-body);
  font-size: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--muted-ink);
  font-style: italic;
  margin-top: 4px;
}

.dispatch-divider {
  border-top: 1px solid var(--line);
  margin: 20px 0;
}

/* =========================
   NOTICE BOX (CLASSIFIED-STYLE)
========================= */
.notice-box {
  border: 1.5px solid var(--ink);
  padding: 14px 14px 12px;
  margin-top: 4px;
  text-align: center;
}

.notice-title {
  font-family: var(--font-heading);
  font-size: 13px;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 8px;
  color: var(--ink);
}

.notice-body {
  font-family: var(--font-body);
  font-size: 12px;
  line-height: 1.7;
  text-align: center;
  color: var(--muted-ink);
  font-style: italic;
}

/* =========================
   BOTTOM RULE
========================= */
.bottom-rule {
  margin-top: 40px;
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 900px) {
  .projects-page {
    padding: 40px 24px 60px;
  }

  .broadsheet-grid {
    grid-template-columns: 1fr;
    gap: 0;
  }

  .lead-column {
    border-right: none;
    padding-right: 0;
  }

  .lead-body {
    column-count: 1;
  }

  .section-banner {
    font-size: 36px;
    letter-spacing: 3px;
  }

  .dispatch-column {
    border-top: 2px solid var(--ink);
    margin-top: 32px;
    padding-top: 24px;
  }
}

@media (max-width: 480px) {
  .section-banner {
    font-size: 28px;
  }

  .lead-headline {
    font-size: 28px;
  }

  .demo-notice {
    flex-direction: column;
    align-items: flex-start;
    gap: 6px;
  }

  .demo-tag {
    margin-left: 0;
  }
}
</style>
