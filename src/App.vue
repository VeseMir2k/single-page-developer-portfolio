<template>
  <TheHeader />
  <TheSkills />
  <TheProjects />
  <TheContact />
  <TheFooter />
</template>

<script>
import TheContact from './components/contact/TheContact.vue'
import TheFooter from './components/footer/TheFooter.vue'
import TheHeader from './components/header/TheHeader.vue'
import TheProjects from './components/projects/TheProjects.vue'
import TheSkills from './components/skills/TheSkills.vue'

export default {
  name: 'App',
  components: { TheHeader, TheSkills, TheProjects, TheContact, TheFooter }
}
</script>

<style lang="scss" scoped></style>
