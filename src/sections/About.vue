<template>
  <section class="section about feature-article">
    <p class="kicker">Feature Story</p>

    <h2 class="heading">About the Developer</h2>

    <p class="byline">By Harshavardhini • Portfolio Edition</p>

    <div class="about-grid">
      <div class="poster-wrapper">
        <div class="wanted-poster">
          <div class="poster-header">
            <span class="wanted-label">WANTED</span>
          </div>

          <div class="poster-photo-frame">
            <img src="@/assets/harsha_photo.jpeg" class="poster-photo" alt="Harshavardhini" />
          </div>

          <p class="poster-alias">"The Full-Stack Outlaw"</p>

          <div class="poster-rule"></div>

          <p class="poster-charges">
            FOR: Wild ideas, suspiciously good code, unruly bugs &amp; first-degree innovation
          </p>

          <div class="poster-rule"></div>

          <div class="poster-reward-block">
            <span class="reward-label">REWARD</span>
            <span class="reward-amount">$10,000</span>
            <span class="reward-sub">or a full-time offer</span>
          </div>

          <p class="poster-footer">By order of the Dev Community • Chennai, 2026</p>
        </div>
      </div>

      <div class="about-content">
        <p>
          Two years into turning caffeine, curiosity, and questionable sleep schedules into working
          software, this developer has entered a new territory: the
          <span class="highlight">Nike-inspired Sneaker Design Studio</span> — where sneakers get
          makeovers and boring footwear gets a serious upgrade. Armed with interactive 3D visuals
          and an alarming number of color combinations, users can customize their dream kicks
          without spending a fortune on a pair they might regret by Monday.

          <span class="pull-quote">
            “Give a developer a sneaker, and they'll wear it. Give them a color picker, and they'll
            redesign the entire shoe industry.”
          </span>

          After two years of building digital experiences, the mission remains the same: turn wild
          ideas into working products, make interfaces feel less like homework, and send stubborn
          bugs running for the hills. No sneakers were harmed in the making of this project. A few
          bugs, however, were absolutely hunted down.
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
   POSTER WRAPPER
========================= */
.poster-wrapper {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: flex-start;
}

/* Hidden SVG that defines the crumple filter */
.crumple-filter {
  position: absolute;
  width: 0;
  height: 0;
  overflow: hidden;
}

/* Vintage wanted poster */

/* Dark printed masthead */

/* Portrait like a historic woodcut */

.poster-photo {
  width: 100%;
  aspect-ratio: 4 / 5;
  object-fit: cover;
  display: block;
  border: 0;

  filter: grayscale(1) sepia(0.75) contrast(1.35) brightness(0.86);

  mix-blend-mode: multiply;
}

/* Alias and charges */
.poster-alias {
  margin: 10px 0;
  font-family: var(--font-heading);
  font-size: 14px;
  font-weight: 700;
  font-style: italic;
  letter-spacing: 0.5px;
  color: var(--poster-ink);
}

.poster-rule {
  border-top: 2px solid var(--poster-ink);
  margin: 12px 3px;
}

.poster-charges {
  max-width: 270px;
  margin: 0 auto;
  padding: 5px;
  font-size: 10px;
  line-height: 1.8;
  font-weight: 700;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  color: var(--poster-ink);
}

/* Reward: retain your portfolio's burgundy accent */
.poster-reward-block {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 14px 0 8px;
}

.reward-label {
  font-size: 12px;
  font-weight: 900;
  letter-spacing: 5px;
  color: var(--poster-ink);
}

.reward-amount {
  margin: 3px 0;
  font-family: var(--font-heading);
  font-size: clamp(27px, 4vw, 36px);
  font-weight: 900;
  letter-spacing: 1px;
  line-height: 1.15;
  color: var(--accent);
}
.wanted-poster {
  --poster-paper: var(--paper);
  --poster-ink: var(--ink);

  position: relative;
  width: 100%;
  max-width: 370px;
  padding: 24px 22px 20px;
  color: var(--poster-ink);
  text-align: center;
  font-family: var(--font-heading);

  /* Exact same background color as the portfolio */
  background: var(--paper);

  border: 2px solid var(--line);
  outline: 1px solid var(--line);
  outline-offset: -8px;

  box-shadow: 0 8px 20px rgba(38, 33, 28, 0.1);

  clip-path: polygon(
    2% 1%,
    12% 2%,
    23% 0%,
    35% 2%,
    49% 1%,
    63% 2%,
    78% 0%,
    98% 2%,
    99% 15%,
    97% 29%,
    100% 43%,
    98% 58%,
    100% 73%,
    98% 88%,
    100% 98%,
    84% 99%,
    70% 98%,
    53% 100%,
    37% 98%,
    21% 100%,
    2% 98%,
    1% 84%,
    3% 68%,
    1% 53%,
    2% 36%,
    0% 20%
  );
}
.reward-sub {
  font-size: 10px;
  font-style: italic;
  color: var(--poster-ink);
}

.poster-footer {
  margin-top: 15px;
  font-size: 8px;
  line-height: 1.7;
  letter-spacing: 0.6px;
  text-align: center;
  color: var(--poster-ink);
  text-transform: uppercase;
}

@media (max-width: 768px) {
  .wanted-poster {
    max-width: 340px;
    padding: 22px 18px;
  }

  .wanted-label {
    font-size: 30px;
  }
}

/* =========================
   POSTER HEADER BAND
========================= */
.poster-header {
  background: transparent;
  margin: -14px -14px 10px;
  padding: 8px;
  border-top: 4px double var(--line);
  border-bottom: 4px double var(--line);
}

.wanted-label {
  font-family: var(--font-heading);
  font-size: 38px;
  font-weight: 900;
  letter-spacing: 5px;
  color: var(--ink);
  text-transform: uppercase;
}

.poster-alias {
  margin: 6px 0;
  font-size: 11px;
  color: var(--ink);
}

.poster-rule {
  border-top: 1px solid var(--line);
  margin: 7px 3px;
}

.poster-charges {
  max-width: 270px;
  margin: 0 auto;
  padding: 3px;
  font-size: 9px;
  line-height: 1.5;
  color: var(--ink);
}

.poster-reward-block {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 8px 0 4px;
}

.reward-label {
  font-size: 11px;
  letter-spacing: 4px;
  color: var(--ink);
}

.reward-amount {
  font-size: 28px;
  line-height: 1.1;
  color: var(--accent);
}

.reward-sub {
  font-size: 9px;
  color: var(--muted-ink);
}

.poster-footer {
  margin-top: 8px;
  font-size: 8px;
  line-height: 1.5;
  color: var(--muted-ink);
}

/* =========================
   PHOTO FRAME
========================= */
.poster-photo-frame {
  width: 55%;
  max-width: 150px;
  margin: 4px auto 10px;
  padding: 3px;
  overflow: hidden;
  border: 2px solid var(--line);
  box-shadow: inset 0 0 0 1px var(--paper);
}

.poster-photo {
  width: 100%;
  height: 155px;
  object-fit: cover;
  object-position: center 35%;
  display: block;
  border: none;
  filter: grayscale(100%) sepia(25%) contrast(1.1);
  mix-blend-mode: multiply;
}

/* =========================
   POSTER TYPOGRAPHY
========================= */
.poster-name {
  font-family: var(--font-heading);
  font-size: 19px;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  line-height: 1.2;
  margin: 8px 0 4px;
  color: #1e1206;
  text-align: center;
}

.poster-alias {
  font-family: var(--font-body);
  font-size: 11px;
  font-style: italic;
  color: #5a3e10;
  margin-bottom: 8px;
  text-align: center;
}

.poster-rule {
  border-top: 1.5px solid #3b2a0a;
  margin: 8px 4px;
}

.poster-charges {
  font-family: var(--font-body);
  font-size: 10px;
  line-height: 1.55;
  text-align: center;
  color: #3b2a0a;
  padding: 4px 6px;
  text-transform: uppercase;
  letter-spacing: 0.4px;
}

/* =========================
   REWARD BLOCK
========================= */
.poster-reward-block {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 8px 0 4px;
}

.reward-label {
  font-family: var(--font-heading);
  font-size: 13px;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: #3b2a0a;
}

.reward-amount {
  font-family: var(--font-heading);
  font-size: 32px;
  font-weight: 900;
  letter-spacing: 2px;
  color: #7a1c1c;
  /* subtle letterpress indent */
  text-shadow: 1px 1px 0 rgba(0, 0, 0, 0.25);
  line-height: 1.1;
}

.reward-sub {
  font-family: var(--font-body);
  font-size: 9.5px;
  font-style: italic;
  color: #5a3e10;
  margin-top: 2px;
}

/* =========================
   POSTER FOOTER
========================= */
.poster-footer {
  font-family: var(--font-body);
  font-size: 8.5px;
  text-align: center;
  color: #7a6030;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  margin-top: 10px;
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
  background: linear-gradient(to bottom, transparent 65%, rgba(122, 28, 28, 0.08) 65%);
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
