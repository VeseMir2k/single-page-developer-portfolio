<template>
  <section class="contact-section">
    <ContactHeader />
    <ContactForm />
  </section>
</template>

<script>
import ContactForm from './ContactForm.vue'
import ContactHeader from './ContactHeader.vue'

export default {
  name: 'TheContact',
  components: {
    ContactHeader,
    ContactForm
  }
}
</script>

<style lang="scss" scoped>
.contact-section {
  background-color: $dark-grey-color;
  display: flex;
  flex-direction: column;
  gap: 50px;
  padding: 60px 16px 90px;
}
</style>
