<script setup lang="ts">
const year = new Date().getFullYear()
</script>

<template>
  <footer class="footer newspaper-footer">
    <div class="footer-line"></div>

    <div class="footer-content">
      <!-- Left -->
      <p class="footer-text">© {{ year }} Harshavardhini</p>

      <!-- Center -->
      <p class="footer-center">Portfolio Edition • Built with Vue & Laravel</p>

      <!-- Right spacer to balance grid alignment -->
      <div class="footer-spacer"></div>
    </div>
  </footer>
</template>

<style scoped>
.newspaper-footer {
  margin-top: 120px;
  padding: 40px 60px 30px;
  background: var(--paper);
  font-family: var(--font-body);
}

/* Top rule */
.footer-line {
  border-top: 3px solid var(--ink);
  margin-bottom: 20px;
}

/* Layout */
.footer-content {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
}

/* Text styles */
.footer-text {
  font-size: 12px;
  color: var(--muted-ink);
}

.footer-center {
  font-size: 12px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--ink);
  text-align: center;
}

/* Alignment */
.footer-text:first-child {
  text-align: left;
}

.footer-text:last-child {
  text-align: right;
}

/* Responsive */
@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: 10px;
    text-align: center;
  }

  .footer-text:first-child,
  .footer-text:last-child {
    text-align: center;
  }
}
</style>
