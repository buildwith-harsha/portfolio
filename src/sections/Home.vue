<template>
  <section id="home" class="section front-page">
    <!-- Top Editorial Header Wire -->
    <div class="top-wire">
      <div class="wire-left">
        <span class="wire-kicker">FEATURE STORY</span>
        <div class="wire-line"></div>
      </div>
      <div class="wire-right">
        <span>SOFTWARE</span>
        <span class="wire-bullet">•</span>
        <span>PEOPLE</span>
        <span class="wire-bullet">•</span>
        <span>A BETTER TOMORROW</span>
      </div>
    </div>

    <!-- Main Broadsheet Editorial Frame -->
    <div class="broadsheet-frame">
      <!-- 1. LEFT COLUMN: Headline & Story Intro -->
      <article class="hero-story">
        <div>
          <h1 class="hero-headline">
            BEHIND<br />
            EVERY SCREEN,<br />
            <span class="headline-accent">THERE’S A STORY.</span>
          </h1>

          <p class="hero-bio">
            Every digital experience begins with a question, an idea, or a problem waiting to be solved. Behind the interfaces we interact with every day lies a world of creativity, logic, experimentation, and countless lines of code. From the smallest interaction to complex systems, each detail plays a part in turning an idea into something real.
          </p>
        </div>

        <div>
          <p class="hero-byline">
            By Harshavardhini
            <span class="byline-dot">•</span>
            Software Developer
            <span class="byline-dot">•</span>
            Backend, AI &amp; Web
          </p>

          <div class="hero-actions">
            <a href="#projects" class="hero-btn btn-solid">
              VIEW PROJECTS &rarr;
            </a>
            <a href="#contact" class="hero-btn btn-outline">
              GET IN TOUCH
            </a>
          </div>
        </div>
      </article>

      <!-- 2. CENTER COLUMN: Editorial Photo & Cursive Note -->
      <div class="hero-photo-column">
        <div class="photo-container">
          <img
            src="@/assets/harsha_mountain_newsprint.jpg"
            alt="Harsha - Turning Ideas into Impact"
            class="hero-photo"
          />

          <!-- Handwritten note overlay -->
          <div class="handwritten-note">
            <span class="note-line">Better</span>
            <span class="note-line">Systems</span>
            <span class="note-line">Brighter</span>
            <span class="note-line">Tomorrows.</span>
            <div class="note-underline"></div>
          </div>
        </div>
      </div>

      <!-- 3. RIGHT COLUMN: Vertical Dispatch Strip -->
      <aside class="hero-dispatch-strip">
        <div class="strip-top">
          <span>TURNING</span>
          <span>IDEAS</span>
          <span>INTO</span>
          <span>IMPACT</span>
        </div>

        <div class="strip-divider"></div>

        <div class="strip-middle">
          <p>Code.</p>
          <p>Learn.</p>
          <p>Build.</p>
          <p>Improve.</p>
          <p>Repeat.</p>
        </div>

        <div class="strip-bottom">
          <!-- Retro Wireframe Globe -->
          <svg
            class="wireframe-globe"
            viewBox="0 0 64 64"
            fill="none"
            stroke="currentColor"
            xmlns="http://www.w3.org/2000/svg"
          >
            <!-- Outer circle -->
            <ellipse cx="32" cy="32" rx="27" ry="27" stroke-width="1.1" />
            <!-- Latitudes -->
            <ellipse cx="32" cy="32" rx="27" ry="11" stroke-width="0.9" />
            <ellipse cx="32" cy="20" rx="23" ry="7" stroke-width="0.8" stroke-dasharray="1 1" />
            <ellipse cx="32" cy="44" rx="23" ry="7" stroke-width="0.8" stroke-dasharray="1 1" />
            <!-- Longitudes -->
            <ellipse cx="32" cy="32" rx="12" ry="27" stroke-width="0.9" />
            <!-- Equator & Meridian -->
            <line x1="5" y1="32" x2="59" y2="32" stroke-width="0.8" />
            <line x1="32" y1="5" x2="32" y2="59" stroke-width="0.8" />
          </svg>

          <!-- Triple engraved linocut rules -->
          <div class="engraved-marks">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>
      </aside>
    </div>
  </section>
</template>

<style scoped>
/* =========================
   PAGE CONTAINER
========================= */
.front-page {
  max-width: 1240px;
  margin: 0 auto;
  padding: 24px 40px 60px;
}

/* =========================
   TOP EDITORIAL WIRE
========================= */
.top-wire {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  margin-bottom: 12px;
}

.wire-left {
  display: flex;
  align-items: center;
  gap: 14px;
  flex: 1;
}

.wire-kicker {
  font-family: var(--font-heading);
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: var(--accent);
  white-space: nowrap;
}

.wire-line {
  height: 1px;
  background: var(--line);
  flex: 1;
}

.wire-right {
  font-family: var(--font-body);
  font-size: 10.5px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--muted-ink);
  white-space: nowrap;
  display: flex;
  align-items: center;
  gap: 10px;
}

.wire-bullet {
  font-size: 8px;
  opacity: 0.6;
}

/* =========================
   BROADSHEET FRAME
========================= */
.broadsheet-frame {
  border: 1px solid var(--line);
  display: grid;
  grid-template-columns: 1.25fr 0.85fr 0.22fr;
  align-items: stretch;
  background: var(--paper);
}

/* =========================
   1. HERO STORY (LEFT)
========================= */
.hero-story {
  padding: 44px 40px 38px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 460px;
}

.hero-headline {
  font-family: var(--font-heading);
  font-size: clamp(34px, 3.8vw, 54px);
  font-weight: 900;
  line-height: 1.04;
  letter-spacing: -1.2px;
  text-transform: uppercase;
  color: var(--ink);
  margin-bottom: 24px;
}

.headline-accent {
  color: var(--accent);
  font-style: italic;
  font-weight: 900;
  display: inline-block;
}

.hero-bio {
  font-family: var(--font-body);
  font-size: 15px;
  line-height: 1.75;
  color: var(--ink);
  margin-bottom: 26px;
  max-width: 100%;
  text-align: justify;
  text-justify: inter-word;
  hyphens: auto;
}

.hero-byline {
  font-family: var(--font-body);
  font-size: 12.5px;
  color: var(--muted-ink);
  margin-bottom: 28px;
  display: flex;
  align-items: center;
  gap: 8px;
  flex-wrap: wrap;
}

.byline-dot {
  opacity: 0.6;
}

.hero-actions {
  display: flex;
  gap: 16px;
  align-items: center;
  flex-wrap: wrap;
}

.hero-btn {
  font-family: var(--font-heading);
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 12px 24px;
  text-decoration: none;
  display: inline-block;
  transition: all 0.2s ease;
  white-space: nowrap;
}

.btn-solid {
  background: var(--accent);
  color: #fff;
  border: 1px solid var(--accent);
  box-shadow: 0 2px 8px rgba(122, 28, 28, 0.15);
}

.btn-solid:hover {
  background: #5d1515;
  border-color: #5d1515;
  color: #fff;
}

.btn-outline {
  background: transparent;
  color: var(--ink);
  border: 1px solid var(--ink);
}

.btn-outline:hover {
  background: var(--ink);
  color: var(--paper);
}

/* =========================
   2. HERO PHOTO (CENTER)
========================= */
.hero-photo-column {
  position: relative;
  display: flex;
  align-items: stretch;
  border-left: 1px solid var(--line);
  padding: 16px;
  background: var(--paper);
}

.photo-container {
  position: relative;
  width: 100%;
  height: 100%;
  min-height: 480px;
  border: 1px solid rgba(38, 33, 28, 0.4);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
  overflow: hidden;
  background: #fdfbf7;
}

.hero-photo {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 60%;
  display: block;
  border: 0;
  filter: grayscale(100%) contrast(1.15) brightness(0.97);
  mix-blend-mode: multiply;
}

/* Handwritten Cursive Note */
.handwritten-note {
  position: absolute;
  top: 24px;
  left: 22px;
  z-index: 2;
  font-family: var(--font-handwriting);
  font-size: 24px;
  line-height: 1.22;
  color: #231c16;
  transform: rotate(-6.5deg);
  text-shadow: 0 1px 1px rgba(255, 255, 255, 0.5);
  display: flex;
  flex-direction: column;
  pointer-events: none;
  letter-spacing: 0.3px;
}

.note-underline {
  width: 88px;
  height: 2px;
  background: #231c16;
  margin-top: 5px;
  transform: rotate(1deg);
  opacity: 0.85;
  border-radius: 1px;
}

/* =========================
   3. DISPATCH STRIP (RIGHT)
========================= */
.hero-dispatch-strip {
  border-left: 1px solid var(--line);
  padding: 26px 14px 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}

.strip-top {
  display: flex;
  flex-direction: column;
  gap: 5px;
  font-family: var(--font-heading);
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 2.2px;
  text-transform: uppercase;
  color: var(--muted-ink);
}

.strip-divider {
  width: 1px;
  height: 38px;
  background: var(--line);
  margin: 16px 0;
  opacity: 0.7;
}

.strip-middle {
  font-family: var(--font-body);
  font-size: 11px;
  line-height: 1.7;
  color: var(--muted-ink);
}

.strip-middle p {
  text-align: center;
  font-size: 11px;
  color: var(--muted-ink);
}

.strip-bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
  margin-top: auto;
  padding-top: 18px;
}

.wireframe-globe {
  width: 44px;
  height: 44px;
  color: var(--ink);
  transform: rotate(-10deg);
}

.engraved-marks {
  display: flex;
  flex-direction: column;
  gap: 2.5px;
  width: 38px;
}

.engraved-marks span {
  height: 1px;
  background: var(--line);
  width: 100%;
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 1040px) {
  .broadsheet-frame {
    grid-template-columns: 1fr 1fr;
  }

  .hero-dispatch-strip {
    display: none;
  }

  .hero-story {
    padding: 32px 28px;
  }
}

@media (max-width: 768px) {
  .front-page {
    padding: 16px 20px 40px;
  }

  .top-wire {
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
  }

  .wire-line {
    display: none;
  }

  .broadsheet-frame {
    grid-template-columns: 1fr;
  }

  .hero-photo-column {
    border-left: 0;
    border-top: 1px solid var(--line);
    min-height: 320px;
  }

  .hero-story {
    min-height: auto;
    padding: 28px 20px;
  }

  .hero-headline {
    font-size: 32px;
  }
}
</style>
