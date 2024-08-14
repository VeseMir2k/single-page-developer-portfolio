<template>
  <article class="project-card">
    <ProjectCardImage :images="images" />
    <ProjectCardHeader :name="name" :tags="tags" />
    <ProjectCardButtons :links="links" />
  </article>
</template>

<script>
import ProjectCardHeader from './ProjectCardHeader.vue'
import ProjectCardButtons from './ProjectCardButtons.vue'
import ProjectCardImage from './ProjectCardImage.vue'

export default {
  name: 'ProjectCard',
  components: { ProjectCardImage, ProjectCardHeader, ProjectCardButtons },
  props: {
    name: {
      type: String,
      required: true
    },
    images: {
      type: Object,
      required: true
    },
    tags: {
      type: Array,
      required: true
    },
    links: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.project-card {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
