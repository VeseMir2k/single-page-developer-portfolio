<template>
  <form class="form" @submit.prevent="submitForm" novalidate>
    <div class="form__group">
      <input
        class="form__input"
        v-model="form.username"
        @blur="validateField(form.username, 3, 24, errors.username, 'Username')"
        type="text"
        placeholder="name"
      />
      <span v-if="errors.username" class="form__error">{{ errors.username }}</span>
    </div>
    <div class="form__group">
      <input
        class="form__input"
        v-model="form.email"
        @blur="validateEmail"
        type="email"
        placeholder="email"
      />
      <span v-if="errors.email" class="form__error">{{ errors.email }}</span>
    </div>
    <div class="form__group">
      <textarea
        class="form__textarea"
        v-model="form.message"
        @blur="validateField(form.message, 3, 244, errors.message, 'Message')"
        rows="4"
        placeholder="message"
      ></textarea>
      <span v-if="errors.message" class="form__error">{{ errors.message }}</span>
    </div>
    <button class="form__button" type="submit">SEND MESSAGE</button>
  </form>
</template>

<script setup>
import { reactive } from 'vue'

defineOptions({
  name: 'ContactForm'
})

const form = reactive({
  username: '',
  email: '',
  message: ''
})

const errors = reactive({
  username: '',
  email: '',
  message: ''
})

const validateField = (field, min, max, errKey, name) => {
  if (field.trim().length <= 0) {
    errors[errKey] = `${name} is required.`
  } else if (field.trim().length < min) {
    errors[errKey] = `${name} must be at least ${min} characters long.`
  } else if (field.trim().length > max) {
    errors[errKey] = `${name} must be less than ${max} characters long.`
  } else {
    errors[errKey] = null
  }
}

const validateEmail = () => {
  if (form.email.trim().length <= 0) {
    errors.email = 'Email is required.'
  } else {
    const emailPattern = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/
    if (!emailPattern.test(form.email.trim())) {
      errors.email = 'Please enter a valid email address.'
    } else {
      errors.email = null
    }
  }
}

const submitForm = () => {
  validateField(form.username, 3, 24, 'username', 'Username')
  validateEmail()
  validateField(form.message, 3, 244, 'message', 'Message')

  if (!errors.username && !errors.email && !errors.message) {
    console.log('Send')
  } else {
    console.log('Errors present:', errors)
  }
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

  &__group {
    display: flex;
    flex-direction: column;
  }

  &__error {
    color: $red-color;
    @include error-font;
    text-align: right;
  }

  &__input,
  &__textarea {
    @include body-mobile-font;
    position: relative;
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
