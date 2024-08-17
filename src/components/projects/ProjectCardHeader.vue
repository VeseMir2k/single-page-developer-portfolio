<template>
  <div class="project-card-header">
    <h4 class="project-card-header__title">{{ name }}</h4>
    <div class="project-card-header__tags">
      <div class="project-card-header__tag" v-for="tag in tags" :key="tag">{{ tag }}</div>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: 'ProjectCardHeader'
})

defineProps({
  name: {
    type: String,
    required: true
  },
  tags: {
    type: Array,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.project-card-header {
  display: flex;
  flex-direction: column;
  gap: 7px;

  &__title {
    text-transform: uppercase;
  }
  &__tags {
    @include tag-font;
    display: flex;
    gap: 18px;
    text-transform: uppercase;
  }
}
</style>
