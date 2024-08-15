<template>
  <header class="header-section">
    <div class="header-section__logo-socials">
      <TheLogo />
      <TheSocials />
    </div>
    <img class="header-section__profile-image" :src="profileImage" alt="" />
    <img class="header-section__rings-pattern" :src="ringsPattern" alt="" />
    <img class="header-section__circle-pattern" :src="circlePattern" alt="" />
    <HeaderIntro />
  </header>
</template>

<script>
import TheLogo from '../TheLogo.vue'
import TheSocials from '../TheSocials.vue'
import HeaderIntro from './HeaderIntro.vue'
import profileImage from '../../assets/image-profile-mobile.webp'
import circlePattern from '../../assets/pattern-circle.svg'
import ringsPattern from '../../assets/pattern-rings.svg'

export default {
  name: 'TheHeader',
  components: {
    TheLogo,
    TheSocials,
    HeaderIntro
  },
  setup() {
    return {
      profileImage,
      circlePattern,
      ringsPattern
    }
  }
}
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
  &__rings-pattern {
    left: -350px;
    position: absolute;
    top: 130px;
    z-index: -1;
  }
  &__circle-pattern {
    position: absolute;
    right: -65px;
    top: 265px;
  }
}
</style>
