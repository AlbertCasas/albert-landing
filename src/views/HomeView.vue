<script setup lang="ts">
import NavBar from '../components/layout/NavBar.vue'
import HeroSection from '../components/layout/HeroSection.vue'
import StackSection from '../components/layout/StackSection.vue'
import ProjectsSection from '../components/layout/ProjectsSection.vue'
import ContactSection from '../components/layout/ContactSection.vue'
</script>

<template>
  <div>
    <NavBar />
    <main>
      <HeroSection />
      <StackSection />
      <ProjectsSection />
      <ContactSection />
    </main>
  </div>
</template>