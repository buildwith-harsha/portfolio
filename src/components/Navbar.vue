<template>
  <nav class="navbar">
    <!-- Masthead -->
    <div class="masthead">
      <img src="@/assets/NameSticker.png" class="name-logo" />
      <p class="edition">Portfolio Edition • 2026</p>
    </div>

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
  { name: "Resume", id: "resume" },
]
</script>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;

  background: var(--paper);
  border-bottom: 3px solid var(--ink);

  padding: 18px 40px 12px;
}

/* masthead area */
.masthead {
  text-align: center;
  margin-bottom: 10px;
}

.name-logo {
  height: 42px;
  display: block;
  margin: 0 auto;
}

.edition {
  font-family: var(--font-body);
  font-size: 12px;
  color: var(--muted-ink);
  letter-spacing: 1px;
  margin-top: 4px;
}

/* section links */
.sections {
  display: flex;
  justify-content: center;
  gap: 42px;
  list-style: none;
  padding: 10px 0 0;
  border-top: 1px solid var(--line);
}

.sections a {
  font-family: var(--font-heading);
  font-size: 13px;
  text-transform: uppercase;
  letter-spacing: 2px;
  color: var(--ink);
  text-decoration: none;
}

.sections a:hover {
  text-decoration: underline;
}

/* mobile */
@media (max-width: 768px) {
  .sections {
    gap: 20px;
    flex-wrap: wrap;
  }

  .name-logo {
    height: 36px;
  }
}
</style>
