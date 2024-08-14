<template>
  <article class="project-card">
    <ProjectCardImage />
    <ProjectCardHeader />
    <ProjectCardButtons />
  </article>
</template>

<script>
import ProjectCardHeader from './ProjectCardHeader.vue'
import ProjectCardButtons from './ProjectCardButtons.vue'
import ProjectCardImage from './ProjectCardImage.vue'

export default {
  name: 'ProjectCard',
  components: { ProjectCardImage, ProjectCardHeader, ProjectCardButtons }
}
</script>

<style lang="scss" scoped>
.project-card {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
