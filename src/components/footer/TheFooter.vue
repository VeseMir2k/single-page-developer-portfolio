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
  components: { TheLogo, TheSocials }
}
</script>

<style lang="scss" scoped>
.footer-section {
  position: relative;
  padding: 40px 16px 60px;
  background-color: $dark-grey-color;
  &__logo-socials {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }
  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 16px;
    right: 16px;
    height: 1px;
    background-color: $white-color;
  }
}
</style>
