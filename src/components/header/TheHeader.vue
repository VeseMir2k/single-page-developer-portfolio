<template>
  <header class="header">
    <div class="header__logo-socials">
      <TheLogo />
      <TheSocials />
    </div>
    <img class="header__profile-image" :src="profileImage" alt="" />
    <img class="header__rings-pattern" :src="ringsPattern" alt="" />
    <img class="header__circle-pattern" :src="circlePattern" alt="" />
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
  components: { TheLogo, TheSocials, HeaderIntro },
  setup() {
    return { profileImage, circlePattern, ringsPattern }
  }
}
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 16px 80px;
  &__logo-socials {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    top: 20px;
    gap: 20px;
    text-align: center;
  }
  &__profile-image {
    width: 180px;
  }
  &__rings-pattern {
    position: absolute;
    top: 130px;
    left: -350px;
    z-index: -1;
  }
  &__circle-pattern {
    position: absolute;
    top: 265px;
    right: -65px;
  }
}
</style>
