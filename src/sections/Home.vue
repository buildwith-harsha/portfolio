<template>
  <section class="section home front-page">
    <!-- Edition line -->
    <p class="edition-line">
      Portfolio Edition • Chennai • 2026
    </p>

    <div class="rule thick"></div>

    <!-- Kicker -->
    <p class="kicker">Front Page</p>

    <!-- Main headline -->
    <h1 class="headline">
      Turning <span class="emphasis">Business Problems</span><br />
      Into <span class="accent">Digital Solutions</span>
    </h1>

    <div class="rule thin"></div>

    <!-- Sub-headline / deck -->
    <p class="deck">
      A developer’s work in building ERP systems, dashboards, and internal
      workflows actively used in real-world business operations.
    </p>
  </section>
</template>

<style scoped>
/* =========================
   FRONT PAGE LAYOUT
========================= */
.front-page {
  padding: 80px 40px 120px;
  text-align: center;
  max-width: 1100px;
  margin: auto;
}

/* =========================
   EDITION LINE
========================= */
.edition-line {
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--muted-ink);
  font-family: var(--font-body);
  margin-bottom: 10px;
}

/* =========================
   KICKER
========================= */
.kicker {
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin: 14px 0;
  font-family: var(--font-body);
}

/* =========================
   HEADLINE
========================= */
.headline {
  font-family: var(--font-heading);
  font-size: 64px; /* print-like scale */
  line-height: 1.05;
  max-width: 900px;
  margin: 0 auto 20px;
}

/* Emphasis underline */
.emphasis {
  font-style: italic;
  border-bottom: 3px solid var(--ink);
}

/* Accent word */
.accent {
  color: var(--accent);
}

/* =========================
   DECK (SUB-HEADLINE)
========================= */
.deck {
  font-family: var(--font-body);
  font-size: 16px;
  line-height: 1.7;
  max-width: 640px;
  margin: 26px auto 0;
  color: var(--muted-ink);
}

/* =========================
   RULES (LINES)
========================= */
.rule {
  margin: 14px auto;
  width: 80%;
}

.rule.thick {
  border-top: 3px solid var(--ink);
}

.rule.thin {
  border-top: 1px solid var(--line);
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 768px) {
  .headline {
    font-size: 42px;
  }

  .deck {
    font-size: 15px;
  }
}
</style>
