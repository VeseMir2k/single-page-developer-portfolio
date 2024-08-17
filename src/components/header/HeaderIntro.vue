<template>
  <div class="header-intro">
    <h2 class="header-intro__title">
      Nice to meet you! I'm <span class="header-intro__name">Adam Keyes</span>.
    </h2>
    <p class="header-intro__description">
      Based in the UK, I'm a front-end developer passionate about building accessible web apps that
      users love.
    </p>
    <BasicButton link="#" text="contact me" />
  </div>
</template>

<script setup>
import BasicButton from '../BasicButton.vue'

defineOptions({
  name: 'HeaderIntro'
})
</script>

<style lang="scss" scoped>
.header-intro {
  margin-top: 40px;
  text-align: center;

  &__title {
    margin-bottom: 20px;
  }
  &__name {
    border-bottom: 4px solid $green-color;
    display: inline-block;
  }
  &__description {
    color: $grey-color;
    margin-bottom: 24px;
  }
}
</style>
