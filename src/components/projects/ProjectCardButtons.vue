<template>
  <div class="project-card-buttons">
    <BasicButton text="view project" :link="links.project" />
    <BasicButton text="view code" :link="links.code" />
  </div>
</template>

<script>
import BasicButton from '../BasicButton.vue'

export default {
  name: 'ProjectCardButtons',
  components: { BasicButton },
  props: {
    links: { type: Object, required: true }
  }
}
</script>

<style lang="scss" scoped>
.project-card-buttons {
  display: flex;
  gap: 30px;
}
</style>
