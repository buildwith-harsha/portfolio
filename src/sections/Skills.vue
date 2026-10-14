<template>
  <section class="section skills classifieds">
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
  if (typeof window !== 'undefined' && 'IntersectionObserver' in window) {
    gsap.from('.word', {
      y: 20,
      opacity: 0,
      stagger: 0.05,
      duration: 0.5,
      ease: 'power2.out',
      scrollTrigger: {
        trigger: '.classifieds',
        start: 'top 85%',
        once: true,
      },
    })
  }
})
</script>

<style scoped>
/* Section spacing */
.classifieds {
  padding: 24px 60px 70px;
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
  margin-top: 36px;
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
  transition: all 0.22s ease;
  cursor: default;
}

.word:hover {
  background: var(--ink);
  color: var(--paper);
  border-color: var(--ink);
  transform: translateY(-2px);
  box-shadow: 0 4px 10px rgba(38, 33, 28, 0.18);
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
