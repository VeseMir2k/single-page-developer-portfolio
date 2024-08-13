<template>
  <div class="intro">
    <h2 class="intro__title">Nice to meet you! I'm <span class="intro__name">Adam Keyes</span>.</h2>
    <p class="intro__description">
      Based in the UK, I’m a front-end developer passionate about building accessible web apps that
      users love.
    </p>
    <BasicButton link="#" text="contact me" />
  </div>
</template>

<script>
import BasicButton from '../BasicButton.vue'

export default {
  name: 'HeaderIntro',
  components: { BasicButton }
}
</script>

<style lang="scss" scoped>
.intro {
  text-align: center;
  margin-top: 40px;
  &__title {
    margin-bottom: 20px;
  }
  &__name {
    display: inline-block;
    border-bottom: 4px solid $green-color;
  }
  &__description {
    color: $grey-color;
    margin-bottom: 24px;
  }
}
</style>
