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
   ARTICLE CARD
========================= */
.news-card {
  padding: 18px 16px;
  margin-bottom: 28px;

  background: transparent;

  border-top: 3px solid var(--line);
  border-bottom: 1px solid var(--line);

  font-family: var(--font-body);
  cursor: default;
}

/* =========================
   HEADLINE
========================= */
.headline {
  font-family: var(--font-heading);
  font-size: 19px;              /* print-scale */
  font-weight: 700;
  line-height: 1.25;
  letter-spacing: -0.3px;
  margin-bottom: 6px;
  color: var(--ink);
}

/* =========================
   RULE
========================= */
.rule {
  height: 1px;
  background: var(--line);
  margin: 8px 0 12px;
}

/* =========================
   BODY TEXT
========================= */
.summary {
  font-size: 13.5px;
  line-height: 1.75;
  color: var(--muted-ink);
  text-align: justify;
}
</style>
