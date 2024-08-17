<template>
  <div class="contact-header">
    <h3 class="contact-header__title">Contact</h3>
    <p class="contact-header__info">
      I would love to hear about your project and how I could help. Please fill in the form, and
      I’ll get back to you as soon as possible.
    </p>
  </div>
</template>

<script setup>
defineOptions({
  name: 'ContactHeader'
})
</script>

<style lang="scss" scoped>
.contact-header {
  text-align: center;

  &__title {
    margin-bottom: 20px;
  }
  &__info {
    color: $grey-color;
  }
}
</style>
