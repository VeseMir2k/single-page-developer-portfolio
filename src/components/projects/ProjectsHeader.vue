<template>
  <div class="projects-header">
    <h3 class="projects-header__title">Projects</h3>
    <BasicButton text="contact me" link="#" />
  </div>
</template>

<script setup>
import BasicButton from '../BasicButton.vue'

defineOptions({
  name: 'ProjectsHeader'
})
</script>

<style lang="scss" scoped>
.projects-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 40px;
}
</style>
