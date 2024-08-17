<template>
  <a class="button" :href="link">{{ text }}</a>
</template>

<script setup>
defineOptions({
  name: 'BasicButton'
})

defineProps({
  link: {
    type: String
  },
  text: {
    type: String
  }
})
</script>

<style lang="scss" scoped>
.button {
  @include button-font;
  color: $white-color;
  display: inline-block;
  padding-bottom: 12px;
  position: relative;
  text-decoration: none;
  text-transform: uppercase;

  &::after {
    background-color: $green-color;
    bottom: 0;
    content: '';
    display: block;
    height: 2px;
    left: 0;
    position: absolute;
    right: 0;
  }
  &:hover {
    color: $green-color;
  }
}
</style>
