<template>
  <TheHeader />
  <main class="main">
    <TheSkills />
    <TheProjects />
  </main>
  <TheContact />
  <TheFooter />
</template>

<script setup>
import TheContact from './components/contact/TheContact.vue'
import TheFooter from './components/footer/TheFooter.vue'
import TheHeader from './components/header/TheHeader.vue'
import TheProjects from './components/projects/TheProjects.vue'
import TheSkills from './components/skills/TheSkills.vue'

defineOptions({
  name: 'App'
})
</script>

<style lang="scss" scoped>
@media (min-width: $desktop-breakpoint) {
  .main {
    width: 1120px;
  }
}
</style>
