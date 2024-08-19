<template>
  <TheHeader />
  <main>
    <TheSkills />
    <TheProjects />
    <TheContact />
  </main>
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

<style lang="scss" scoped></style>
