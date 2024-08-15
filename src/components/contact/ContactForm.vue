<template>
  <form class="form">
    <input class="form__input" type="text" placeholder="name" />
    <input class="form__input" type="text" placeholder="email" />
    <textarea class="form__textarea" rows="1" placeholder="message"></textarea>
  </form>
</template>

<script>
export default {
  name: 'ContactForm'
}
</script>

<style lang="scss" scoped>
.form {
  display: flex;
  flex-direction: column;
  gap: 32px;
  &__input,
  &__textarea {
    background-color: transparent;
    border: none;
    color: $white-color;
    @include body-mobile-font;
    border-bottom: 1px solid $white-color;
    padding-left: 24px;
  }
  &__input {
    padding-bottom: 16px;
  }
  &__textarea {
    padding-bottom: 80px;
  }
  &__input:focus,
  &__textarea:focus {
    outline: none;
    border-bottom-color: $green-color;
  }
  &__input::placeholder,
  &__textarea::placeholder {
    text-transform: uppercase;
  }
}
</style>
