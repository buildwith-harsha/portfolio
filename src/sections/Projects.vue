<template>
  <section class="section projects-page">
    <!-- Standardized Section Banner -->
    <h2 class="heading">Project Chronicle</h2>

    <!-- 3-Column Broadsheet Grid (Equal Columns) -->
    <div class="projects-triptych">
      <!-- Column 1: Sneaker Design Studio -->
      <article class="project-column">
        <p class="project-kicker">★ Featured Project • Live Web</p>
        <h3 class="project-headline">Sneaker Design Studio</h3>
        <p class="project-subhead">A Canvas That Moves in Real-Time</p>
        <div class="project-rule"></div>

        <p class="project-body">
          A browser-based 3D creative suite that puts customisation into customer hands.
          Built with Vue and Three.js, rendering interactive footwear with instant colour
          pickers, material selectors, and reactive scene-graph updates with no page reloads.
        </p>

        <p class="project-stack">Stack: Vue.js &bull; Three.js &bull; WebGL &bull; Vercel</p>

        <div class="project-action">
          <a
            href="https://sneaker-design-studio.vercel.app/"
            target="_blank"
            rel="noopener"
            class="project-btn live-btn"
          >
            <span>▸ Live Edition</span>
            <span class="btn-arrow">↗</span>
          </a>
        </div>
      </article>

      <!-- Column 2: HR Management System -->
      <article class="project-column">
        <p class="project-kicker">Enterprise Systems • Operations</p>
        <h3 class="project-headline">HR Management System</h3>
        <p class="project-subhead">Internal Corporate ERP Platform</p>
        <div class="project-rule"></div>

        <p class="project-body">
          A full-scale internal ERP platform powering corporate operations across departments.
          Integrates automated payroll processing, attendance tracking, story-point sprint
          accounting, and real-time employee performance dashboards.
        </p>

        <p class="project-stack">Stack: Laravel &bull; Vue.js &bull; MySQL &bull; REST</p>

        <div class="project-action">
          <span class="project-badge">
            <span class="badge-dot">●</span>
            <span>Shipped to Production</span>
          </span>
        </div>
      </article>

      <!-- Column 3: Kanban & Workflow Tracker -->
      <article class="project-column">
        <p class="project-kicker">Productivity Tools • Real-Time</p>
        <h3 class="project-headline">Kanban &amp; Workflow Tracker</h3>
        <p class="project-subhead">High-Velocity Agile Orchestration</p>
        <div class="project-rule"></div>

        <p class="project-body">
          A story-point–driven workflow board engineered for agile team velocity. Supports
          live WebSocket synchronization, role-based views, sprint progress tracking, and automated
          reporting that uncovers actionable delivery insights.
        </p>

        <p class="project-stack">Stack: Vue.js &bull; Laravel &bull; WebSockets &bull; MySQL</p>

        <div class="project-action">
          <span class="project-badge">
            <span class="badge-dot">●</span>
            <span>Shipped to Production</span>
          </span>
        </div>
      </article>
    </div>

    <!-- Bottom Broadsheet Verification Ribbon -->
    <div class="notice-ribbon">
      <div class="notice-rule"></div>
      <div class="notice-content">
        <span class="notice-tag">Developer on Record</span>
        <p class="notice-text">
          All systems documented above are verified production deliverables, engineered for active commercial and internal deployment. Available for new commissions.
        </p>
      </div>
      <div class="notice-rule"></div>
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
    ScrollTrigger.refresh()
    // Staggered broadsheet column entry
    gsap.fromTo(
      '.project-column',
      { y: 22, opacity: 0 },
      {
        y: 0,
        opacity: 1,
        stagger: 0.12,
        duration: 0.6,
        ease: 'power2.out',
        scrollTrigger: {
          trigger: '.projects-triptych',
          start: 'top 85%',
          once: true,
        },
      }
    )
  }
})
</script>

<style scoped>
/* =========================
   SECTION WRAPPER
========================= */
.projects-page {
  padding: 60px 60px 40px;
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
  padding: 14px 0 12px;
  margin-bottom: 14px;
  width: 100%;
  box-sizing: border-box;
}

/* =========================
   3 EQUAL COLUMNS (TRIPTYCH)
========================= */
.projects-triptych {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0;
  margin-top: 36px;
  align-items: stretch;
}

.project-column {
  display: flex;
  flex-direction: column;
  padding: 0 32px;
  border-right: 1px solid var(--line);
  box-sizing: border-box;
}

.project-column:first-child {
  padding-left: 0;
}

.project-column:last-child {
  border-right: none;
  padding-right: 0;
}

/* =========================
   COLUMN TYPOGRAPHY
========================= */
.project-kicker {
  font-family: var(--font-body);
  font-size: 9.5px;
  letter-spacing: 2.2px;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 700;
  margin-bottom: 6px;
  text-align: left;
}

.project-headline {
  font-family: var(--font-heading);
  font-size: 22px;
  line-height: 1.2;
  letter-spacing: 0.5px;
  font-weight: 700;
  color: var(--ink);
  text-transform: uppercase;
  margin: 0 0 4px;
}

.project-subhead {
  font-family: var(--font-body);
  font-size: 11.5px;
  font-style: italic;
  color: var(--muted-ink);
  margin-bottom: 6px;
}

.project-rule {
  border-top: 1px solid var(--line);
  margin: 8px 0 14px;
}

.project-body {
  font-family: var(--font-body);
  font-size: 13.5px;
  line-height: 1.78;
  text-align: justify;
  color: var(--ink);
  margin-bottom: 16px;
  flex-grow: 1;
}

/* =========================
   STACK & ACTION
========================= */
.project-stack {
  font-family: var(--font-body);
  font-size: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--muted-ink);
  font-style: italic;
  padding-top: 10px;
  border-top: 1px dashed rgba(59, 52, 45, 0.35);
  margin-bottom: 14px;
}

.project-action {
  margin-top: auto;
  padding-bottom: 4px;
}

.project-btn {
  display: inline-flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  padding: 8px 16px;
  font-family: var(--font-heading);
  font-size: 11px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  text-decoration: none;
  background: var(--ink);
  color: var(--paper);
  border: 1px solid var(--ink);
  transition: all 0.2s ease;
  width: 100%;
  box-sizing: border-box;
}

.project-btn:hover {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
  text-decoration: none;
}

.btn-arrow {
  font-size: 13px;
  transition: transform 0.2s ease;
}

.project-btn:hover .btn-arrow {
  transform: translate(2px, -2px);
}

.project-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 7px 14px;
  font-family: var(--font-body);
  font-size: 10px;
  letter-spacing: 1.2px;
  text-transform: uppercase;
  color: var(--muted-ink);
  border: 1px solid var(--line);
  background: rgba(38, 33, 28, 0.025);
  width: 100%;
  box-sizing: border-box;
  justify-content: center;
}

.badge-dot {
  color: #3b7036;
  font-size: 8px;
}

/* =========================
   BOTTOM NOTICE RIBBON
========================= */
.notice-ribbon {
  margin-top: 44px;
}

.notice-rule {
  border-top: 1px solid var(--line);
}

.notice-content {
  padding: 12px 16px;
  display: flex;
  align-items: center;
  gap: 20px;
  background: rgba(38, 33, 28, 0.02);
}

.notice-tag {
  font-family: var(--font-heading);
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 700;
  white-space: nowrap;
}

.notice-text {
  font-family: var(--font-body);
  font-size: 12px;
  color: var(--muted-ink);
  margin: 0;
  font-style: italic;
  line-height: 1.6;
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 960px) {
  .projects-triptych {
    grid-template-columns: 1fr;
    gap: 0;
  }

  .project-column {
    padding: 24px 0;
    border-right: none;
    border-bottom: 1px solid var(--line);
  }

  .project-column:first-child {
    padding-top: 0;
  }

  .project-column:last-child {
    border-bottom: none;
    padding-bottom: 0;
  }

  .notice-content {
    flex-direction: column;
    align-items: flex-start;
    gap: 6px;
  }
}

@media (max-width: 480px) {
  .projects-page {
    padding: 40px 20px;
  }

  .project-headline {
    font-size: 20px;
  }

  .project-body {
    font-size: 13px;
  }
}
</style>
