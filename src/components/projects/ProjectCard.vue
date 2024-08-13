<template>
  <article class="project-card">
    <img class="project-card__img" src="../../assets/thumbnail-project-1-small.webp" alt="" />
    <ProjectCardHeader />
    <div class="project-card__buttons"></div>
  </article>
</template>

<script>
import ProjectCardHeader from './ProjectCardHeader.vue'

export default {
  name: 'ProjectCard',
  components: { ProjectCardHeader }
}
</script>

<style lang="scss" scoped>
.project-card {
  display: flex;
  flex-direction: column;
  gap: 20px;
  &__img {
    width: 100%;
  }
}
</style>
