<script setup lang="ts">
</script>

<template>
  <section class="hero">
    <div class="hero-tag">
      <span class="dot"></span>
      open to work
    </div>
    <h1>Senior Frontend<br><span class="muted">Developer.</span></h1>
<p>3+ years building scalable product features and reusable component systems. Deep expertise in Vue.js — from architecture to production.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn-primary">View projects</a>
      <a href="/cv.pdf" class="btn-secondary" target="_blank">Download CV</a>
    </div>
  </section>
</template>

<style scoped>
.hero {
  padding: 6rem 3rem 5rem;
  max-width: 780px;
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
  margin-bottom: 2rem;
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
  font-size: 56px;
  font-weight: 500;
  line-height: 1.1;
  letter-spacing: -2px;
  color: var(--color-text);
  margin-bottom: 1.5rem;
}

.muted {
  color: var(--color-text-muted);
}

p {
  font-size: 17px;
  color: var(--color-text-secondary);
  max-width: 480px;
  margin-bottom: 2.5rem;
  line-height: 1.7;
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
  padding: 11px 22px;
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
  padding: 11px 22px;
  border-radius: var(--radius);
  transition: color 0.15s, border-color 0.15s;
}

.btn-secondary:hover {
  color: var(--color-text);
  border-color: var(--color-text-muted);
}

@media (max-width: 768px) {
  .hero {
    padding: 3rem 1.5rem 3rem;
  }

  h1 {
    font-size: 36px;
    letter-spacing: -1px;
  }

  p {
    font-size: 15px;
  }

  .hero-ctas {
    flex-wrap: wrap;
  }

  .btn-primary,
  .btn-secondary {
    flex: 1;
    justify-content: center;
    text-align: center;
  }
}
</style>