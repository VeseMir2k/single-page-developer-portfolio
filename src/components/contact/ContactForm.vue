<template>
  <form class="form" @submit.prevent="submitForm" novalidate>
    <div class="form__group">
      <input
        :class="['form__input', { 'form__input--error': errors.username }]"
        v-model="form.username"
        @blur="validateField('username', 3, 24, 'Username')"
        type="text"
        placeholder="name"
      />
      <span v-if="errors.username" class="form__error">{{ errors.username }}</span>
    </div>
    <div class="form__group">
      <input
        :class="['form__input', { 'form__input--error': errors.email }]"
        v-model="form.email"
        @blur="validateEmail"
        type="email"
        placeholder="email"
      />
      <span v-if="errors.email" class="form__error">{{ errors.email }}</span>
    </div>
    <div class="form__group">
      <textarea
        :class="['form__textarea', { 'form__textarea--error': errors.message }]"
        v-model="form.message"
        @blur="validateField('message', 3, 244, 'Message')"
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

const validateField = (field, min, max, name) => {
  const value = form[field].trim()
  if (value.length === 0) {
    errors[field] = `${name} is required.`
  } else if (value.length < min) {
    errors[field] = `${name} must be at least ${min} characters long.`
  } else if (value.length > max) {
    errors[field] = `${name} must be less than ${max} characters long.`
  } else {
    errors[field] = null
  }
}

const validateEmail = () => {
  const value = form.email.trim()
  const emailPattern = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/
  if (value.length === 0) {
    errors.email = 'Email is required.'
  } else if (!emailPattern.test(value)) {
    errors.email = 'Please enter a valid email address.'
  } else {
    errors.email = null
  }
}

const submitForm = () => {
  validateField('username', 3, 24, 'Username')
  validateEmail()
  validateField('message', 3, 244, 'Message')

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
    position: relative;
  }

  &__error {
    color: $red-color;
    @include error-font;
    position: absolute;
    bottom: -20px;
    right: 0;
  }

  &__input,
  &__textarea {
    flex-grow: 1;
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

    &--error {
      border-bottom-color: $red-color;
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

@media (min-width: $tablet-breakpoint) {
  .form {
    width: 445px;
    &::after {
      bottom: -65px;
      left: -120%;
    }
  }
}

@media (min-width: $desktop-breakpoint) {
  .form {
    &::after {
      bottom: -40px;
      left: -230%;
    }
  }
}
</style>
