<template>
  <section class="section about feature-article">
    <!-- Section label -->
    <p class="kicker">Feature Story</p>

    <!-- Headline -->
    <h2 class="heading">About the Developer</h2>

    <!-- Byline -->
    <p class="byline">By Harshavardhini Manikandan • Portfolio Edition</p>

    <div class="about-grid">
      <!-- Image column -->
      <figure class="about-img">
        <img
          src="@/assets/harsha_photo.jpg"
          class="Harshavardhini-photo"
        />
        <figcaption>
          The developer behind production-grade systems used in everyday workflows.
        </figcaption>
      </figure>

      <!-- Article column -->
      <div class="about-content">
        <p>
          One year deep into turning
          <span class="highlight">business ideas</span>
          into real-world systems. These ERP platforms didn’t remain concepts —
          they were implemented, evaluated, and used inside organizations for
          day-to-day operations.

          Modules such as <span class="highlight">Payroll</span> and
          <span class="highlight">Kanban</span> became part of routine workflow.
          From story-point calculation and time tracking to performance dashboards,
          the systems gradually began fulfilling their original purpose — measuring,
          organizing, and occasionally revealing more than expected.

          <span class="pull-quote">
            “There’s something addictive about watching a raw idea evolve into
            infrastructure people rely on every day.”
          </span>

          Even the quieter components — cron jobs, queues, and scheduled tasks —
          played a critical role in keeping operations consistent and dependable.
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
  padding: 80px 60px;
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
  margin-bottom: 6px;
  font-family: var(--font-body);
}

/* =========================
   HEADLINE
========================= */
.heading {
  font-family: var(--font-heading);
  font-size: 34px;
  text-align: center;
  margin-bottom: 6px;
}

/* =========================
   BYLINE
========================= */
.byline {
  text-align: center;
  font-size: 12px;
  color: var(--muted-ink);
  font-style: italic;
  margin-bottom: 40px;
}

/* =========================
   GRID LAYOUT
========================= */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 56px;
  align-items: start;
}

/* =========================
   IMAGE
========================= */
.Harshavardhini-photo {
  width: 100%;
  max-width: 240px;
  filter: grayscale(100%) contrast(1.05);
  border: 3px solid var(--ink);
  border-radius: 0;
}

/* Caption */
figcaption {
  margin-top: 6px;
  font-size: 10px;
  font-variant: small-caps;
  letter-spacing: 0.8px;
  color: var(--muted-ink);
  text-align: center;
}

/* =========================
   ARTICLE TEXT
========================= */
.about-content p {
  column-count: 2;
  column-gap: 34px;
  font-size: 14.8px; /* true print scale */
  line-height: 1.85;
  text-align: justify;
  font-family: var(--font-body);
}

/* Drop cap */
.about-content p::first-letter {
  font-family: var(--font-heading);
  font-size: 52px;
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
    transparent 65%,
    rgba(122, 28, 28, 0.08) 65%
  );
  padding: 0 2px;
}

/* =========================
   PULL QUOTE
========================= */
.pull-quote {
  display: block;
  font-family: var(--font-heading);
  font-size: 19px;
  line-height: 1.4;
  margin: 24px 0;
  padding-left: 16px;
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
    font-size: 14.5px;
  }
}
</style>
