<template>
  <Navbar />

  <Home id="home" />
  <About id="about" />
  <Skills id="skills" />
  <Projects id="projects" />
  <Resume id="resume" />

  <Footer />
</template>

<script setup>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

import Home from '@/sections/Home.vue'
import About from '@/sections/About.vue'
import Skills from '@/sections/Skills.vue'
import Projects from '@/sections/Projects.vue'
import Resume from '@/sections/Resume.vue'
import Card from '@/components/Card.vue'

</script>
