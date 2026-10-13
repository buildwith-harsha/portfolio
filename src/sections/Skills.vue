<template>
  <section class="section skills classifieds">
    <!-- Section label -->
    <p class="kicker">Technical Index</p>

    <!-- Heading -->
    <h2 class="heading">Skills</h2>

    <!-- Classified grid -->
    <div class="container">
      <div class="columns">
        <span class="word" v-for="(skill, index) in skills" :key="index">
          {{ skill }}
        </span>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const skills = ref([
  'React.js',
  'JavaScript',
  'Node.js',
  'REST APIs',
  'AWS',
  'Git & GitHub',
  'CI/CD',
  'GitHub Actions',
  'Docker',
  'SQL & Databases',
  'Redux Toolkit',
  'Laravel',
])

onMounted(() => {
  gsap.from('.word', {
    y: 24,
    opacity: 0,
    stagger: 0.06,
    duration: 0.6,
    ease: 'power2.out',
    scrollTrigger: {
      trigger: '.classifieds',
      start: 'top 80%',
    },
  })
})
</script>

<style scoped>
/* Section spacing */
.classifieds {
  padding: 80px 60px;
}

/* Small editorial label */
.kicker {
  text-align: center;
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 10px;
  font-family: var(--font-body);
}

/* Grid wrapper */
.container {
  display: flex;
  justify-content: center;
}

/* Classified-style grid */
.columns {
  display: grid;
  grid-template-columns: repeat(3, minmax(160px, 1fr));
  gap: 16px 30px;
  max-width: 760px;
  margin-top: 40px;
}

/* Individual skill item */
.word {
  border: 1px solid var(--line);
  padding: 10px 14px;
  font-family: var(--font-body);
  font-size: 13px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  text-align: center;
  color: var(--ink);
  background: transparent;
  cursor: default;
}

/* Subtle hover – newspaper style */
.word:hover {
  background: rgba(0, 0, 0, 0.03);
}

/* Responsive */
@media (max-width: 768px) {
  .columns {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .columns {
    grid-template-columns: 1fr;
  }
}
</style>
