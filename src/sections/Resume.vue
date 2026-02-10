<template>
  <section class="section resume special-insert">
    <!-- Section label -->
    <p class="kicker">Special Insert</p>

    <!-- Heading -->
    <h2 class="heading">Résumé</h2>

    <!-- Dateline -->
    <p class="dateline">Portfolio Edition • Prepared for Professional Review</p>

    <div class="rule"></div>



    <!-- Actions -->
    <div class="actions">
      <a
        :href="resumeUrl"
        target="_blank"
        rel="noopener"
        class="btn outline"
      >
        View Full Insert
      </a>

      <a
        :href="resumeUrl"
        download
        class="btn solid"
      >
        Download PDF
      </a>
    </div>

    <!-- Footer note -->
    <p class="note">
      This résumé is presented as a printable insert, formatted for clarity,
      accuracy, and real-world evaluation.
    </p>
  </section>
</template>

<script setup>
const resumeUrl = "/resume/HarshaVardhiniManikandan-Resume.pdf"
</script>

<style scoped>
/* =========================
   SECTION WRAPPER
========================= */
.special-insert {
  padding: 80px 60px 100px;
  text-align: center;
}

/* =========================
   KICKER
========================= */
.kicker {
  font-size: 11px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 6px;
  font-family: var(--font-body);
}

/* =========================
   HEADING
========================= */
.heading {
  font-family: var(--font-heading);
  font-size: 36px;
  margin-bottom: 6px;
}

/* =========================
   DATELINE
========================= */
.dateline {
  font-size: 12px;
  font-style: italic;
  color: var(--muted-ink);
  margin-bottom: 24px;
}

/* =========================
   RESUME FRAME
========================= */
.resume-frame {
  max-width: 820px;
  height: 520px;
  margin: 0 auto;
  border: 3px solid var(--ink);
  background: #fff;
  overflow: hidden;
}

/* Iframe */
.resume-frame iframe {
  width: 100%;
  height: 100%;
}

/* =========================
   ACTIONS
========================= */
.actions {
  margin-top: 28px;
  display: flex;
  justify-content: center;
  gap: 18px;
  flex-wrap: wrap;
}

/* Buttons (print-style) */
.btn {
  font-family: var(--font-heading);
  font-size: 12px;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 8px 22px;
  text-decoration: none;
  cursor: pointer;
}

/* Outline notice */
.outline {
  border: 2px solid var(--ink);
  color: var(--ink);
}

/* Solid notice */
.solid {
  background: var(--ink);
  color: var(--paper);
}

/* =========================
   NOTE
========================= */
.note {
  margin-top: 26px;
  font-size: 13px;
  line-height: 1.6;
  color: var(--muted-ink);
  font-family: var(--font-body);
  max-width: 520px;
  margin-left: auto;
  margin-right: auto;
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 768px) {
  .resume-frame {
    height: 420px;
  }

  .heading {
    font-size: 32px;
  }
}

@media (max-width: 480px) {
  .resume-frame {
    height: 360px;
  }
}
</style>
