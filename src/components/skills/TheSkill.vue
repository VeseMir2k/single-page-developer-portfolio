<template>
  <div class="skill">
    <h4 class="skill__title">{{ name }}</h4>
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
    margin: 0;
    margin-bottom: 1px;
    @include heading-l-mobile-font;
  }
  &__exp {
    @include body-mobile-font;
    color: $grey-color;
    margin: 0;
  }
}
</style>
