<template>
  <TheHeader />
  <TheSkills />
</template>

<script>
import TheHeader from './components/header/TheHeader.vue'
import TheSkills from './components/skills/TheSkills.vue'

export default {
  name: 'App',
  components: { TheHeader, TheSkills }
}
</script>

<style lang="scss" scoped></style>
