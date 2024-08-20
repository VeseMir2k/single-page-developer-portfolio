<template>
  <header class="header-section">
    <div class="header-section__logo-socials">
      <TheLogo />
      <TheSocials />
    </div>
    <img class="header-section__profile-image" :src="profileImage" alt="" />
    <HeaderIntro />
  </header>
</template>

<script setup>
import TheLogo from '../TheLogo.vue'
import TheSocials from '../TheSocials.vue'
import HeaderIntro from './HeaderIntro.vue'
import profileImage from '../../assets/image-profile-mobile.webp'

defineOptions({
  name: 'TheHeader'
})
</script>

<style lang="scss" scoped>
.header-section {
  align-items: center;
  display: flex;
  flex-direction: column;
  padding: 0 16px 80px;
  position: relative;

  &__logo-socials {
    align-items: center;
    display: flex;
    flex-direction: column;
    gap: 20px;
    position: absolute;
    top: 20px;
    width: 100%;
  }
  &__profile-image {
    width: 180px;
  }
  &::before {
    content: '';
    width: 530px;
    height: 129px;
    position: absolute;
    top: 124px;
    right: 50%;
    z-index: -1;
    background-image: url('../../assets/pattern-rings.svg');
  }

  &::after {
    content: '';
    width: 129px;
    height: 129px;
    position: absolute;
    top: 264px;
    right: calc(50% - 250px);
    background-image: url('../../assets/pattern-circle.svg');
  }
}

@media (min-width: $tablet-breakpoint) {
  .header-section {
    &__logo-socials {
      flex-direction: row;
      justify-content: space-between;
      top: 30px;
      left: 32px;
      right: 32px;
      width: auto;
    }
  }
}
</style>
