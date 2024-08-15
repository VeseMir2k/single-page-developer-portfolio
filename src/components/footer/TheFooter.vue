<template>
  <footer class="footer-section">
    <div class="footer-section__logo-socials">
      <TheLogo />
      <TheSocials />
    </div>
  </footer>
</template>

<script>
import TheLogo from '../TheLogo.vue'
import TheSocials from '../TheSocials.vue'

export default {
  name: 'TheFooter',
  components: {
    TheLogo,
    TheSocials
  }
}
</script>

<style lang="scss" scoped>
.footer-section {
  background-color: $dark-grey-color;
  padding: 40px 16px 60px;
  position: relative;

  &__logo-socials {
    align-items: center;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  &::before {
    background-color: $white-color;
    content: '';
    height: 1px;
    left: 16px;
    position: absolute;
    right: 16px;
    top: 0;
  }
}
</style>
