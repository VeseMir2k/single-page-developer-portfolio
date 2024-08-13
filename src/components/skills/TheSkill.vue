<template>
  <div class="skill-card">
    <h3 class="skill-card__title">{{ name }}</h3>
    <p class="skill-card__exp">{{ exp }} Experience</p>
  </div>
</template>

<script>
export default {
  name: 'TheSkill',
  props: {
    name: {
      type: String
    },
    exp: {
      type: String
    }
  }
}
</script>

<style lang="scss" scoped>
.skill-card {
  text-align: center;
  &__title {
    margin-bottom: 1px;
  }
  &__exp {
    color: $grey-color;
  }
}
</style>
