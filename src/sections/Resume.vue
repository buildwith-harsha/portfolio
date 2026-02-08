<template>
  <section class="section resume special-insert">
    <!-- Section label -->
    <p class="kicker">Special Insert</p>

    <!-- Heading -->
    <h2 class="heading">Resume</h2>

    <!-- Resume frame -->
    <div class="resume-frame">
      <iframe
        :src="resumeUrl"
        title="Resume Preview"
        frameborder="0"
      ></iframe>
    </div>

    <!-- Actions -->
    <div class="actions">
      <a
        :href="resumeUrl"
        target="_blank"
        rel="noopener"
        class="btn outline"
      >
        Open Full Page
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
      This resume is a printable insert, formatted for clarity and real-world use.
    </p>
  </section>
</template>

<script setup>
const resumeUrl = "/resume/HarshaVardhiniManikandan-Resume.pdf"
</script>

<style scoped>
/* Section spacing */
.special-insert {
  padding: 80px 60px;
  text-align: center;
}

/* Small editorial label */
.kicker {
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 10px;
  font-family: var(--font-body);
}

/* Heading */
.heading {
  font-family: var(--font-heading);
  font-size: 42px;
  margin-bottom: 40px;
}

/* Resume frame */
.resume-frame {
  max-width: 820px;
  height: 520px;
  margin: 0 auto;
  border: 3px solid var(--ink);
  overflow: hidden;
  background: white;
}

/* Iframe */
.resume-frame iframe {
  width: 100%;
  height: 100%;
}

/* Action buttons */
.actions {
  margin-top: 30px;
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

/* Buttons */
.btn {
  font-family: var(--font-heading);
  font-size: 13px;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 10px 22px;
  text-decoration: none;
  cursor: pointer;
}

/* Outline button */
.outline {
  border: 2px solid var(--ink);
  color: var(--ink);
}

/* Solid button */
.solid {
  background: var(--ink);
  color: var(--paper);
}

/* Small note */
.note {
  margin-top: 26px;
  font-size: 13px;
  color: var(--muted-ink);
  font-family: var(--font-body);
}

/* Responsive */
@media (max-width: 768px) {
  .resume-frame {
    height: 420px;
  }

  .heading {
    font-size: 34px;
  }
}

@media (max-width: 480px) {
  .resume-frame {
    height: 360px;
  }
}
</style>
