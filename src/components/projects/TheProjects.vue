<template>
  <section class="projects-section">
    <ProjectsHeader />
    <ProjectCard />
  </section>
</template>

<script>
import ProjectCard from './ProjectCard.vue'
import ProjectsHeader from './ProjectsHeader.vue'

export default {
  name: 'TheProjects',
  components: { ProjectsHeader, ProjectCard }
}
</script>

<style lang="scss" scoped>
.projects-section {
  padding: 80px 0;
}
</style>
