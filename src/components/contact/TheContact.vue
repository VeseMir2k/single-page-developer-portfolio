<template>
  <section class="contact-section">
    <div class="contact-section__container">
      <ContactHeader />
      <ContactForm />
    </div>
  </section>
</template>

<script setup>
import ContactForm from './ContactForm.vue'
import ContactHeader from './ContactHeader.vue'

defineOptions({
  name: 'TheContact'
})
</script>

<style lang="scss" scoped>
.contact-section {
  background-color: $dark-grey-color;
  padding: 60px 16px 90px;
  display: flex;
  justify-content: center;
  &__container {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }
}

@media (min-width: $tablet-breakpoint) {
  .contact-section {
    align-items: center;
  }
}

@media (min-width: $desktop-breakpoint) {
  .contact-section {
    width: 100%;
    padding: 90px 16px;
    &__container {
      width: 1120px;
      flex-direction: row;
      justify-content: space-between;
    }
  }
}
</style>
