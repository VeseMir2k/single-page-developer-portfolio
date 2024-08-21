<template>
  <article class="project-card">
    <ProjectCardImage :images="images" />
    <ProjectCardHeader :name="name" :tags="tags" />
    <ProjectCardButtons :links="links" />
  </article>
</template>

<script setup>
import ProjectCardHeader from './ProjectCardHeader.vue'
import ProjectCardButtons from './ProjectCardButtons.vue'
import ProjectCardImage from './ProjectCardImage.vue'

defineOptions({
  name: 'ProjectCard'
})

defineProps({
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
})
</script>

<style lang="scss" scoped>
.project-card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 20px;
}

@media (min-width: $tablet-breakpoint) {
  .project-card {
    flex-basis: calc(50% - 11px);
  }
}
</style>
