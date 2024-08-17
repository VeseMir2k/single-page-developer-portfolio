<template>
  <form class="form" @submit.prevent="handleSubmitForm">
    <input class="form__input" type="text" placeholder="name" />
    <input class="form__input" type="text" placeholder="email" />
    <textarea class="form__textarea" rows="4" placeholder="message"></textarea>
    <button class="form__button" type="submit">SEND MESSAGE</button>
  </form>
</template>

<script setup>
defineOptions({
  name: 'ContactForm'
})

const handleSubmitForm = () => {
  console.log('Wysłano')
}
</script>

<style lang="scss" scoped>
.form {
  display: flex;
  flex-direction: column;
  gap: 32px;
  position: relative;

  &::after {
    background-image: url('../../assets/pattern-rings.svg');
    bottom: 7px;
    content: '';
    height: 129px;
    position: absolute;
    right: 50%;
    width: 530px;
  }

  &__input,
  &__textarea {
    @include body-mobile-font;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid $white-color;
    color: $white-color;
    padding-left: 24px;
    padding-bottom: 16px;
    z-index: 1;

    &:focus {
      border-bottom-color: $green-color;
      outline: none;
    }
    &::placeholder {
      text-transform: uppercase;
    }
  }
  &__button {
    @include button-font;
    align-self: flex-end;
    background-color: transparent;
    border: 0;
    border-bottom: 2px solid $green-color;
    color: $white-color;
    cursor: pointer;
    padding-bottom: 10px;

    &:hover {
      color: $green-color;
    }
  }
}
</style>
