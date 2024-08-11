<template>
  <div class="intro">
    <h1 class="intro__title">Nice to meet you! I’m Adam Keyes.</h1>
    <p class="intro__description">
      Based in the UK, I’m a front-end developer passionate about building accessible web apps that
      users love.
    </p>
    <button class="intro__button">CONTACT ME</button>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.intro {
  text-align: center;
  &__title {
    @include heading-xl-mobile-font;
  }
  &__description {
    @include body-mobile-font;
    color: $grey-color;
  }
}
</style>
