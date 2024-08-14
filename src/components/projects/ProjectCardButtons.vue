<template>
  <div class="project-card-buttons">
    <BasicButton text="view project" />
    <BasicButton text="view code" />
  </div>
</template>

<script>
import BasicButton from '../BasicButton.vue'

export default {
  name: 'ProjectCardButtons',
  components: { BasicButton }
}
</script>

<style lang="scss" scoped>
.project-card-buttons {
  display: flex;
  gap: 30px;
}
</style>
