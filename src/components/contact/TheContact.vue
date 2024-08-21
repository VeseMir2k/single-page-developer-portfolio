<template>
  <section class="contact-section">
    <ContactHeader />
    <ContactForm />
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
  display: flex;
  flex-direction: column;
  gap: 50px;
  padding: 60px 16px 90px;
}

@media (min-width: $tablet-breakpoint) {
  .contact-section {
    align-items: center;
  }
}
</style>
