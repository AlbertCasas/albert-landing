<script setup lang="ts">
function scrollTo(id: string) {
  const el = document.getElementById(id)
  if (el) el.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <header class="nav">
    <span class="nav-logo">AlbertCasas<span class="dot">.</span></span>
    <nav class="nav-links">
      <a @click.prevent="scrollTo('projects')">projects</a>
      <a @click.prevent="scrollTo('contact')">contact</a>
    </nav>
  </header>
</template>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.75rem 3rem;
  border-bottom: 1px solid var(--color-border);
  position: sticky;
  top: 0;
  background: var(--color-bg);
  z-index: 100;
  backdrop-filter: blur(12px);
}

.nav-logo {
  font-size: 20px;
  font-weight: 500;
  letter-spacing: -0.5px;
}

.dot {
  color: var(--color-accent);
}

.nav-links {
  display: flex;
  gap: 2.5rem;
}

.nav-links a {
  font-size: 16px;
  color: var(--color-text-secondary);
  transition: color 0.15s;
  cursor: pointer;
}

.nav-links a:hover {
  color: var(--color-text);
}

@media (max-width: 768px) {
  .nav {
    padding: 1.25rem 1.5rem;
    flex-wrap: wrap;
    gap: 0.75rem;
  }

  .nav-logo {
    font-size: 17px;
  }

  .nav-links {
    gap: 1.25rem;
  }

  .nav-links a {
    font-size: 13px;
  }
}
</style>