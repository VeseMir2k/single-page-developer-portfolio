<template>
  <img class="project-card-image" :src="images.small" alt="" />
</template>

<script>
export default {
  name: 'ProjectCardImage',
  props: {
    images: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.project-card-image {
  width: 100%;
}
</style>
