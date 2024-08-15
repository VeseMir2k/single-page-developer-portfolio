<template>
  <section class="contact-section">
    <ContactHeader />
  </section>
</template>

<script>
import ContactHeader from './ContactHeader.vue'

export default {
  name: 'TheContact',
  components: { ContactHeader }
}
</script>

<style lang="scss" scoped>
.contact-section {
  background-color: $dark-gray-color;
  padding: 60px 16px 90px;
}
</style>
