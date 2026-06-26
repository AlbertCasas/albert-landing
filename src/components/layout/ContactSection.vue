<template>
  <section class="contact" id="contacto">
    <div class="content">
      <div class="text">
        <h3>¿hablamos?</h3>
        <p>Abierto a oportunidades y colaboraciones</p>
      </div>
      <div class="links">
        <a href="mailto:tu@email.com" class="contact-btn">
          <span>✉</span> email
        </a>
        <a href="https://github.com/tuusuario" target="_blank" class="contact-btn">
          <span>⌥</span> github
        </a>
        <a href="https://linkedin.com/in/tuusuario" target="_blank" class="contact-btn">
          <span>in</span> linkedin
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  border-top: 1px solid var(--color-border);
  padding: 2.5rem 2rem;
  margin-top: 2rem;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
}

h3 {
  font-size: 16px;
  font-weight: 500;
  color: var(--color-text);
  margin-bottom: 4px;
}

p {
  font-size: 13px;
  color: var(--color-text-secondary);
}

.links {
  display: flex;
  gap: 8px;
}

.contact-btn {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 12px;
  color: var(--color-text-secondary);
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius);
  padding: 8px 16px;
  transition: color 0.15s, border-color 0.15s;
}

.contact-btn:hover {
  color: var(--color-text);
  border-color: var(--color-border-strong);
}
</style>