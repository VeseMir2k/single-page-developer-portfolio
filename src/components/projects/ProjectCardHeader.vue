<template>
  <div class="project-card-header">
    <h4 class="project-card-header__title">DESIGN PORTFOLIO</h4>
    <div class="project-card-header__tags">
      <div class="project-card-header__tag">HTML</div>
      <div class="project-card-header__tag">CSS</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCardHeader'
}
</script>

<style lang="scss" scoped>
.project-card-header {
  display: flex;
  flex-direction: column;
  gap: 7px;
  &__tags {
    @include tag-font;
    display: flex;
    gap: 18px;
  }
}
</style>
