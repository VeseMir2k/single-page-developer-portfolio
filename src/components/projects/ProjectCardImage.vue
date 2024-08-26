<template>
  <img class="project-card-image" :src="images.small" alt="" />
</template>

<script setup>
defineOptions({
  name: 'ProjectCardImage'
})

defineProps({
  images: {
    type: Object,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.project-card-image {
  width: 100%;
}

@media (min-width: $desktop-breakpoint) {
  .project-card-image {
  }
}
</style>
