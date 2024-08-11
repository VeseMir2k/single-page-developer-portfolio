<template>
  <div class="intro">
    <h1 class="intro__title">Nice to meet you! I’m <span class="intro__name">Adam Keyes</span>.</h1>
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
  margin: 40px 0 24px;
  text-align: center;
  &__title {
    @include heading-xl-mobile-font;
    margin: 0 0 20px;
  }
  &__name {
    display: inline-block;
    border-bottom: 4px solid $green-color;
  }
  &__description {
    @include body-mobile-font;
    color: $grey-color;
  }
}
</style>
