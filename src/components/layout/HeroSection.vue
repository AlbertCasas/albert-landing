<script setup lang="ts">
</script>

<template>
  <section class="hero">
    <div class="hero-tag">
      <span class="dot"></span>
      disponible para trabajar
    </div>
    <h1>Frontend developer<br><span class="muted">& diseño que importa.</span></h1>
    <p>Construyo interfaces limpias y funcionales con Vue 3. Me importa tanto el código como la experiencia de quien lo usa.</p>
    <div class="hero-ctas">
      <a href="#proyectos" class="btn-primary">ver proyectos</a>
      <a href="/cv.pdf" class="btn-secondary" target="_blank">
        descargar CV
      </a>
    </div>
  </section>
</template>

<style scoped>
.hero {
  padding: 5rem 2rem 4rem;
  max-width: 700px;
}

.hero-tag {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 12px;
  color: var(--color-accent);
  background: var(--color-accent-bg);
  border: 1px solid rgba(74, 222, 128, 0.2);
  border-radius: 20px;
  padding: 5px 14px;
  margin-bottom: 1.75rem;
}

.dot {
  width: 6px;
  height: 6px;
  background: var(--color-accent);
  border-radius: 50%;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.3; }
}

h1 {
  font-size: 42px;
  font-weight: 500;
  line-height: 1.15;
  letter-spacing: -1.5px;
  color: var(--color-text);
  margin-bottom: 1.25rem;
}

.muted {
  color: var(--color-text-muted);
}

p {
  font-size: 16px;
  color: var(--color-text-secondary);
  max-width: 460px;
  margin-bottom: 2rem;
}

.hero-ctas {
  display: flex;
  gap: 12px;
  align-items: center;
}

.btn-primary {
  background: var(--color-accent);
  color: #0e0e0e;
  font-size: 13px;
  font-weight: 500;
  padding: 10px 20px;
  border-radius: var(--radius);
  transition: opacity 0.15s;
}

.btn-primary:hover {
  opacity: 0.85;
}

.btn-secondary {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  color: var(--color-text-secondary);
  border: 1px solid var(--color-border-strong);
  padding: 10px 20px;
  border-radius: var(--radius);
  transition: color 0.15s, border-color 0.15s;
}

.btn-secondary:hover {
  color: var(--color-text);
  border-color: var(--color-text-muted);
}
</style>