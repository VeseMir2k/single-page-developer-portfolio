<template>
  <div class="project-card-buttons">
    <BasicButton text="view project" :link="links.project" />
    <BasicButton text="view code" :link="links.code" />
  </div>
</template>

<script setup>
import BasicButton from '../BasicButton.vue'

defineOptions({
  name: 'ProjectCardButtons'
})

defineProps({
  links: {
    type: Object,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.project-card-buttons {
  display: flex;
  gap: 30px;
}

@media (min-width: $desktop-breakpoint) {
  .project-card-buttons {
  }
}
</style>
