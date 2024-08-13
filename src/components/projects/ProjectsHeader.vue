<template>
  <div class="projects-header">
    <h3 class="projects-header__title">Projects</h3>
    <BasicButton text="contact me" link="#" />
  </div>
</template>

<script>
import BasicButton from '../BasicButton.vue'

export default {
  name: 'ProjectsHeader',
  components: { BasicButton }
}
</script>

<style lang="scss" scoped>
.projects-header {
  display: flex;
  justify-content: space-between;
}
</style>
