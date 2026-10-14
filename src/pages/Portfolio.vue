<template>
  <Navbar />

  <Home id="home" />
  <About id="about" />
  <Skills id="skills" />
  <Projects id="projects" />
  <Contact id="contact" />

  <Footer />
</template>

<script setup>
import { onMounted, onUnmounted, nextTick } from 'vue'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

import Home from '@/sections/Home.vue'
import About from '@/sections/About.vue'
import Skills from '@/sections/Skills.vue'
import Projects from '@/sections/Projects.vue'
import Contact from '@/sections/Contact.vue'

gsap.registerPlugin(ScrollTrigger)

let scrollTriggers = []

onMounted(() => {
  nextTick(() => {
    const headings = document.querySelectorAll('.heading')
    headings.forEach((heading) => {
      // If already in or above viewport, show immediately
      const rect = heading.getBoundingClientRect()
      if (rect.top <= (window.innerHeight || 800)) {
        heading.classList.add('is-visible')
      }

      try {
        const st = ScrollTrigger.create({
          trigger: heading,
          start: 'top 92%',
          onEnter: () => heading.classList.add('is-visible'),
          onEnterBack: () => heading.classList.add('is-visible'),
        })
        scrollTriggers.push(st)
      } catch {
        heading.classList.add('is-visible')
      }
    })
  })
})

onUnmounted(() => {
  scrollTriggers.forEach((st) => st.kill())
  scrollTriggers = []
})
</script>
