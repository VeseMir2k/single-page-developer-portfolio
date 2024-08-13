<template>
  <div class="skill">
    <h3 class="skill__title">{{ name }}</h3>
    <p class="skill__exp">{{ exp }} Experience</p>
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
.skill {
  text-align: center;
  &__title {
    margin-bottom: 1px;
  }
  &__exp {
    color: $grey-color;
  }
}
</style>
