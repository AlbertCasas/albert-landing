<script setup lang="ts">
const projects = [
  {
    id: 1,
    title: 'wanderlog',
    description: 'Plan and organize your trips. Full CRUD app with authentication, interactive destination map and travel stats.',
    tags: ['Vue.js', 'FastAPI', 'MySQL', 'fullstack'],
    featured: true,
    emoji: '✈️',
    link: 'https://wanderlog-frontend-seven.vercel.app'
  },
  {
    id: 2,
    title: 'UI component library',
    description: 'Reusable component system with animations, accessibility and full TypeScript support.',
    tags: ['Vue.js', 'TypeScript', 'SCSS'],
    featured: false,
    emoji: '🧩',
    link: '#'
  },
  {
    id: 3,
    title: 'analytics dashboard',
    description: 'Real-time data visualization with interactive charts and filtering.',
    tags: ['Vue.js', 'D3.js', 'REST API'],
    featured: false,
    emoji: '📊',
    link: '#'
  }
]

function openProject(link: string) {
  if (link !== '#') {
    window.open(link, '_blank')
  }
}
</script>

<template>
  <section class="projects" id="projects">
    <div class="section-header">
      <p class="label">selected projects</p>
    </div>

    <div class="grid">
      <div
        v-for="project in projects"
        :key="project.id"
        class="card"
        :class="{ featured: project.featured }"
        @click="openProject(project.link)"
      >
        <div class="card-top">
          <span class="emoji">{{ project.emoji }}</span>
          <span v-if="project.featured" class="badge">featured</span>
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