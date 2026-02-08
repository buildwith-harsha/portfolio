<template>
  <section class="section about feature-article">
    <!-- Section label -->
    <p class="kicker">Feature Story</p>

    <!-- Headline -->
    <h2 class="heading">About Me</h2>

    <div class="about-grid">
      <!-- Image column -->
      <figure class="about-img">
        <img
          src="@/assets/harsha_photo.jpg"
          class="Harshavardhini-photo"
        />
        <figcaption>
          Designing and maintaining systems used in real-world workflows.
        </figcaption>

      </figure>

      <!-- Article column -->
      <div class="about-content">
        <p>
          One year deep into turning
          <span class="highlight">business fantasies</span>
          into reality. These ERP systems didn’t just stay as ideas — they were
          actually implemented and used inside the company for real evaluation
          and tracking.

          Modules like <span class="highlight">Payroll</span> and
          <span class="highlight">Kanban</span> became part of everyday workflow.
          From story point calculation and time scoring to employee performance
          dashboards, the system slowly started doing what it was built for —
          measuring, tracking, and sometimes even exposing a little too much.

          <span class="pull-quote">
            “There’s something addictive about watching a raw idea evolve into a
            system people depend on every single day.”
          </span>

          Even the quiet workers in the background — cron jobs and scheduled
          tasks — played a big role in keeping everything running smoothly.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* =========================
   SECTION WRAPPER
========================= */
.feature-article {
  padding: 90px 60px;
}

/* =========================
   KICKER
========================= */
.kicker {
  text-align: center;
  font-size: 11px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 8px;
  font-family: var(--font-body);
}

/* =========================
   HEADLINE
========================= */
.heading {
  font-family: var(--font-heading);
  font-size: 38px;
  text-align: center;
  margin-bottom: 40px;
}

/* =========================
   GRID LAYOUT
========================= */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 60px;
  align-items: start;
}

/* =========================
   IMAGE
========================= */
.Harshavardhini-photo {
  width: 100%;
  max-width: 250px;
  filter: grayscale(100%);
  border-radius: 0;
}


figcaption {
  font-size: 10px;
  font-variant: small-caps;
  letter-spacing: 0.8px;
  font-style: italic;
  color: var(--muted-ink);
  font-style: italic;
}


/* =========================
   ARTICLE TEXT
========================= */
.about-content p {
  column-count: 2;
  column-gap: 36px;
  font-size: 15.5px; /* authentic newspaper size */
  line-height: 1.75;
  text-align: justify;
  font-family: var(--font-body);
}

/* Drop cap */
.about-content p::first-letter {
  font-family: var(--font-heading);
  font-size: 56px;
  float: left;
  line-height: 0.9;
  margin: 6px 12px 0 0;
}

/* =========================
   SUBTLE HIGHLIGHTS
========================= */
.highlight {
  background: linear-gradient(
    to bottom,
    transparent 60%,
    rgba(139, 0, 0, 0.12) 60%
  );
  padding: 0 2px;
}

/* =========================
   PULL QUOTE
========================= */
.pull-quote {
  display: block;
  font-family: var(--font-heading);
  font-size: 20px;
  line-height: 1.4;
  margin: 26px 0;
  padding-left: 18px;
  border-left: 3px solid var(--ink);
  column-span: all;
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 768px) {
  .about-grid {
    grid-template-columns: 1fr;
  }

  .about-content p {
    column-count: 1;
    font-size: 15px;
  }
}
</style>
