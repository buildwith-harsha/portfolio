<template>
  <header class="masthead-wrapper">
    <!-- ==============================================
         1. GRAND BROADSHEET MASTHEAD (Top of page)
         ============================================== -->
    <div class="grand-masthead">
      <!-- Top newspaper border line -->
      <div class="top-rule"></div>

      <!-- Masthead Title with Ornamental Flourish Wings -->
      <div class="masthead">
        <a href="#home" class="logo-link">
          <div class="masthead-title-row">
            <!-- Left ornamental wing -->
            <svg class="masthead-flourish-wing" viewBox="0 0 180 20" fill="currentColor" aria-hidden="true">
              <line x1="0" y1="10" x2="68" y2="10" stroke="currentColor" stroke-width="1.2" />
              <g transform="translate(90, 10)">
                <circle cx="0" cy="0" r="2.2" fill="currentColor" />
                <path d="M -2 0 C -7 -6 -16 -4 -18 0 C -16 4 -7 6 -2 0 Z" fill="currentColor" />
                <path d="M 2 0 C 7 -6 16 -4 18 0 C 16 4 7 6 2 0 Z" fill="currentColor" />
                <circle cx="-19" cy="0" r="1.2" fill="currentColor" />
                <circle cx="19" cy="0" r="1.2" fill="currentColor" />
              </g>
              <line x1="112" y1="10" x2="180" y2="10" stroke="currentColor" stroke-width="1.2" />
            </svg>

            <!-- HARSHA Title -->
            <span class="masthead-title">HARSHA</span>

            <!-- Right ornamental wing -->
            <svg class="masthead-flourish-wing" viewBox="0 0 180 20" fill="currentColor" aria-hidden="true">
              <line x1="0" y1="10" x2="68" y2="10" stroke="currentColor" stroke-width="1.2" />
              <g transform="translate(90, 10)">
                <circle cx="0" cy="0" r="2.2" fill="currentColor" />
                <path d="M -2 0 C -7 -6 -16 -4 -18 0 C -16 4 -7 6 -2 0 Z" fill="currentColor" />
                <path d="M 2 0 C 7 -6 16 -4 18 0 C 16 4 7 6 2 0 Z" fill="currentColor" />
                <circle cx="-19" cy="0" r="1.2" fill="currentColor" />
                <circle cx="19" cy="0" r="1.2" fill="currentColor" />
              </g>
              <line x1="112" y1="10" x2="180" y2="10" stroke="currentColor" stroke-width="1.2" />
            </svg>
          </div>
        </a>

        <!-- Meta Dateline -->
        <div class="meta">
          <span>THE DEVELOPER'S EDITION</span>
          <span class="meta-dot">•</span>
          <span>SOFTWARE ENGINEER</span>
          <span class="meta-dot">•</span>
          <span>INDIA</span>
        </div>
      </div>

      <!-- Bottom newspaper border line -->
      <div class="bottom-rule"></div>

      <!-- Full Section Navigation Links -->
      <ul class="sections">
        <li v-for="item in menu" :key="item.id">
          <a
            :href="'#' + item.id"
            :class="{ active: activeSection === item.id }"
          >
            {{ item.name }}
          </a>
        </li>
      </ul>
    </div>

    <!-- ==============================================
         2. SLIM COMPRESSED STICKY RIBBON (~44px)
         Pinnable when scrolled past hero / masthead
         ============================================== -->
    <nav
      class="sticky-ribbon"
      :class="{ 'is-visible': isScrolled }"
      aria-label="Sticky editorial navigation"
    >
      <div class="ribbon-inner">
        <!-- Left: Brand (Flourish + HARSHA) -->
        <a href="#home" class="ribbon-brand" title="Return to Top">
          <span class="ribbon-brand-ornament">❧</span>
          <span class="ribbon-brand-title">HARSHA</span>
        </a>

        <!-- Center: Section links (exact same text position & width as grand masthead) -->
        <ul class="ribbon-sections">
          <li v-for="item in menu" :key="item.id" class="ribbon-item">
            <a
              :href="'#' + item.id"
              :class="{ active: activeSection === item.id }"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>

        <!-- Right: Action CTA -->
        <div class="ribbon-action">
          <a href="#contact" class="ribbon-cta">
            Hire Desk ➔
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const activeSection = ref('home')

const menu = [
  { name: 'Home', id: 'home' },
  { name: 'About', id: 'about' },
  { name: 'Skills', id: 'skills' },
  { name: 'Projects', id: 'projects' },
  { name: 'Contact', id: 'contact' }
]

const handleScroll = () => {
  // Show the slim ribbon once scrolled past the grand masthead
  isScrolled.value = window.scrollY > 160

  // Active section spy
  const scrollPos = window.scrollY + 100
  for (let i = menu.length - 1; i >= 0; i--) {
    const el = document.getElementById(menu[i].id)
    if (el) {
      if (scrollPos >= el.offsetTop) {
        activeSection.value = menu[i].id
        break
      }
    }
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
  handleScroll()
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
/* =========================
   MASTHEAD WRAPPER
========================= */
.masthead-wrapper {
  width: 100%;
  position: relative;
}

/* =========================
   1. GRAND MASTHEAD (Top)
========================= */
.grand-masthead {
  max-width: 1240px;
  margin: 0 auto;
  padding: 10px 40px 10px;
  background: var(--paper);
}

.top-rule,
.bottom-rule {
  height: 2px;
  background: var(--ink);
  margin: 0;
}

.masthead {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0;
  padding: 0;
}

.logo-link {
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  line-height: 1;
}

.masthead-title-row {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 24px;
  margin: 2px 0 4px;
}

.masthead-title {
  font-family: var(--font-heading);
  font-size: clamp(48px, 6vw, 76px);
  font-weight: 900;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: var(--ink);
  line-height: 0.92;
  display: inline-block;
  user-select: none;
}

.masthead-flourish-wing {
  width: 170px;
  height: 18px;
  color: var(--ink);
  flex-shrink: 0;
  display: block;
}

.meta {
  margin: 2px 0 10px;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: var(--muted-ink);
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 12px;
  line-height: 1.2;
}

.meta-dot {
  font-size: 8px;
  opacity: 0.6;
}

.sections {
  margin-top: 10px;
  padding-top: 0;
  display: flex;
  justify-content: center;
  gap: 40px;
  list-style: none;
  border-top: none;
}

.sections a {
  font-family: var(--font-heading);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 2.2px;
  text-transform: uppercase;
  color: var(--ink);
  text-decoration: none;
  transition: color 0.15s ease;
}

.sections a:hover,
.sections a.active {
  color: var(--accent);
  text-decoration: underline;
  text-decoration-thickness: 1px;
  text-underline-offset: 3px;
}

/* ==============================================
   2. SLIM COMPRESSED STICKY RIBBON (~44px - 46px)
============================================== */
.sticky-ribbon {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 46px;
  z-index: 1000;
  background: rgba(242, 232, 207, 0.96);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  border-bottom: 2px solid var(--ink);
  box-shadow: 0 4px 18px rgba(38, 33, 28, 0.08);

  /* Hidden initially off-screen */
  transform: translateY(-100%);
  opacity: 0;
  pointer-events: none;
  transition: transform 0.28s cubic-bezier(0.16, 1, 0.3, 1), opacity 0.2s ease;
}

.sticky-ribbon.is-visible {
  transform: translateY(0);
  opacity: 1;
  pointer-events: auto;
}

.ribbon-inner {
  max-width: 1240px;
  height: 100%;
  margin: 0 auto;
  padding: 0 40px;
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
}

/* Ribbon Left Brand */
.ribbon-brand {
  display: flex;
  align-items: center;
  gap: 8px;
  text-decoration: none;
  line-height: 1;
  justify-self: start;
}

.ribbon-brand-ornament {
  font-size: 14px;
  color: var(--accent);
}

.ribbon-brand-title {
  font-family: var(--font-heading);
  font-size: 14px;
  font-weight: 900;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: var(--ink);
  transition: color 0.15s ease;
}

.ribbon-brand:hover .ribbon-brand-title {
  color: var(--accent);
}

/* Ribbon Center Sections (Exact same position, width & spacing as grand masthead) */
.ribbon-sections {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 40px;
  list-style: none;
  margin: 0;
  padding: 0;
  justify-self: center;
}

.ribbon-item {
  display: flex;
  align-items: center;
}

.ribbon-item a {
  font-family: var(--font-heading);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 2.2px;
  text-transform: uppercase;
  color: var(--ink);
  text-decoration: none;
  transition: color 0.15s ease;
}

.ribbon-item a:hover,
.ribbon-item a.active {
  color: var(--accent);
  text-decoration: underline;
  text-decoration-thickness: 1px;
  text-underline-offset: 3px;
}

/* Ribbon Right Action Button */
.ribbon-action {
  display: flex;
  align-items: center;
  justify-self: end;
}

.ribbon-cta {
  font-family: var(--font-heading);
  font-size: 10.5px;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  text-decoration: none;
  background: var(--ink);
  color: var(--paper);
  padding: 6px 14px;
  border: 1px solid var(--ink);
  transition: all 0.18s ease;
  white-space: nowrap;
}

.ribbon-cta:hover {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
  text-decoration: none;
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 1024px) {
  .sections,
  .ribbon-sections {
    gap: 24px;
  }
}

@media (max-width: 900px) {
  .masthead-flourish-wing {
    width: 110px;
  }
  .masthead-title-row {
    gap: 16px;
  }
}

@media (max-width: 768px) {
  .grand-masthead {
    padding: 8px 20px 8px;
  }

  .sections {
    gap: 16px;
    flex-wrap: wrap;
  }

  .masthead-flourish-wing {
    width: 60px;
  }

  .masthead-title {
    font-size: 42px;
    letter-spacing: 3px;
  }

  .masthead-title-row {
    gap: 12px;
    margin: -2px 0 2px;
  }

  .meta {
    font-size: 9.5px;
    letter-spacing: 1.5px;
    gap: 8px;
    flex-wrap: wrap;
  }

  .ribbon-inner {
    display: flex;
    justify-content: space-between;
    padding: 0 16px;
    gap: 10px;
  }

  .ribbon-sections {
    gap: 16px;
    overflow-x: auto;
    white-space: nowrap;
    scrollbar-width: none;
    -ms-overflow-style: none;
    padding: 2px 0;
  }

  .ribbon-sections::-webkit-scrollbar {
    display: none;
  }

  .sections a,
  .ribbon-item a {
    font-size: 11px;
    letter-spacing: 1.5px;
  }

  .ribbon-cta {
    padding: 5px 10px;
    font-size: 9.5px;
  }
}

@media (max-width: 520px) {
  .masthead-flourish-wing {
    display: none;
  }

  .masthead-title {
    font-size: 36px;
  }

  .sections a,
  .ribbon-item a {
    font-size: 10px;
    letter-spacing: 1px;
  }
}
</style>
