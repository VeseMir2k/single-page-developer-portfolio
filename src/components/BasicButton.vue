<template>
  <a class="button" :href="link">{{ text }}</a>
</template>

<script>
export default {
  name: 'BasicButton',
  props: {
    link: {
      type: String
    },
    text: {
      type: String
    }
  }
}
</script>

<style lang="scss" scoped>
.button {
  @include button-font;
  display: inline-block;
  text-transform: uppercase;
  color: $white-color;
  text-decoration: none;
  padding-bottom: 12px;
  position: relative;
  &::after {
    content: '';
    display: block;
    height: 2px;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: $green-color;
  }
  &:hover {
    color: $green-color;
  }
}
</style>
