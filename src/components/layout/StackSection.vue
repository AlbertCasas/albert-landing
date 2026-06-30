<template>
  <section class="stack">
    <p class="label">stack</p>
    <div class="pills">
      <span class="pill accent">Vue.js</span>
      <span class="pill accent">TypeScript</span>
      <span class="pill accent">JavaScript</span>
      <span class="pill accent">SCSS</span>
      <span class="pill">Pinia</span>
      <span class="pill">Vuex</span>
      <span class="pill">FastAPI</span>
      <span class="pill">MySQL</span>
      <span class="pill">REST APIs</span>
      <span class="pill">Git</span>
      <span class="pill">Node.js</span>
    </div>
  </section>
</template>

<style scoped>
.stack {
  padding: 2rem 2rem;
  border-top: 1px solid var(--color-border);
}

.label {
  font-size: 11px;
  color: var(--color-text-muted);
  letter-spacing: 1px;
  text-transform: uppercase;
  margin-bottom: 1rem;
}

.pills {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}

.pill {
  font-size: 12px;
  color: var(--color-text-secondary);
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 20px;
  padding: 5px 14px;
  transition: border-color 0.15s;
}

.pill:hover {
  border-color: var(--color-border-strong);
}

.pill.accent {
  color: var(--color-accent);
  background: var(--color-accent-bg);
  border-color: rgba(74, 222, 128, 0.2);
}
</style>