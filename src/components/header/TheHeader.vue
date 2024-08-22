<template>
  <header class="header-section">
    <div class="header-section__logo-socials">
      <TheLogo />
      <TheSocials />
    </div>
    <picture>
      <source media="(min-width: 1200px)" :srcset="profileImageDesktop" />
      <source media="(min-width: 768px)" :srcset="profileImageTablet" />
      <img class="header-section__profile-image" :src="profileImageMobile" alt="" />
    </picture>
    <HeaderIntro />
  </header>
</template>

<script setup>
import TheLogo from '../TheLogo.vue'
import TheSocials from '../TheSocials.vue'
import HeaderIntro from './HeaderIntro.vue'
import profileImageMobile from '../../assets/image-profile-mobile.webp'
import profileImageTablet from '../../assets/image-profile-tablet.webp'
import profileImageDesktop from '../../assets/image-profile-desktop.webp'

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
    height: 660px;
    padding: 0 32px 0;
    display: block;
    &__logo-socials {
      flex-direction: row;
      justify-content: space-between;
      top: 30px;
      left: 32px;
      right: 32px;
      width: auto;
    }
    &__profile-image {
      width: auto;
      height: 600px;
      position: absolute;
      right: 0;
      top: 0;
      z-index: -1;
    }
    &::before {
      top: 85px;
      right: 65%;
    }
    &::after {
      top: 470px;
      right: calc(0px - 65px);
    }
  }
}

@media (min-width: $desktop-breakpoint) {
  .header-section {
    padding: 0;
    height: 820px;
    width: 1120px;

    &__logo-socials {
      left: 0;
      right: 32px;
    }
    &__profile-image {
      height: 720px;
      width: 445px;
    }
    &::before {
      top: 135px;
      left: -20%;
    }
    &::after {
      top: 520px;
      right: 35%;
    }
  }
}
</style>
