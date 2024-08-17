<template>
  <div class="socials">
    <a class="socials__social" v-for="icon in socialIcons" :key="icon.name" :href="icon.link">
      <img class="socials__icon" :src="icon.src" :alt="icon.name" />
    </a>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import gitHubIcon from '../assets/icon-github.svg'
import frontendMentorIcon from '../assets/icon-frontend-mentor.svg'
import likedInIcon from '../assets/icon-linkedin.svg'
import twitterIcon from '../assets/icon-twitter.svg'

defineOptions({
  name: 'TheSocials'
})

const socialIcons = ref([
  {
    name: 'GitHub',
    src: gitHubIcon,
    link: '#'
  },
  {
    name: 'FrontendMentor',
    src: frontendMentorIcon,
    link: '#'
  },
  {
    name: 'LinkedIn',
    src: likedInIcon,
    link: '#'
  },
  {
    name: 'Twitter',
    src: twitterIcon,
    link: '#'
  }
])
</script>

<style lang="scss" scoped>
.socials {
  display: flex;
  gap: 25px;

  &__icon {
    width: 20px;
  }
}
</style>
