<template>
  <section class="section about feature-article">
    <h2 class="heading">About the Developer</h2>

    <p class="byline">By Harshavardhini • Portfolio Edition</p>

    <div class="about-grid">
      <!-- 1. LEFT COLUMN: Editorial Staff Portrait -->
      <div class="portrait-wrapper">
        <figure class="editorial-portrait">
          <div class="portrait-frame">
            <img
              src="@/assets/harsha_portrait.png"
              class="portrait-photo"
              alt="Harshavardhini - Software Developer"
            />
          </div>

          <figcaption class="portrait-caption">
            <span class="caption-name">HARSHAVARDHINI</span>
            <div class="caption-divider"></div>
            <p class="caption-role">Software Developer &bull; Chennai, India</p>
            <p class="caption-note">Backend &bull; AI &bull; Web Systems</p>
          </figcaption>
        </figure>
      </div>

      <!-- 2. RIGHT COLUMN: Dramatic Story Broadsheet Article -->
      <article class="about-content">
        <p class="story-lead">
          <span class="drop-cap">I</span>t begins not in silence, but in the relentless hum of logic gates, terminal logs, and late-night curiosity. Harshavardhini did not merely stumble into software engineering—she arrived with an engineer’s appetite for breaking down monolithic problems into elegant, synchronized systems. From her engineering roots in Tamil Nadu to architecting enterprise-scale applications in Chennai at T Cube, her journey has been driven by a single obsession: bridging the invisible chasm between complex business logic and fluid, human-first digital experiences.
        </p>

        <p>
          Today, her trajectory points toward the cutting edge—modern frontend architecture, scalable cloud systems, and AI-assisted digital products. In a world crowded with hasty prototypes, Harsha builds systems designed to endure: fast, resilient, and deeply purposeful. Because behind every screen, every API contract, and every deploy pipeline... there is always a story worth engineering to perfection.
        </p>

        <blockquote class="pull-quote">
          “Code is never just syntax on a dark screen—it is the invisible architecture that decides whether a person’s workday feels like an uphill struggle or effortless momentum.”
        </blockquote>

        <!-- Archival Verification Stamp -->
        <div class="vintage-stamp" aria-hidden="true">
          <div class="stamp-ring">
            <span class="stamp-org">EDITORIAL DISPATCH</span>
            <span class="stamp-icon">★ 2026 ★</span>
            <span class="stamp-status">PASSED FOR RECORD</span>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  if (typeof window !== 'undefined' && 'IntersectionObserver' in window) {
    // Portrait plate smooth entry
    gsap.from('.portrait-wrapper', {
      x: -20,
      opacity: 0,
      duration: 0.7,
      ease: 'power2.out',
      scrollTrigger: {
        trigger: '.about-grid',
        start: 'top 85%',
        once: true,
      },
    })

    // Story article text staggered entry
    gsap.from('.about-content > *', {
      y: 18,
      opacity: 0,
      stagger: 0.08,
      duration: 0.55,
      ease: 'power2.out',
      scrollTrigger: {
        trigger: '.about-content',
        start: 'top 85%',
        once: true,
      },
    })
  }
})
</script>

<style scoped>
/* =========================
   SECTION WRAPPER
========================= */
.feature-article {
  padding: 80px 60px 44px;
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
  padding: 14px 0 12px;
  margin-bottom: 14px;
  width: 100%;
  box-sizing: border-box;
}

/* =========================
   BYLINE
========================= */
.byline {
  text-align: center;
  font-size: 12px;
  color: var(--muted-ink);
  font-style: italic;
  margin-bottom: 36px;
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
   EDITORIAL PORTRAIT
========================= */
.portrait-wrapper {
  display: flex;
  justify-content: center;
  align-items: flex-start;
}

.editorial-portrait {
  width: 100%;
  max-width: 360px;
  background: var(--paper);
  border: 1px solid var(--line);
  padding: 14px 14px 18px;
  box-shadow: 0 4px 16px rgba(38, 33, 28, 0.06);
  margin: 0;
}

.portrait-frame {
  position: relative;
  width: 100%;
  aspect-ratio: 1 / 1;
  overflow: hidden;
  border: 1px solid var(--line);
  background: #fdfbf7;
}

.portrait-photo {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 20%;
  display: block;
}

.portrait-caption {
  margin-top: 14px;
  text-align: center;
}

.caption-name {
  display: block;
  font-family: var(--font-heading);
  font-size: 14px;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--ink);
}

.caption-divider {
  width: 36px;
  height: 1px;
  background: var(--line);
  margin: 8px auto;
  opacity: 0.7;
}

.caption-role {
  font-family: var(--font-body);
  font-size: 11.5px;
  font-style: italic;
  color: var(--muted-ink);
  text-align: center;
  margin: 0;
}

.caption-note {
  font-family: var(--font-body);
  font-size: 10.5px;
  color: var(--muted-ink);
  text-align: center;
  margin-top: 4px;
  letter-spacing: 0.3px;
}

/* =========================
   ARTICLE TEXT (BROADSHEET)
========================= */
.about-content {
  column-count: 2;
  column-gap: 36px;
  font-family: var(--font-body);
}

.about-content p {
  font-size: 14.6px;
  line-height: 1.82;
  text-align: justify;
  text-justify: inter-word;
  color: var(--ink);
  margin-bottom: 16px;
  hyphens: auto;
}

/* Authentic editorial drop-cap */
.drop-cap {
  font-family: var(--font-heading);
  font-size: 54px;
  line-height: 0.85;
  float: left;
  margin: 6px 12px 0 0;
  font-weight: 900;
  color: var(--ink);
}

/* Highlights */
.highlight {
  background: linear-gradient(to bottom, transparent 65%, rgba(122, 28, 28, 0.12) 65%);
  font-weight: 700;
  color: var(--ink);
  padding: 0 2px;
}

/* Pull quote */
.pull-quote {
  column-span: all;
  margin: 22px 0 20px;
  padding: 16px 20px 16px 22px;
  border-left: 3px solid var(--accent);
  background: rgba(122, 28, 28, 0.035);
  font-family: var(--font-heading);
  font-size: 17.5px;
  font-style: italic;
  font-weight: 700;
  line-height: 1.45;
  color: var(--ink);
  letter-spacing: 0.2px;
  border-top: 1px dashed rgba(44, 40, 37, 0.2);
  border-bottom: 1px dashed rgba(44, 40, 37, 0.2);
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 900px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .editorial-portrait {
    max-width: 320px;
    margin: 0 auto;
  }

  .about-content {
    column-count: 1;
  }
}

@media (max-width: 768px) {
  .feature-article {
    padding: 60px 24px;
  }

  .about-content p {
    font-size: 14.5px;
  }
}

/* =========================
   VINTAGE RUBBER STAMP
========================= */
.vintage-stamp {
  display: inline-block;
  margin-top: 32px;
  padding: 10px 18px;
  border: 2px dashed rgba(122, 28, 28, 0.75);
  border-radius: 4px;
  transform: rotate(-3.5deg);
  font-family: var(--font-heading);
  color: var(--accent);
  text-align: center;
  transition: transform 0.35s ease, border-color 0.35s ease;
  cursor: default;
  user-select: none;
}

.vintage-stamp:hover {
  transform: rotate(0deg) scale(1.04);
  border-color: var(--accent);
}

.stamp-ring {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2px;
}

.stamp-org {
  font-size: 9px;
  letter-spacing: 2px;
  text-transform: uppercase;
  font-weight: 700;
}

.stamp-icon {
  font-size: 10px;
  letter-spacing: 3px;
  color: var(--accent);
}

.stamp-status {
  font-size: 8.5px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}
</style>
