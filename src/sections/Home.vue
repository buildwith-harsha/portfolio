<template>
  <section class="section home front-page">
    <p class="kicker">Front Page</p>

    <h1 class="headline">
      Turning <span class="emphasis">Business Problems</span><br />
      Into <span class="accent">Digital Solutions</span>
    </h1>

    <p class="deck">
      Building real-world ERP systems, dashboards, and workflows that companies
      actually use every day.
    </p>
  </section>
</template>

<style scoped>
.front-page {
  padding: 80px 40px 100px;
  text-align: center;
}

/* small intro line */
.kicker {
  font-family: var(--font-body);
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 20px;
}

/* main headline */
.headline {
  font-family: var(--font-heading);
  font-size: 76px;
  line-height: 1.05;
  max-width: 900px;
  margin: 0 auto 24px;
}

/* underline emphasis instead of bubbles */
.emphasis {
  font-style: italic;
  border-bottom: 3px solid var(--ink);
}

/* accent word */
.accent {
  color: var(--accent);
}

/* sub-headline (deck) */
.deck {
  font-family: var(--font-body);
  font-size: 18px;
  line-height: 1.6;
  max-width: 620px;
  margin: 0 auto;
  color: var(--muted-ink);
}

/* mobile */
@media (max-width: 768px) {
  .headline {
    font-size: 46px;
  }
}
</style>
