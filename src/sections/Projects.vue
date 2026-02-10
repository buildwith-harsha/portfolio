<template>
  <section class="section projects">
    <!-- Section label -->
    <p class="kicker">Case Records</p>

    <!-- Heading -->
    <h2 class="heading">Projects</h2>

    <div class="rule"></div>

    <!-- Newspaper columns -->
    <div class="projects-columns">
      <article class="news-card">
        <h3 class="project-title">HR Management System</h3>
        <p class="project-desc">
          A full-scale internal ERP platform covering payroll, attendance,
          employee performance dashboards, and operational reporting,
          built using Laravel and Vue and used in daily workflows.
        </p>
      </article>

      <article class="news-card">
        <h3 class="project-title">College Management System</h3>
        <p class="project-desc">
          An academic management system designed to handle student records,
          course administration, attendance tracking, and institutional
          workflows using Laravel.
        </p>
      </article>

      <article class="news-card">
        <h3 class="project-title">Kanban & Workflow Tracker</h3>
        <p class="project-desc">
          A story-point–driven Kanban system created to measure productivity,
          timelines, and team performance, supporting real-world project
          tracking and reporting.
        </p>
      </article>
    </div>
  </section>
</template>

<style scoped>
/* =========================
   SECTION WRAPPER
========================= */
.projects {
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
   NEWSPAPER COLUMNS
========================= */
.projects-columns {
  padding-top : 30px;
  column-count: 3;
  column-gap: 40px;
  max-width: 1200px;
  margin: 0 auto;
}

/* =========================
   PROJECT ARTICLE (ARCHIVE STYLE)
========================= */
.news-card {
  break-inside: avoid;
  margin-bottom: 34px;
  padding-top: 10px;
  border-top: 1px solid var(--line);
}

/* =========================
   PROJECT TITLE
========================= */
.project-title {
  font-family: var(--font-heading);
  font-size: 17px;
  letter-spacing: 0.5px;
  margin-bottom: 6px;
  text-transform: uppercase;
}

/* =========================
   PROJECT BODY
========================= */
.project-desc {
  font-family: var(--font-body);
  font-size: 13.5px;
  line-height: 1.8;
  text-align: justify;
  color: var(--muted-ink);
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 1100px) {
  .projects-columns {
    column-count: 2;
  }
}

@media (max-width: 700px) {
  .projects-columns {
    column-count: 1;
  }
}
</style>
