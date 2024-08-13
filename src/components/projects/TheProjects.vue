<template>
  <section class="projects-section">
    <ProjectsHeader />
  </section>
</template>

<script>
import ProjectsHeader from './ProjectsHeader.vue'

export default {
  name: 'TheProjects',
  components: { ProjectsHeader }
}
</script>

<style lang="scss" scoped>
.projects-section {
  padding: 80px 0;
}
</style>
