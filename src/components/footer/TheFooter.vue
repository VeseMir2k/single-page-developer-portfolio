<template>
  <footer class="footer-section">
    <div class="footer-section__logo-socials">
      <TheLogo />
      <TheSocials />
    </div>
  </footer>
</template>

<script setup>
import TheLogo from '../TheLogo.vue'
import TheSocials from '../TheSocials.vue'

defineOptions({
  name: 'TheFooter'
})
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

@media (min-width: $tablet-breakpoint) {
  .footer-section {
    padding: 30px 32px 40px;
    &__logo-socials {
      flex-direction: row;
      justify-content: space-between;
    }
    &::before {
      left: 32px;
      right: 32px;
    }
  }
}

@media (min-width: $desktop-breakpoint) {
  .footer-section {
    width: 100%;
    display: flex;
    justify-content: center;
    &__logo-socials {
      width: 1120px;
    }
    &::before {
      width: 1120px;
      left: 50%;
      transform: translateX(-50%);
    }
  }
}
</style>
