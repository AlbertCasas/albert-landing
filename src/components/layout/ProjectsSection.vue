<script setup lang="ts">
const projects = [
  {
    id: 1,
    title: 'wanderlog',
    description: 'Planifica y organiza tus viajes. CRUD completo con autenticación y mapa interactivo de destinos.',
    tags: ['Vue 3', 'FastAPI', 'PostgreSQL', 'fullstack'],
    featured: true,
    emoji: '✈️',
    link: '#'
  },
  {
    id: 2,
    title: 'componentes UI',
    description: 'Librería de componentes reutilizables con animaciones y accesibilidad.',
    tags: ['Vue 3', 'CSS'],
    featured: false,
    emoji: '🧩',
    link: '#'
  },
  {
    id: 3,
    title: 'dashboard analytics',
    description: 'Visualización de datos en tiempo real con gráficas interactivas.',
    tags: ['Vue 3', 'D3.js'],
    featured: false,
    emoji: '📊',
    link: '#'
  }
]
</script>

<template>
  <section class="projects" id="proyectos">
    <div class="section-header">
      <p class="label">proyectos seleccionados</p>
    </div>

    <div class="grid">
      <div
        v-for="project in projects"
        :key="project.id"
        class="card"
        :class="{ featured: project.featured }"
        @click="() => project.link !== '#' && window.open(project.link)"
      >
        <div class="card-top">
          <span class="emoji">{{ project.emoji }}</span>
          <span v-if="project.featured" class="badge">destacado</span>
        </div>
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <div class="tags">
          <span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span>
        </div>
        <span class="arrow">→</span>
      </div>
    </div>
  </section>
</template>

<style scoped>
.projects {
  padding: 2.5rem 2rem;
  border-top: 1px solid var(--color-border);
}

.section-header {
  margin-bottom: 1.5rem;
}

.label {
  font-size: 11px;
  color: var(--color-text-muted);
  letter-spacing: 1px;
  text-transform: uppercase;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 12px;
}

.card {
  display: block;
  position: relative;
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  padding: 1.5rem;
  transition: border-color 0.2s, background 0.2s;
  cursor: pointer;
}

.card:hover {
  border-color: var(--color-border-strong);
  background: var(--color-surface-2);
}

.card.featured {
  grid-column: 1 / -1;
  display: grid;
  grid-template-columns: 1fr;
}

.card-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 1rem;
}

.emoji {
  font-size: 24px;
}

.badge {
  font-size: 11px;
  color: var(--color-accent);
  background: var(--color-accent-bg);
  border: 1px solid rgba(74, 222, 128, 0.2);
  border-radius: 4px;
  padding: 3px 10px;
}

h3 {
  font-size: 15px;
  font-weight: 500;
  color: var(--color-text);
  margin-bottom: 6px;
}

p {
  font-size: 13px;
  color: var(--color-text-secondary);
  line-height: 1.6;
  margin-bottom: 1.25rem;
}

.tags {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
}

.tag {
  font-size: 11px;
  color: var(--color-text-muted);
  background: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 4px;
  padding: 3px 8px;
}

.arrow {
  position: absolute;
  bottom: 1.5rem;
  right: 1.5rem;
  font-size: 14px;
  color: var(--color-text-muted);
  transition: color 0.15s, transform 0.15s;
}

.card:hover .arrow {
  color: var(--color-accent);
  transform: translateX(3px);
}
</style>