<template>
  <header class="nav">
    <span class="nav-logo">albert<span class="dot">.</span></span>
    <nav class="nav-links">
      <a href="#proyectos">proyectos</a>
      <a href="#sobre-mi">sobre mí</a>
      <a href="#contacto">contacto</a>
    </nav>
  </header>
</template>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.25rem 2rem;
  border-bottom: 1px solid var(--color-border);
  position: sticky;
  top: 0;
  background: var(--color-bg);
  z-index: 100;
  backdrop-filter: blur(12px);
}

.nav-logo {
  font-size: 15px;
  font-weight: 500;
  letter-spacing: -0.3px;
}

.dot {
  color: var(--color-accent);
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-links a {
  font-size: 13px;
  color: var(--color-text-secondary);
  transition: color 0.15s;
}

.nav-links a:hover {
  color: var(--color-text);
}
</style>