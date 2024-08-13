<template>
  <TheHeader />
  <TheSkills />
  <TheProjects />
</template>

<script>
import TheHeader from './components/header/TheHeader.vue'
import TheProjects from './components/projects/TheProjects.vue'
import TheSkills from './components/skills/TheSkills.vue'

export default {
  name: 'App',
  components: { TheHeader, TheSkills, TheProjects }
}
</script>

<style lang="scss" scoped></style>
