<template>
  <nav class="navbar">
    <!-- Top line -->
    <div class="top-rule"></div>

    <!-- Masthead -->
    <div class="masthead">
      <img src="@/assets/NameSticker.png" class="name-logo" />
      <div class="meta">
        <span>Portfolio Edition</span>
        <span>•</span>
        <span>2026</span>
      </div>
    </div>

    <!-- Bottom line -->
    <div class="bottom-rule"></div>

    <!-- Sections -->
    <ul class="sections">
      <li v-for="item in menu" :key="item.id">
        <a :href="'#' + item.id">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script setup>
const menu = [
  { name: "Home", id: "home" },
  { name: "About", id: "about" },
  { name: "Skills", id: "skills" },
  { name: "Projects", id: "projects" },
  { name: "Resume", id: "resume" }
]
</script>

<style scoped>
/* =========================
   NAVBAR WRAPPER
========================= */
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;

  background: var(--paper);
  padding: 18px 40px 14px;
}

/* =========================
   RULES (NEWSPAPER LINES)
========================= */
.top-rule,
.bottom-rule {
  height: 2px;
  background: var(--ink);
}

.top-rule {
  margin-bottom: 12px;
}

.bottom-rule {
  margin-top: 12px;
}

/* =========================
   MASTHEAD
========================= */
.masthead {
  text-align: center;
}

.name-logo {
  height: 46px;
  width: auto;              /* 👈 prevents stretching */
  max-width: 240px;         /* 👈 safety limit */
  object-fit: contain;      /* 👈 keeps proportions */
  display: block;
  margin: 0 auto;
}


/* edition line */
.meta {
  margin-top: 6px;
  font-family: var(--font-body);
  font-size: 11px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--muted-ink);

  display: flex;
  justify-content: center;
  gap: 10px;
}

/* =========================
   SECTION LINKS
========================= */
.sections {
  margin-top: 14px;
  padding-top: 10px;

  display: flex;
  justify-content: center;
  gap: 44px;

  list-style: none;
  border-top: 1px solid var(--line);
}

.sections a {
  font-family: var(--font-heading);
  font-size: 12px;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: var(--ink);
  text-decoration: none;
}

.sections a:hover {
  text-decoration: underline;
  text-decoration-thickness: 1px;
}

/* =========================
   MOBILE
========================= */
@media (max-width: 768px) {
  .sections {
    gap: 20px;
    flex-wrap: wrap;
  }

  .name-logo {
    height: 36px;
    width: auto;
    max-width: 200px;
  }
}

</style>
