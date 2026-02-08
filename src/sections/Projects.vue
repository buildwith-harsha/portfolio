<template>
  <section class="section projects editorial">
    <!-- Section label -->
    <p class="kicker">Case Studies</p>

    <!-- Heading -->
    <h2 class="heading">Projects</h2>

    <!-- Editorial grid -->
    <div class="projects-grid">
      <Card
        title="HR Management System"
        desc="A full-scale internal ERP system built using Laravel and Vue, covering payroll, attendance, performance tracking, and dashboards used daily by employees."
      />

      <Card
        title="College Management System"
        desc="A Laravel-based academic management platform handling student records, courses, attendance, and administrative workflows."
      />

      <Card
        title="Kanban & Workflow Tracker"
        desc="A task and story-point driven Kanban system designed to measure productivity, timelines, and employee performance metrics."
      />
    </div>
  </section>
</template>

<script setup>
import Card from "@/components/Card.vue"
</script>

<style scoped>
/* Section spacing */
.editorial {
  padding: 80px 60px;
}

/* Small section label */
.kicker {
  text-align: center;
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 10px;
  font-family: var(--font-body);
}

/* Grid layout */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px 30px;
  max-width: 1000px;
  margin: 60px auto 0;
}

/* Responsive */
@media (max-width: 900px) {
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>
