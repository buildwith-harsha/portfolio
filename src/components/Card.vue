<template>
  <article class="news-card">
    <h3 class="headline">{{ title }}</h3>
    <div class="rule"></div>
    <p class="summary">{{ desc }}</p>
  </article>
</template>

<script setup>
defineProps({
  title: String,
  desc: String
})
</script>

<style scoped>
/* =========================
   CARD WRAPPER
========================= */
.news-card {
  width: 280px;
  padding: 20px 18px;

  background: transparent;

  border-top: 2px solid var(--ink);
  border-bottom: 1px solid var(--line);

  font-family: var(--font-body);
  cursor: default;

  transition: transform 0.2s ease;
}

/* subtle lift – like lifting paper */
.news-card:hover {
  transform: translateY(-3px);
}

/* =========================
   HEADLINE
========================= */
.headline {
  font-family: var(--font-heading);
  font-size: 20px;          /* smaller = more authentic */
  font-weight: 700;
  line-height: 1.25;
  letter-spacing: -0.3px;
  margin-bottom: 6px;
}

/* =========================
   RULE
========================= */
.rule {
  width: 100%;
  height: 1px;
  background: var(--line);
  margin: 10px 0 12px;
}

/* =========================
   BODY TEXT
========================= */
.summary {
  font-size: 13.5px;        /* true newspaper size */
  line-height: 1.7;
  color: var(--muted-ink);
  text-align: justify;
}
</style>
